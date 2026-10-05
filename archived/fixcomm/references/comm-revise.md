
# comm-revise — Communication Revision

Read this protocol in full before executing it. Run its steps in order: **read the basis and guides → assess proposals → revise → inspect the result → return**. Complete each step before dependent work begins.

Use the current draft, its governing request, supporting context and `ComCritic.md` to produce a coherent revised communication. Preserve the author's intended meaning and **intended openness** while applying supported corrections.

## Invocation and inputs

fixcomm, or another caller, invokes this protocol after a usable communication critique exists. The draft may still contain the problems to be corrected.

The caller must identify:

- **Target:** the current draft or named set of drafts, supplied as text or accessible files, and the version reviewed.
- **Task:** the request the communication serves, author, recipient, purpose, medium, current corrections and exclusions, and what should remain open.
- **Critique:** the applicable `ComCritic.md`; provide `dynamic_comm_critic_prompt.md` when needed to recover the review's framing.
- **Supporting basis:** relevant source contents or recoverable locations, and any additional or explicitly substituted guidance.
- **Output instructions, if specified:** destination, format, edit mode and any remedy choices already made by the author.

These inputs can come from the active exchange and files; a separate context document is not required. Resolve supplied locations to concrete paths. Do not infer target identity from a filename alone.

The caller coordinates source acquisition, task clarification and any renewed critique. This protocol makes editorial choices within that task and identifies specific needs it cannot resolve.

## Step 1 — Read the basis and guides

Read the current target, governing request and `ComCritic.md` in full. Read supporting material needed to establish the meaning of proposed changes. Previously surfaced source contents are usable while they remain available in active context; after context loss, recover the contents rather than relying on a source list or remembered summary.

**At the start of every invocation, read all five guides below in full before assessing proposals.** Complete truncated reads. Resolve the default paths relative to this protocol file; a caller may supply their actual locations when packaged elsewhere.

| Guide | What it governs |
|---|---|
| [Non-ambiguity](comm-critic-d/references/non-ambiguity.md) | Referents, relationships, prerequisite context and connected sections. |
| [Meaning and fidelity](comm-critic-d/references/meaning-and-fidelity.md) | Required answers, supported claims, actual status, intended openness and retained corrections. |
| [Recipient and purpose](comm-critic-d/references/recipient-and-purpose.md) | The intended aspect, useful detail, presentation, voice and supporting references. |
| [Operational communication](comm-critic-d/references/operational-communication.md) | Progress briefings, decision requests and coordination messages. |
| [Author preferences](comm-critic-d/references/author-preferences.md) | Communication in the author's name, within each item's stated conditions. |

Use these shared checks to judge revisions; this protocol governs the revision operation. Their links to the critic entrypoint do not instruct you to run another critique.

Read additional applicable task-supplied guides in full. Use a replacement guide set only when explicitly instructed. Reading a guide does not make every item applicable. Preserve all four fields of each check in your judgment, including its conditions and limits.

Current explicit instructions govern the task. Apply personal and organisational guidance only within its scope. Do not turn a personal preference into a general policy or use recency alone to settle conflicting sources.

If applicable guides conflict and the task does not resolve the conflict, identify the competing requirements and return the affected choice to the caller. Do not silently impose the stricter rule; continue corrections independent of that choice.

Establish what the recipient needs now, what context the exchange actually supplies, and which meanings must remain provisional. Distinguish authoring instructions and private source material from what the recipient should receive.

Compare the current task and target with the report's reviewed version and assumptions. Reassess findings affected by changes to facts, audience or purpose; retain findings whose basis still holds.

If the target, request, critique or required guide cannot be identified or read, return the specific missing basis before revising. If only a particular correction depends on an unavailable fact, source or decision, continue with independent supported work and carry that unresolved need to the return step. Never reconstruct missing substance from a plausible guess.

## Step 2 — Assess findings and proposed remedies

Consider every finding in `ComCritic.md`, including omissions. Combine overlapping concerns and distinguish alternative remedies from changes intended to work together.

For each concern, determine:

