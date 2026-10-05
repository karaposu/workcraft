# Non-ambiguity detector

## What detection is

Detection finds the places in a communication where the intended recipient cannot establish a meaning they need, and records where each one is and what is missing. It does not explain, rate, fix or rewrite; it locates and names. Detection is multi-dimensional: one sentence can fail the recipient in several independent ways at once, and each way is a separate finding. A match under one pattern never closes a sentence to matches under other patterns, or to a second match under the same pattern on a different expression. Accuracy means recording every match the text and the recipient's context support, and nothing they do not.

## Required reading

Read `non-ambiguity-patterns.md` in full before examining anything, every time this detector runs. It holds the patterns used for matching, the conditions under which each one is and is not a problem, the patterns each is confused with, and the rules for reading from the recipient's position. Read every pattern block, including its “Not a problem when” and “Distinguish from” lines, and complete any truncated read. Do not summarise, restate or replace the patterns, generate a dynamic prompt, or invoke another critique or revision skill. If the patterns file is unavailable, stop and say so; do not detect from memory.

## Expected yield, estimated before the local review

Before reading the patterns in detail and before examining any chunk, estimate how many supported findings a complete reading of this target should contain. Do not detect anything in this step.

1. Count the target's words as whitespace-delimited units, including headings, bullets and table text, and its physical lines.
2. Describe the kind of text from its structure only: genre, length, how many actors or roles it addresses, whether it instructs, whether it refers to things outside itself, how many delivery surfaces it has. These make ambiguity more or less likely in general; they are not findings.
3. Apply the measured density: on one facilitator script of about 4,500 words, several independent readings together found about 10 to 14 supported findings per 1,000 words, measured on 2026-09-30. If this target differs materially from that kind of text, say how and whether you adjust; never adjust silently.
4. Judge the zero case: say whether a near-empty result is plausible here (very short, single-actor, non-instructional or self-contained texts can legitimately contain no supported ambiguity). If so, the range starts at zero and the high end is a ceiling, not a target.
5. Note the result in `run-record.md` as one block: word count, kind, expected low and high, basis with provenance, zero-case judgment. No separate file.

Treat the range as the order of magnitude a complete reading of this target reaches; it overrides the line below that there is no target count. The estimate changes nothing about what counts as a finding: every finding still needs its evidence line, a finding you cannot evidence is not a finding, and when the text supports fewer findings than the range, fewer is the right answer. Do not revise the estimate during the review.

## Inputs and restrictions

Use only the unchanged target, the governing request, the author brief if one is supplied, the patterns file, this detector, a chunk table if the caller supplies one, and the artifacts this run produces. A brief establishes the target's purpose and delivery format; it is not a new creation task. Do not retrieve other chats, earlier reviews, revised versions of the target, external systems or embedded links. Examples in the patterns file illustrate judgments; they establish no facts about the target.

## Prepare

Create a fresh directory under `outputs/`, or use the one the caller supplies. Copy the target, request, brief, patterns file and this detector into `sources/` unchanged and work from those copies.

Report one-based physical line numbers from the unchanged target, counting blank lines. Never use display wrapping or generated numbering as source text.

Keep a compact `run-record.md`: input paths, the chunk table, chunks completed, and whether the whole-document check is complete. It records progress, not assessment.

## Review sequentially

Perform one full local review in source order, then one whole-document connection check. **Do not use subagents or delegate to other sessions.** Process each chunk yourself and finish it before starting the next. Thoroughness matters more than speed.

If the caller supplies a chunk table, use it. Otherwise partition the target so that every word has exactly one primary chunk: chunks of about 300 words, never more than 420 and never fewer than 150 except the last, cut at the paragraph, list-item, table-row or heading ending nearest the 300-word mark. Give each chunk the 200 words before it and the 100 words after it as context. Count words as whitespace-delimited units, including headings, bullets and table text. Write the table into `run-record.md` so later runs can reuse it.

If a cut splits a sentence or paragraph, read the whole unit. Keep the headings, table headers, brief and full target available. Chunk boundaries are not defects.

## Examine each chunk

For each paragraph in the chunk's primary range, establish what it needs to convey and what the intended recipient knows at that point. Where the target has several delivery surfaces, distinguish what participants hear or see from facilitator-only instructions.

Then take every sentence in order, including headings, bullets, labels and table entries, and go down the pattern index in order, P01 to P32. For each pattern that could apply, ask its question. Record a match when the recipient cannot establish the meaning from the text and their legitimate context, and the pattern's “Not a problem when” line does not apply; you will have to quote the words that meet the “Problem when” clause and say why the limit fails, so check both before recording. Continue through the remaining patterns before moving to the next sentence.

Matches are independent:

