
---
name: non-explicitness-detection
description: Find the places in a document where the wording needs something particular (which one, of what, who, what is done, by what criterion, which system, …) and the text does not single it out, by answering the explicitness question bank sentence by sentence in fresh subagents, one per section. Detection only, no fixing; the result is a numbered gap list in a file, backed by the full row-by-row record.
---

# non-explicitness-detection: explicitness gaps by question bank

This skill finds **explicitness gaps**. A gap is a place where the wording demands something particular and the text does not single it out among the alternatives it puts in play. Two tests decide each case:

- **Demand:** is something particular needed here?
- **Sufficiency:** does the text pick it out, at or before that point (or in the very next sentence)?

The detector judges the text only, never what a reader happens to know. It does not rate or fix anything.

Detection runs in fresh subagents, each answering the bank on one section of the document. Each subagent writes one JSON row per sentence, per questioned phrase and per question. This session then joins the gap answers into one list.

**Invocation:** `/non-explicitness-detection <source> [setting: <what the document is and who it is for>] [runs: 1|2] [model: <name>]`. Every part except the source is optional.

Outside a skill-aware session, for example in Codex: "Read `<this folder>/SKILL.md` in full and execute it on `<source>`."

## Step 1: settle the inputs, in this session

1. **Source.** The document to examine.
   - A file path in the invocation is the source.
   - Inline text is written unchanged to `source.md` in the run folder, and that file is the source.
   - With neither, take the document this conversation is working on and name it before launching. If two documents are equally plausible, ask which one.
2. **Setting.** One sentence on what the document is and who it is for, for example: "an internal project document (a research finding) written for project members."
   - Take it from the invocation or the conversation. Otherwise derive it from the document's own frontmatter or title.
   - The setting counts as text. It is the only context the subagents get besides the document.
3. **Runs.** 1 by default; 2 when asked.
   - Two independent runs find about 20% more distinct gaps in total.
   - Gaps that both runs find are real more often (see "Measured behaviour").
4. **Model.**
   - The model named in the invocation, in the form the environment accepts (a family alias in Claude Code, a model ID in Codex).
   - Otherwise `opus` where available, since the bank was tested on Opus.
   - Otherwise the session's model.
5. **Run folder.** `outputs/explicitness-<YYYY-MM-DD_HHMM>/` beside the source file, or under the current workspace for inline text. Create it; never reuse one.
   - Write `run.md` in it with the source path, setting, runs, model and launch time.
6. **Numbered copy.** Write `document-numbered.md` in the run folder: every line of the source, unchanged, prefixed with its line number (from 1) and a bar, for example `  12| text`.
   - Every row the subagents write cites these physical line numbers.
7. **Sections.** Cut the document into sections of about 800 words, never more than 1,800, and record their line ranges in `run.md`.
   - Cut only at a heading, or at a paragraph boundary when there is no heading nearby.
   - Leave YAML frontmatter out of every section.
   - A document under about 1,000 words is one section.
   - The ranges must cover every non-empty line after the frontmatter exactly once.
   - Smaller sections give more real gaps. One pass reports a roughly fixed amount, so a large section is skimmed.
   - Name the sections `s1-L<first>-<last>`, `s2-…`, and so on.
8. **Reference files**, passed by absolute path. This session does not read them.
   - `references/detection-instructions.md` in this skill's folder: the subagent's procedure.
   - `references/explicitness-bank.md`: the question bank, with its rules, answer values, slots and output rows.

## Step 2: launch the subagents

Launch one fresh subagent per section and run, all at once. Each one does not inherit this conversation (it is not a fork), and each gets this prompt with every placeholder filled in:

```
Read <INSTRUCTIONS> in full and follow it exactly, with BANK = <BANK>, DOC = <RUN>/document-numbered.md, SETTING = "<SETTING>", FIRST = <first line>, LAST = <last line>, NAME = <section name> and OUT = <RUN>/run<k>/<section name>.jsonl.
```

- `<INSTRUCTIONS>` and `<BANK>` are the absolute paths of the two reference files.
- `<k>` is 1, or 1 and 2 when two runs were asked for. Create `run1/` (and `run2/`) first.

**How to launch, by environment:**
- **Claude Code:** the Agent tool, `subagent_type: general-purpose`, with `model` set to the alias.
- **Codex:** `spawn_agent` with `model` set and no `fork_context`.
- **Other environments:** use what the launch mechanism accepts, and report any difference.

**Rules while the subagents run:**
- Do not run the detection in this session, even in part.
- Do not edit the source while they run.
- If this environment cannot launch subagents, return the filled-in prompts for the user to run in fresh sessions.

Each subagent replies with:
- its line count;
- the rows its self-check added;
- its SENT rows;
- its number of gap answers.

Record each reply in `run.md`. A reply that reports no SENT rows, or a file that does not exist, is a failed section: launch that section again once.

## Step 3: build the gap list, in this session

Read the row files; a throwaway script may do this.

**Which rows are gaps.** A gap row is any question row whose `answer` is one of:
- `LATER`: stated only after the next sentence;
- `MULTIPLE`: two or more candidates fit;
- `CONFLICT`: two places disagree;
- `CANNOT`: not singled out at all;
- `UNSPECIFIC`: an earlier mention is fuller than the wording here.

