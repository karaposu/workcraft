
---
name: non-explicitness-fix
description: Fix the explicitness gaps that non-explicitness-detection found, on a copy of the source. Fresh agents decide every gap (fixed with a quoted basis, asked as an author question, or declined) in one shared missing-meanings table and write wording proposals (one agent for short texts, one per section in parallel for long ones); this session asks the author once, applies the proposals mechanically, runs a trace script and one independent reviewer, and returns the revised copy, the table, the questions, the diff and the record. Never invents a particular; no detection loop.
---

# non-explicitness-fix: decide, word, apply, check

This skill turns an explicitness detection run into a revised copy of the source.

**An explicitness gap** is a place where the wording needs something particular (which one, of what, who, what is done, by what criterion, which system, when or where) and the text does not single it out.

**Every gap is decided, one by one, with exactly one outcome:**
- **fixed:** something establishes the missing meaning; the fix quotes it;
- **asked:** nothing establishes it; it becomes a question for the author;
- **declined:** the text already singles it out at or before that point; the decline quotes those words.

**The text is changed only for fixed gaps.** Nothing is ever invented.

**The work has four layers:**

| Layer | What happens | Who does it |
|---|---|---|
| Decide | the missing-meanings table: one row per missing meaning, with its outcome, exact wording, first-use place and basis | one fresh agent |
| Word | replacement proposals, per sentence | one fresh agent for short texts; one per section, in parallel, for long texts |
| Apply | literal replacement of the proposals | this session, mechanically |
| Check | a trace script, then one fresh reviewer, once | this session plus one fresh agent |

**Two rules about who does what:**
- This session never decides or words. A session that discussed the text knows meanings the text does not state. It would decline real gaps and use invisible bases.
- This session's role: orchestrate, talk to the author, apply, run the scripts.

**Invocation:** `/non-explicitness-fix <source> [detection: <run folder>] [basis: <files>] [answers: <file>] [batch] [band: short|long] [review-proposals] [model: <name>]`. Every part except the source is optional.

Outside a skill-aware session: "Read `<this folder>/SKILL.md` in full and execute it on `<source>`."

## Step 1: Settle the inputs

1. **Source.** The file to fix. It is never edited.
2. **Detection run folder.** It contains `document-numbered.md`, `run.md` and `run1/` (optionally `run2/`) with the per-section JSONL rows.
   - Take it from the invocation, or the newest `outputs/explicitness-*` folder beside the source whose `run.md` names this source.
   - If none exists, run the `non-explicitness-detection` skill on the source first (default options), then continue.
   - If the source changed after the detection ran (its text no longer matches `document-numbered.md` without the numbers), say so and run detection again.
3. **Basis files.** Optional: a request, a brief, source documents. These are the only outside material a fix may draw meaning from.
   - **Conversation facts.** If this conversation contains facts about the text's subject that the author wants to count (who, which system, which document), offer once to write them to `context.md` in the run folder. Write only what the author approves. Facts not written there do not count.
4. **Answers file.** Optional: a filled-in `questions.md` from an earlier run of this skill on the same source. If given:
   - work in a new run folder;
   - copy that run's `table.jsonl` and `gaps-input.jsonl` into it;
   - use the earlier run's fixed copy as `original.md`;
   - apply the filled answers as in Step 3, item 4;
   - continue at Step 4, in `word-rows` mode for the newly fixed rows, then Steps 5–7.
5. **Mode.** Interactive by default (ask the author in this session). `batch` writes the questions and stops.
6. **Model.** The model named in the invocation; otherwise `opus` where available; otherwise the session's model.
7. **Run folder.** `outputs/fix-<YYYY-MM-DD_HHMM>/` beside the source. Create it and never reuse it.
   - Copy the source into it as `original.md`.
   - Copy any basis files into `basis/`.
   - Write `run.md` with the inputs, the mode and the model.
8. **Gap list.** Write `gaps-input.jsonl` in the run folder. A throwaway script may do this. Take every row from every `run*/` JSONL file of the detection run whose `answer` is LATER, MULTIPLE, CONFLICT, CANNOT or UNSPECIFIC. Give each row an id `r<k>-<n>` (run k, n-th gap row in line order). Keep these fields:
   - `line`
   - `trigger`
   - `slot`
   - `qid`
   - `answer`
   - `quote`
   - `candidates`
   - `earlier_mention`
   - `main_point`
   - `note`
   - `via`

   Record the count in `run.md`.
9. **Band.** Count the source's words.
   - Up to 1,800 words is the **short band**.
   - Above that is the **long band**.
   - `band:` in the invocation overrides this.
   - In the long band, the wording sections are the detection run's sections: the line ranges in its file names `s<k>-L<first>-<last>.jsonl`.

## Step 2: Decide (and, in the short band, word)

Launch **one** fresh subagent (not a fork) with this prompt, placeholders filled with absolute paths:

```
Read <SKILL>/references/fixer-instructions.md in full and follow it exactly, with ROLE = <decide-and-word | decide>, SOURCE = <RUN>/original.md, NUMBERED = <DETECTION>/document-numbered.md, GAPS = <RUN>/gaps-input.jsonl, BASIS = <RUN>/basis/ (and <RUN>/context.md if present), TABLE = <RUN>/table.jsonl, PROPOSALS = <RUN>/proposals-all.jsonl.
```