- Does the defect still exist in this communication, judged against the actual request and reader's needs?
- Is the proposed meaning supported by the available evidence and current instructions?
- Is making that change within the task's delegated authority?
- Does the remedy preserve necessary meaning, previous corrections and intended openness, including when combined with other remedies?

Use severity to direct attention, not to grant authority or require a new approval. Quick, robust and long-term mitigations are options; they are not all mandatory actions.

Choose, adapt or replace a remedy when justified. A valid defect can have a poor remedy: rejecting the remedy must not silently discard the concern. Reject unsupported findings on their grounds; do not manufacture a change to satisfy the report. If no supported repair is available for a required meaning, retain the specific unresolved need.

Choose between faithful wording or structural alternatives using the requested voice, purpose and medium. Return a substantive choice that the task has not delegated. A requested recommendation may be developed when supported; an exploration meant to leave the choice open must remain open.

This assessment does not require a per-finding ledger or another diagnostic report.

## Step 3 — Integrate the corrections

Revise the nominated communication using the original content, current task basis and supported remedies together.

Preserve necessary information that the critique did not mention. Retain warranted qualifications, attribution, status, relationships, author preferences and applicable removals. Preserve current authorised meaning rather than obsolete wording.

Use local edits when sufficient. Restructure when organisation itself prevents understanding. The extent of an edit does not determine its authority: consider what the change makes the author say.

**Preserve intended openness explicitly throughout revision.** Clarify what an unresolved choice or emerging concept refers to without forcing a final decision, definition or precision. Do not remove uncertainty labels that carry necessary meaning or add them mechanically to every sentence.

Place the explanation the recipient needs in the actual delivery. Use legitimate shared context; do not force every thread reply to stand alone. Keep private authoring instructions and editorial discussion out of the recipient-facing text.

Correct clearly supported incidental defects within the same communication task, including problems introduced by combining edits. Return needs requiring new facts, authority or underlying operational work to the caller.

For long communications, work through coherent sections with the context needed to interpret them. Keep connected claims and qualifications together, then integrate the whole.

## Step 4 — Inspect the actual result

Produce the revision in the requested form and location. Follow the caller's edit mode. If none is specified, return inline revisions for inline drafts; for file drafts, create a distinct revised copy beside the target, retain its format and use an available filename. Do not overwrite an unrelated existing output. If no change is warranted, return the existing communication without creating a needless duplicate.

Read the actual produced text; for saved output, read the saved version back. Check:

- The applicable defects were addressed, or their consequential unresolved requirements are identified.
- The communication supplies the meaning the request requires now, including answers absent from the original draft.
- Necessary content, qualifications, previous corrections, voice and intended openness survived.
- Combined edits did not introduce unsupported claims, contradictory status, broken referents or disconnected reasoning.
- Required context and usable references are present where the recipient will receive them.
- The result fits the requested medium and contains no accidental editorial instructions or private review notes.

Repair supported problems found in this readback and inspect the affected text and its connections again. If repair requires missing substance or a changed task basis, return that specific need. Do not automatically repeat the entire critique workflow or use zero findings as a completion rule.

If the required output cannot be produced or inspected, state the specific limitation and identify any usable partial result; do not claim that the requested artifact was completed.

## Step 5 — Return to the caller

Return the complete revised communication, or a link to the saved result, in its intended form. Identify an intentionally unchanged result when applicable.

Keep any editorial note separate and proportionate. Explain consequential departures from proposed remedies when the caller needs the reason to understand the result. Report unresolved required meaning with the affected passage or requirement, the missing fact, source or decision, and why it prevents completion.

When essential meaning remains unresolved, identify the result as partial to the caller. Do not describe a polished partial draft as a completed answer. A private note does not substitute for required meaning in the recipient's communication.

Finish after the result has been inspected and returned with any consequential unmet needs. This establishes what was revised and checked, not a guarantee that every possible defect has been detected.

## Boundary

Revise only the nominated communication. Keep `ComCritic.md`, its generated prompt, source evidence and principle files unchanged. Do not send or publish the result, perform the underlying operational task, archive review artifacts, or mark the parent workflow complete. Those actions remain with the caller under the user's instructions.

