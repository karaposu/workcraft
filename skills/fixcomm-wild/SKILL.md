
---
name: fixcomm-wild
description: Improve an existing outgoing message, document or presentation using coordinated context discovery across sources, then full comm-critic-d and comm-revise. Use when relevant context may be scattered or unlinked; unplugged surfacing coordinates repeated full Surfacing invocations and optional parallel workers before critique and supported revision.
---

# fixcomm-wild — Communication Revision with Context Discovery

A thinking discipline for turning an existing draft into a faithful, understandable communication for its intended recipient and purpose.

Run **prepare → unplugged surfacing → comm-critic-d → comm-revise → return**. Unplugged surfacing coordinates full ordinary Surfacing invocations and integrates their evidence. Preserve the governing request, supported meaning, applicable corrections and **intended openness**: choices, concepts or uncertainty that the communication is deliberately meant to leave unresolved.

## Mandatory execution discipline

Read this entrance in full before starting. For every component invocation:

1. **Load its actual instructions and mandatory references in full into active context.** Filenames, headings, selected excerpts, summaries and remembered contents do not satisfy this requirement. Complete truncated reads. Never shorten a required read to save time or context.
2. **Execute the full component in order.** Do not substitute the descriptions below for its instructions. Do not draft, precompute or run a dependent stage in parallel with the work it depends on.
3. **Consume and check the actual output before the handoff.** Check its correspondence to the current target, request and evidence; file existence alone is insufficient. Complete the component's own output checks and correct defects before dependent work proceeds.
4. **Record the completed handoff and continue immediately to the next ready stage.** A component's return hands control back to fixcomm-wild. Do not end the workflow or ask whether to continue merely because context recovery or the critic finished.

Independent retrieval assignments may run concurrently under unplugged surfacing's coordination. Dependent critique and revision wait for an identified, checked context handoff. Workers do not change the context account used by an ongoing review.

The critic and revision protocol each require all five communication guides to be read in full at every invocation. Preserve their rules for additional or explicitly substituted guidance. Reading is mandatory; application remains scoped to the task, author and communication.

Keep necessary source contents available through the handoffs. After context loss, recover required instructions and relevant source contents before using them; a saved source list cannot replace the evidence.

When a prerequisite cannot be satisfied, use **Handle returned needs** below. Continue work that remains independently supported; never invent missing inputs to keep the sequence moving.

## Step 0 — Resolve the operating dependencies

Use the components below from the Workcraft bundle. Install the skill folders together as siblings; each workflow calls the shared dependencies at their resolved locations.

| Dependency | How to locate it | Required use |
|---|---|---|
| [Unplugged surfacing](../unplugged-surfacing/SKILL.md) | The shared Unplugged Surfacing skill | Execute its inquiry formation, full Surfacing calls, evidence integration and bounded return |
| [Ordinary Surfacing](../surfacing/SKILL.md) | The shared Surfacing skill and its `references/surfacing.md` | Unplugged surfacing invokes it; the executor reads its full entrypoint and operating reference every time |
| [comm-critic-d](../comm-critic-d/SKILL.md) | The shared outgoing critic and its five files under `references/` | Run reference reading, prompt generation/checking and critique execution/checking |
| [comm-revise](../fixcomm/references/comm-revise.md) | The shared outgoing revision protocol under Fixcomm | Read and execute it in full, using the actual guide locations resolved from the critic |

Resolve relative references from the file declaring them. Use the resolved components from this bundle unless the user explicitly requests a replacement. Retain concrete locations for the selected components and their required references; use a consistent set throughout the run. Invoke a component by reading its entrypoint and executing its full instructions with the available tools.

The critic and revision protocol share the guides in `../comm-critic-d/references/`. Supply their actual locations if an explicitly requested replacement changes that arrangement. Generated critique prompts must carry locations usable in their execution environment.

If a required component or reference cannot be located or read, identify the exact missing dependency and stop its dependent work. Do not replace it with generic writing advice. Source-system access is a separate task constraint; available operating instructions do not establish access to company evidence.

## Step 1 — Prepare the task and review workspace

Read the nominated draft and governing request in full. Establish from available material:

- The target text or named set of drafts, and the version being reviewed.
- The current request, known author, intended recipient, purpose and medium.
- Applicable corrections, exclusions, guidance and what should remain open.
- Known supporting sources, the draft's origin and relevant exchange, and actual source restrictions.
- Requested output location, format and edit mode.