- Several patterns on one sentence are several findings. List all of them.
- The same pattern on two expressions in one sentence is two findings.
- A different pattern on the same expression is a separate finding when it names a different missing meaning.
- Drop a match only when the pattern's “Distinguish from” line sends that same missing meaning to another pattern; record it there, once.
- One missing meaning that recurs across many passages because the document never supplies it is one finding with many locations, not one finding per passage. Record it once, at the first passage that depends on it, and add the other locations to that row as you meet them.
- Do not stop because the passage already has findings or because the table is long. There is no target count and no minimum severity.
- When you suspect a gap but cannot produce both evidence parts for it, record it in `candidates.md` (see Save detections only) and move on. Do not stretch the evidence to turn a suspicion into a finding, and do not drop the suspicion; the candidates file is where it belongs.

After each paragraph, apply the connection patterns, P27 to P32, to how its sentences fit together. After each chunk, write one line per paragraph in `examination-log.md`: what it needs to convey, and the pattern IDs considered and matched. That log is the only place the examination is visible; keep it terse and do not put detections in it.

After all chunks, perform the whole-document check: apply the connection patterns, P27 to P32, across sections and delivery surfaces, including meaning the account needs that no sentence states, and resolve anything a chunk deferred.

## Record as you go

Append rows to `ambiguity-detections.md` after each chunk. Never rewrite existing rows except to correct a quotation or line number against the source. After each chunk, verify the new rows' quotations and line numbers. At the end, sort the table by source location and merge only exact duplicates: the same location and the same missing meaning reached twice through overlapping context or the whole-document check, or the same document-level missing meaning recorded at several locations, which becomes one row listing all of them.

## Second and later passes

The caller states the pass number and, above pass 1, the mode. Without a pass number, this is pass 1 and this section does not apply.

- **Independent** (default): do not open any earlier report. Run exactly as pass 1 into a new detections file. The caller merges passes by missing meaning, not by line and category.
- **Extension:** read the earlier pass's `ambiguity-detections.md` in full first. Examine the entire target again against every pattern. A flagged sentence is not finished: check it against every pattern not yet matched there, and for further expressions under the patterns already matched. Give unflagged passages the same care. Append new rows and new matches, each labelled `(pass N)`. Do not remove or reword earlier rows. If an earlier match looks wrong, note it with its reason in `run-record.md` and leave the row in place.

## Save detections only

`ambiguity-detections.md` contains only this table:

| Source line(s) | Exact affected text | Pattern match(es) |
|---|---|---|

- One row per affected sentence or short passage. Keep separate locations in separate rows, with one exception: a missing meaning that the document never supplies and that many passages depend on gets one row listing every affected location and quoting the first, so a document-level gap does not multiply by the number of sentences it touches. Separate rows remain right when the missing meanings differ from passage to passage, even under the same pattern.
- The match cell lists every finding for that passage as four lines. The first line is the finding: pattern ID, a short statement of the missing meaning, and the category tag, as in `P20 — condition for escalation unstated: “if still failing” [N4]`. The second line is its evidence, beginning `evidence:`, with two parts separated by ` | `: `meets: “<the exact words from the passage that satisfy the pattern's “Problem when” clause>”` and `limit: <one clause saying which “Not a problem when” condition was considered and why it does not hold here>`. In an extension pass, add `(pass N)` to the first line.
- The third line is the sentence kind, beginning `kind:`, with one of two values and one clause: `instruction` when the affected sentence tells its reader to do or not do something, or states a rule the reader must follow; `statement` when it describes, explains or names. The clause names who is told to do what, or says that the sentence describes. The kind must be checkable against the quoted words. The fourth line is `rating:`, transcribed, not judged: look up the pattern's group (action or meaning) in the patterns file and read the cell for that group and this kind from the Consequence groups table there; write that value and nothing else. Do not rate consequence, severity or importance by any other route.
- A finding without both evidence parts is not a finding. If you cannot quote words that satisfy the “Problem when” clause, or cannot say why the “Not a problem when” clause fails, do not record the row; record the suspicion in `candidates.md` instead. The evidence is a test the finding must pass, not a description of it: when the limit clause holds, the honest result is no row, not a row with a weak reason.
- Quote the affected wording exactly. For a finding across passages, include each line range and each quotation. For an omission, anchor the row to the passage that needs the missing meaning; never invent text to quote.
- No explanations, consequences, severity, mitigations, proposed wording or clean-passage assessments. If nothing is found, leave the table body empty and say so in `run-record.md`.

`candidates.md` is a second file with this table and no other content:

| Source line(s) | Exact affected text | Suspected missing meaning |
|---|---|---|

One row per suspicion that failed the evidence test: the location, the exact words, and the missing meaning in a few words, with no pattern ID, no evidence line and no rating. Candidates are not findings and are not counted as findings. Append to it as you go, the same way as the detections table. If there are none, leave its table body empty.

Do not revise the target or the patterns file. If context is lost, reload this detector, the patterns file, the sources, `run-record.md` and `examination-log.md`, then resume at the first unfinished chunk. If a required input is missing, name it rather than presenting an incomplete review as complete.

Finish by stating the full paths of `ambiguity-detections.md`, `candidates.md`, `examination-log.md`, `run-record.md` and the run directory, the expected yield you estimated, the number of findings by rating and the number of candidates, the pass number and mode, and whether the local review and the whole-document check were completed.





----