Skip `SENT` and `PHRASE` rows, and rows answered `QUOTE` or `NOT-DEMANDED`.

**Write `<RUN>/gaps.md`.**

1. **Header:**
   - the source path;
   - the setting;
   - the model;
   - the date;
   - the number of runs;
   - per section: its line range and gap count.
2. **One numbered item per gap, in line order:**
   ```
   N. L<line> — "<trigger>" — <slot or qid>: <ANSWER> — <note> [quote: <quote>]
   ```
   - A row with a `"via"` field is not a new gap. List it as a sub-bullet under the gap of its root trigger.
   - Mark `UNSPECIFIC` items "(earlier mention is fuller)".
3. **With two runs**, give one item per distinct gap.
   - Two rows are the same gap when they are on the same line (or the same phrase) and name the same missing meaning, whatever the wording.
   - Mark each item "both runs" or "run 1 only" / "run 2 only".
   - Put the both-runs count and the one-run count in the header.

The row files stay in `run1/` and `run2/`. They are the full record: every question asked and how it was decided, including what was found supplied (`QUOTE`) or not needed (`NOT-DEMANDED`, with its exemption).

## Step 4: return

Return:
- the path of `gaps.md`;
- the model requested and the model applied;
- the number of sections and runs;
- the number of gaps (with two runs, also how many both runs found).

Do not paste the list unless asked; the file is the result.

Add one line saying three things: this is detection only; each item is a place where the text does not single out something its wording needs; and the items are not verified.

## Boundary

- This session reads only what Step 1 needs: the source to number and section it, then the row files in Step 3.
- The skill does not rate, fix, send or publish anything, and does not change its reference files.

## Measured behaviour

The bank in `references/explicitness-bank.md` is version 6.7.2: version 6.7.1 plus one rule, V6.7.2-A (see "Version 6.7.2" at the end of this section). Version 6.7.1 was tested on 5 October 2026, with fresh Opus 5.5 subagents and two independent runs on each text. Two texts were used:
- **Benchmark A:** 42 short technical excerpts, run in sections of 7 excerpts (400–770 words).
- **Benchmark B:** a 5,000-word research finding, run in 4 sections (690–1,800 words).

**Precision on benchmark A.** A blind editor judged every gap, without knowing which detector produced it:
- 79–82% of the bank's gaps were real (169–173 real per run, 35–43 false);
- for comparison, a plain one-prompt detector on the same text had 65% real (155 real, 83 false).

**Stability.** Gaps found by both runs were real 85% of the time. About two in three distinct gaps were found by both runs.

**Recall against the authors' 70 issues (benchmark A):**
- 40–45 per run fully found;
- 45–47 across both runs.

**Recall against the 46-row reference (benchmark B):**
- 36–39 rows per run (78–85%);
- 39–41 across both runs.
- 27–38% of the reported items there matched a reference row.

**Known weak spots:**
- **Exemptions.** Three gates sometimes exempt real gaps: V6.7-A1 ("one end state"), V6.7-A3 ("the point is about the whole") and V6.7-A8 (possessive, doer).
- **Consistency between distant places** (a figure or claim checked against another place far away) is mostly not detected; it needs a whole-document check, which this skill does not do.

**Cost.** Each section's subagent took 3–14 minutes and roughly 90–175k tokens.

**Trial of this skill as packaged (5 October 2026).** The skill was run twice on each of two benchmark files, giving 16 sections.

- **Benchmark A, given as one 3,600-word file of 42 independent excerpts.** The setting sentence stated that the excerpts are independent, and the file was cut into 4 sections of 850–990 words.
  - Per run: 177–181 real gaps, 79–81% real.
  - Authors' issues fully found: 45–48 per run, 51 across both runs.
  - Gaps found by both runs were 86% real.
  - This is equal to or slightly better than the unpackaged bank, judged by the same blind editors.
- **Benchmark C, 30 short trip messages with 56 planted gaps.**
  - 49–50 planted gaps found per run.
  - 78–79% of the reported gaps were real.
  - 4 false alarms per run in the 8 paragraphs that hold no planted gap. These are mostly "two readings fit" calls; some are arguably real.
- **Self-checked sentence coverage.** Every section's coverage was complete. One agent's self-check added 5 missing sentence rows.

**Version 6.7.2 (7 October 2026).** Rule V6.7.2-A: a non-ordinary term whose head is an action or relational noun ("the first 42 full readings") also gets an "of what?" question; a comparison partner does not supply it.
- **Test setup:** the packaged procedure, two runs on each of the same two benchmark files, judged in one fresh blind editor pool together with version 6.7.1. This pool was stricter than the earlier one, so its percentages are lower for both versions.
- **Benchmark A:**
  - 169 and 163 real gaps per run, against 156 and 156 for version 6.7.1;
  - the same precision (70% against 68–72%);
  - authors' issues fully found: 55 across both runs, against 51.
  - **The rule's own gaps:** 10 distinct gaps, all judged real.
- **Benchmark C:** 48 planted gaps found per run (against 49–50), with 82–83% real (against 78–79%); this is within run-to-run variation.

**Operational note.** Each subagent writes throwaway helper scripts. When launching several at once, tell each to use its own scratch folder, because two agents sharing one ran each other's script in testing.