Use the active exchange and supplied files. A current editing brief may be sufficient without a historical original brief. Keep unsupported details unresolved. Recover missing task context where possible; ask only for a distinction that is needed to identify the target or proceed faithfully.

An outgoing draft shown to the operator retains its outgoing recipient. Distinguish private authoring context from what that recipient will receive.

Use the requested review directory; otherwise create a fresh review directory beside the target file, or in the current workspace for inline text. Pass this directory to the components so their artifacts stay together. Do not overwrite another run's artifacts.

Maintain one compact `_fixcomm-wild.md` in that directory with:

- Current task/target basis and recoverable locations.
- Actual component and output locations.
- The location and current handoff identifier of the discovery account; keep assignment details in that account.
- Last completed and checked operation.
- Next operation or specific unmet need.
- Governing decisions or changes not recoverable from those artifacts.

Create it when the run starts; update it after checked handoffs and before returning an unresolved need or final result. Refer to existing substantive artifacts instead of copying their contents. Keep current state, without a narrative history or per-finding ledger.

## Step 2 — Discover and integrate the relevant context

Load and execute [unplugged surfacing](../unplugged-surfacing/SKILL.md) in full. Execute the coordinator in the current context by default; it may dispatch independent retrieval assignments through the available worker tools.

Give it this purpose: **recover existing material needed to assess this communication against its task, including required meaning absent from the draft.**

Direct relevance toward:

- The request and relevant exchange.
- Material supporting, challenging or qualifying claims and required answers.
- Applicable corrections, preferences and constraints, with their scope.
- Evidence of context available to the intended recipient.
- Instructions or exchanges indicating intended openness.

These concerns can overlap in one source; they are not quotas of searches or answers. Preserve explicit openness instructions and leave unsupported judgments about intent unresolved.

Supply the current task and draft, their origin and relevant exchange, starting source locations, the known work environment and source-system guidance, actual restrictions, and any work allowance. Use a `discovery/` subdirectory of the review directory for its outputs. On a renewed invocation, also supply the existing discovery account and the specific new or changed question.

Require both independently seeded source inquiries and pursuit of meaningful discovered links under the coordinator's rules. The coordinator makes the full ordinary Surfacing invocations, preserves their separate traces and returns `discovery/context.md` with usable integrated evidence, actual coverage and unfinished needs. A worker's trace or completion message alone is not the supporting context.

Read the returned account and necessary source contents. Check task correspondence, supported relationships, qualifications, actual search scope and consequential gaps. Confirm that owned worker activity has been accounted for and that late outputs cannot silently alter the issued account. Record its handoff identifier in `_fixcomm-wild.md` before starting dependent critique.

Handle consequential gaps through **Handle returned needs**. A bounded context handoff can support a provisional communication; it does not establish that every relevant source was found or supply an essential answer that remains unavailable.

## Step 3 — Run the full communication critique

Load and execute [comm-critic-d](../comm-critic-d/SKILL.md) with:

- The actual current target and governing request.
- Known author, recipient, purpose, medium, corrections and intended openness.
- Usable supporting material, source locations and actual limitations.
- Applicable task-supplied guidance and the concrete review output directory.

Use the identified discovery handoff. Keep its supporting contents usable while generating and executing the prompt; recover them after context loss. An acquisition status label does not replace evidence.

Complete its mandatory guide reads, then generate, save and check `dynamic_comm_critic_prompt.md`. Only then execute that saved prompt and produce, save and check `ComCritic.md`. Keep the dynamic prompt's explicit protection of intended openness.

Consume both checked artifacts and verify that they concern this task and target. The critic's findings and mitigations remain proposals. A no-findings report is valid and still proceeds to revision's actual-text inspection.

If review preparation or execution returns a missing prerequisite, handle it below before continuing affected work. Do not treat a partial or unavailable report as a completed critique.

## Step 4 — Apply supported corrections

Read and execute [comm-revise](../fixcomm/references/comm-revise.md) in full. Supply the current target, governing task, applicable `ComCritic.md`, supporting source contents or recoverable locations, actual guide paths and output instructions. Include the dynamic prompt when needed to recover the review's framing.

The protocol must perform its own mandatory guide reads, assess every finding, choose supported remedies, revise coherently and inspect the actual result. Preserve its whole-text checks after section-level work. Do not apply proposals automatically or add another approval requirement because a risk is marked High.

Use the requested edit mode. Without one, follow the protocol's defaults: an inline result for an inline draft, a separate revised copy for a file draft, or the existing communication when no change is warranted.