- **Short band:** `ROLE = decide-and-word`.
- **Long band:** `ROLE = decide`.
- **Launching:**
  - Claude Code: the Agent tool, `subagent_type: general-purpose`, `model` set.
  - Codex: `spawn_agent` without `fork_context`.
  - Without subagents: return the filled prompts and stop.

Wait for it. Then check that `table.jsonl` exists, and that every id in `gaps-input.jsonl` appears in exactly one row's `gaps`. Rows that miss ids get one relaunch with the missing ids named; after that, list any still missing in the return.

## Step 3: The author round

1. Write `questions.md` from the `asked` rows. Order them by the number of gap ids each covers, largest first. For each:
   - the location (first line);
   - the quoted words;
   - the question;
   - the choices, if any, plus "as written is fine";
   - an empty `Answer:` line.
2. **Batch mode:** do not ask. The asked rows stay open. Continue with Steps 4–7 for the rows that are already fixed. In the return, say: "fill in the Answer lines and run again with `answers: <run>/questions.md`".
3. **Interactive mode:** show the author the questions, all at once and briefly (the location, the words, the question, the choices), and ask for answers. Accept partial answers.
4. For each answer, update its row in `table.jsonl`:
   - **A usable answer** (a choice letter, a stated particular, or "use the suggestion" where a suggestion exists): set `status` to `fixed`, `basis_source` to `author`, `basis` to the answer verbatim (with the chosen choice's text spelled out when the answer is a letter), and `wording` to that same text, unedited. The wording agent shapes it into the sentence; this session does not compose wording.
   - **"As written is fine":** set `status` to `declined`, with `decline_quote` set to "author: as written is fine".
   - **No answer, or an unusable one:** the row stays `asked`.

## Step 4: Word

- **Short band:**
  - If Step 3 fixed new rows, launch one subagent with `ROLE = word-rows`, `ROWS = <the newly fixed row ids>` and `PROPOSALS = <RUN>/proposals-answers.jsonl`.
  - Otherwise skip this step.
- **Long band:** launch one subagent per section, all at once. Each gets `ROLE = word-section`, `FIRST`/`LAST` = the section's line range, and `PROPOSALS = <RUN>/proposals-s<k>.jsonl`.
  - If parallel launch is not available, run the sections one after another in one subagent: `ROLE = word-section` with each range in turn.

Wait for all. Collect each agent's `table notes` (in its reply) into `run.md`.

## Step 5: Apply, mechanically

Apply in this session. A throwaway script is the expected way.

1. Read every `proposals-*.jsonl`. **Drop** a proposal that:
   - cites no row;
   - cites a row whose status is not `fixed`;
   - has an empty `new`.

   Record each drop in `apply-log.md`.
2. Write the copy as `<source name>.fixed.<ext>` beside the source (or `-2`, `-3`, … if taken), starting from `original.md`.
3. Sort the proposals by `line`, then by position of `old` in the text. Apply each as a literal replacement:
   - **Applied:** `old` occurs exactly once in the current copy → replace it with `new`.
   - **Not found / not unique:** `old` occurs zero times, or more than once → skip, record it, never fuzzy-match.
   - **Overlap:** two proposals overlap → apply the first; record the second as a conflict.
4. Write `changes.diff` (`diff -u original.md <copy>`). Write `apply-log.md` with one line per proposal: applied / skipped (reason) / dropped (reason), plus its rows.
5. If `review-proposals` was given, show the author the proposals (old → new, rows) before applying. Apply only those accepted; record the rest as rejected-by-author.

## Step 6: Check, once

1. **Trace script** (throwaway). For each applied proposal:
   - take the content words (alphabetic, 4 or more letters, lower-cased) in `new` that are not in `old`;
   - flag any of them that appears in neither the cited rows' `wording` and `basis` nor `original.md`.

   Write the flags to `trace.md`. The script reports; it never reverts.
2. **Reviewer.** Launch one fresh subagent:

   ```
   Read <SKILL>/references/reviewer-instructions.md in full and follow it exactly, with ORIGINAL = <RUN>/original.md, COPY = <copy path>, DIFF = <RUN>/changes.diff, TABLE = <RUN>/table.jsonl, TRACE = <RUN>/trace.md, OUT = <RUN>/review.md.
   ```

3. **One repair pass.**
   - Read `review.md`.
   - For each finding marked `must-fix`, edit the copy in this session, minimally. Prefer reverting the proposal over rewording it when the problem is an invented particular.
   - Record each repair in `apply-log.md`.
   - Do not review again, and do not run detection again.
   - Regenerate `changes.diff`.

## Step 7: Record and return

1. **`fix-record.md`.** One row per gap id, with columns:
   - gap id;
   - line;
   - trigger;
   - answer;
   - outcome (fixed-applied / fixed-not-applied / asked / declined);
   - table row;
   - basis, question or decline quote.

   At the top, the counts by outcome and by answer type, and the **resolution rate**: the share of gap ids that ended applied or declined.
2. **Return:**
   - the copy's path;
   - the run folder;
   - the counts (gaps, missing meanings, fixed and applied, asked, declined, skipped at apply, the reviewer's must-fix findings and the repairs);
   - the questions still open (point to `questions.md`);
   - the band and the number of agents launched.

   Add one line: the edits were checked once by an independent reviewer and not re-detected; asked gaps remain open until answered.

## Boundary

- Never edit the source.
- Never write a particular into the copy that the text, the basis files, `context.md` or an author answer does not establish.
- Do not send or publish anything. Do not change this skill's files or the detection run.










