
---
name: comm-fix-ambiguity
description: Detect ambiguity in an outgoing message, document or presentation with the non-ambiguity detector, then apply the supported wording fixes in the same session and return the revised text with a record of every edit and every deferred question. Detection only when requested.
---

# comm-fix-ambiguity — Ambiguity detection and repair

A workflow for finding the places where the intended recipient cannot establish a meaning they need, and supplying that meaning where the material supports it.

Routes:

- **Fix (default):** prepare → detect → fix → return.
- **Detection only:** prepare → detect → return detections. Finish there.

Invocation outside a skill-aware session: "Read `<this folder>/SKILL.md` in full and execute it on `<target>` with `<request or brief>`."

## Mandatory execution discipline

1. Read this file in full. Then read `references/non-ambiguity-detector.md` and `references/non-ambiguity-patterns.md` in full, every run; the detector requires both and forbids detecting from memory. Complete truncated reads. Summaries and remembered contents do not count.
2. Run every step in this session, in order, without subagents or parallel delegation. Finish and check each step's output before the next begins.
3. Do not invoke another critique or revision skill, generate a dynamic prompt, or retrieve material the steps below do not name.
4. Never invent meaning. Where the material does not establish a missing meaning, the finding is returned to the author as a question, not filled with a plausible guess.

## Step 1 — Prepare

Establish from the request and the supplied files:

- **Target:** the text to be reviewed (a file or inline text) and the version. An outgoing draft shown to the operator keeps its outgoing recipient.
- **Request and author brief:** the governing request, and the author brief if one exists. They establish the text's purpose, recipient and delivery format. The detector reads them; the fix step also uses them as a source of meaning.
- **Permitted context:** any other material the caller supplies that the fixes may draw meaning from (earlier messages, source documents). Nothing else is read. The detector does not use it; only the fix step does.
- **Mode and options:** fix (default) or detection only; pass count (one by default; two adds an extension pass); edit mode (inline result for inline text, a revised copy beside the target for a file; the target is edited in place only when the caller asks); output directory if the caller names one.

Create the run directory: the one supplied, or a fresh folder under `outputs/` beside the target (in the current workspace for inline text). Do not reuse another run's folder. The detector's `run-record.md` in that directory is the run record for the whole workflow: the detector writes its blocks; Step 3 appends its own. Record the mode, options, paths and last completed step there.

## Step 2 — Detect

Execute `references/non-ambiguity-detector.md` exactly, with the run directory, as pass 1 in independent mode. The detector's inputs are only the unchanged target, the request, the brief, the patterns file and the artifacts it produces; it does not read the permitted context.

Check its finish statement before continuing: the full paths of `ambiguity-detections.md`, `candidates.md`, `examination-log.md` and `run-record.md`; the expected yield it estimated; the number of findings by rating and the number of candidates; whether the local review and the whole-document check were completed. An incomplete review is not a result; finish it before Step 3.

When the pass count is two, run the detector again, in this session, in extension mode on the unchanged target, with pass 1's `ambiguity-detections.md` as the earlier report, and check its finish statement in the same way. Do not revise the target between passes.

In detection-only mode, return the detections, the candidates, the examination log, the run record and the run directory, and finish here.

## Step 3 — Fix

Inputs: the unchanged target, the request and brief, the permitted context, `ambiguity-detections.md` and `candidates.md`.

Work through the detections table in source order. Every row gets exactly one outcome: **fixed**, **deferred** or **declined**. Use the rating to order attention (vital first); it never grants or withholds a fix.

**The basis rule.** An edit may make explicit, move or connect a meaning that the target itself, the request, the brief or the permitted context already establishes. It may not add a referent, actor, target, extent, condition, criterion, number, name or fact that none of them establishes. A finding whose missing meaning has no basis is **deferred**: recorded with the missing meaning as a one-line question for the author. The author's answer, if it arrives in this session, is a basis.

**The edit.** Make the smallest change that supplies the meaning: name the referent; state the actor; state the target or extent; state the condition or threshold; give the criterion; place the explanation before the point that depends on it; state the connection between parts. Prefer a local wording change. Reorder passages only where a connection pattern (P27 to P32) names the order itself as the gap. A document-level gap recorded once with many locations is fixed where the document should first introduce the meaning; later passages are touched only if they then read wrongly.

**What every edit preserves.** The author's facts, voice and commitments; existing corrections; the delivery surfaces (what participants hear or see against facilitator-only instructions); and intended openness, as the patterns file's section "When ambiguity is acceptable or necessary" describes it: make clear what is unresolved without resolving it, and do not add precision the author did not mean.

**Declining.** Decline a row only when, read against the brief or the permitted context, the pattern's "Not a problem when" clause actually holds; record the reason. Do not decline a row because the fix is inconvenient.

**Candidates.** Rows in `candidates.md` are suspicions without evidence. Do not act on them; they are returned to the author unchanged.

**The record.** Keep `fix-record.md` in the run directory with this table and no other content:

| Source line(s) | Finding | Outcome | Replaced text | New text | Basis or question |
|---|---|---|---|---|---|

One row per finding, in table order; a finding across passages lists each location. For a fixed row, quote the replaced words and the new words exactly and name the basis (the target line that establishes the meaning, the brief, or the context file). For a deferred row, give the question. For a declined row, give the reason. An edit the table did not call for, made to repair a defect that combining edits introduced, gets its own row with "incidental" in the Finding column. Append rows as you go; after each section of the target, verify the rows against the produced text. Every row in `ambiguity-detections.md` must appear here with an outcome before Step 4.

**Produce the revision** in the requested form and location: an inline result for inline text; for a file, a revised copy beside the target with the same format and an available name. Do not overwrite the target unless asked. If every row is deferred or declined, return the existing text unchanged and say so.

**Readback.** Read the produced text once (the saved copy, for a file). Check that each fixed row's new text is present at its location, that no editorial note, marker or question for the author has leaked into recipient-facing text, and that the format fits the medium. Repair those problems only. Do not re-run detection and do not re-detect the edits; the text is ready as fixed. If the caller wants an independent check of the result, that is a separate run of this skill in detection-only mode on the revised text.

Append a block to `run-record.md`: rows fixed, deferred, declined; the revision's location; readback done.

## Step 4 — Return

Return prominently: the revised text or its path. Then:

- counts: findings by rating; fixed, deferred, declined;
- the deferred questions, as the author's list, each with its location;
- the paths of `ambiguity-detections.md`, `candidates.md`, `fix-record.md`, `examination-log.md`, `run-record.md` and the run directory;
- the detector's finish statement (expected yield, pass and mode, completion);
- one line stating that detection ran on the original text and the fixes themselves were not re-detected.

Do not claim that every ambiguity was found or that the fixes introduced none.

## Resume an interrupted run

Read this file, the detector and the patterns file in full, then `run-record.md`. Recover the sources from the run directory's `sources/`. If detection is unfinished, resume by the detector's own rule (reload its inputs, `run-record.md` and `examination-log.md`, continue at the first unfinished chunk). If the fix step is unfinished, continue at the first row of `ambiguity-detections.md` without an outcome in `fix-record.md`, after reading the revision produced so far. If the target or request changed, preserve the old run and start a fresh one.

## Boundary

Work on the nominated text only. Do not send or publish it, contact anyone, perform the task the text describes, or change the detector or the patterns file. Detection locates and names; the fix step supplies meaning the material establishes and returns the rest to the author.