Consume the inspected result and any returned needs. Keep required recipient context in the actual communication; private editorial notes are separate. The protocol's return does not itself mark fixcomm-wild complete.

## Handle returned needs — at any stage

Determine what the need affects from the current request, evidence and intended openness. Missing required substance, deliberately open meaning and optional detail are different situations.

| Need | Continue from |
|---|---|
| A supported local wording or integration defect | comm-revise's repair and readback; inspect affected connections too |
| Missing relevant material that can be read within the existing authority and scope | Return the specific need to unplugged surfacing with its discovery account; it arranges focused full Surfacing invocations, integrates evidence and issues an updated handoff; then reassess the affected review basis |
| Changed facts, target, recipient, purpose or applicable guidance that invalidate prior review | Renew comm-critic-d for the affected communication, then revision; the affected scope can be the whole draft |
| A required substantive choice, unresolved guidance conflict, inaccessible source or unavailable operating dependency | Explain the specific unmet need; continue independent supported work and hold the dependent outcome |

Give renewed invocations concrete inputs and output locations. Keep prompt/report pairs for different review bases distinguishable, using a fresh review subdirectory when renewing the critique. Retain still-valid evidence and work.

Route new evidence needs through the same discovery owner, including needs found during revision. Compare new material with the actual question and prior search scope. Update the identified context before renewing affected critique; do not repeat the whole investigation merely because a source or recipient changed.

**Expose consequential missing context and supported recovery opportunities.** Explain the required answer or claim affected, why it matters, where the answer may be obtained, the evidence for that lead, why it has not been obtained and the useful choices remaining. Use a proportionate explanation, not a mandatory card for every unknown.

Distinguish unread, inaccessible, outside-scope, disputed and absent material. The AI's missing context does not establish that nobody knows. A person's involvement can support a possible source or referral without proving they hold the answer. A vital gap still needs to be stated when no supported lead exists.

Pursue ready authorised reads without shifting that work to the user. Identifying a person as a possible source does not authorise contacting them. Return choices involving missing access, another person's response, a substantive undelegated decision or changed task scope.

Preserve explicit user choices while their task and circumstances remain unchanged. When new material arrives, inspect whether it answers the actual missing question and what prior judgments it changes. A reply or new file alone does not resolve the gap.

Do not repeat an operation on unchanged inputs and conditions when it cannot make further progress. Return the specific need and any usable partial result. Do not repeat the entire workflow after every edit or use zero findings as the completion rule.

## Resume an interrupted run

Read this entrance, `_fixcomm-wild.md`, the current task, discovery account and relevant actual artifacts. Recover needed source contents and check correspondence with the task/target the artifacts concern.

If acquisition is unfinished or its basis changed, load unplugged surfacing in full and use its resume procedure. Recover actual assignment status; a saved worker identifier or completion mark is not proof of current execution state or available evidence. Do not launch duplicate work while an earlier assignment may still be running.

If the run record is missing or inconsistent, reconstruct only what the actual artifacts and current request establish. Do not infer that a stage was checked merely because its output exists.

Identify the first genuinely unmet operation. A saved prompt may still need checking; an existing report may concern an earlier recipient or draft. Preserve valid work and renew only what the changed basis affects.

Load the resumed component's full instructions and required references, execute its remaining work, check the output, update the run record and continue.

## Finish and return

Finish after the actual result has been produced and inspected, and consequential unmet requirements have been addressed or explicitly returned.

Return the revised communication or its saved location prominently. Identify an intentionally unchanged result. Keep useful prompt/report links and editorial notes proportionate and separate from recipient-facing text.

When essential meaning remains unresolved, label the communication partial and explain what prevents fulfillment. An honest limitation may fulfill a request for a provisional update; it cannot silently replace an essential answer the current request still requires. If the user narrows the task, assess that new task without claiming the earlier objective was achieved.

Record the actual outcome and any remaining need in `_fixcomm-wild.md`. Keep search traces and worker details out of recipient-facing text unless they serve its purpose. Do not claim that inspection guarantees every possible defect was detected.

## Boundary

Work on the nominated communication. Do not implicitly send or publish it, contact people, perform the underlying operational task, change the principles, or archive review artifacts. Communication guidance assesses how work is expressed; it does not authorise managing that work.

Copy agent link
Report this
Terms of Service

This paste expires in <1 hour. Public IP access. Paste anything and get a link like this one from Context.