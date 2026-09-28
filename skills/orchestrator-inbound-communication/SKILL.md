
---
name: orchestrator-inbound-communication
description: Prepare or revise a worker AI's message and Supporting Context for the human or AI coordinating its work. Use for explanations, results, proposals, reviews and updates that need recoverable context. Combines Unplugged Surfacing, an inbound-specific dynamic critique and supported revision.
---

# Orchestrator Inbound Communication

Make the contribution understandable and assessable without assuming the orchestrator shares the worker's detailed context. Explain what the work establishes, its significance for the current exchange, and the evidence and limits that support it.

Run **prepare → establish context → compose the delivery → critique → revise → inspect and return**. Preserve **intended openness**: choices, concepts or uncertainties the task deliberately leaves unresolved.

## Mandatory execution discipline

Read this entrance in full. At each component invocation:

1. Load its actual instructions and mandatory references in full into active context. Complete truncated reads; summaries, filenames and remembered instructions are insufficient.
2. Execute the complete component. Finish and check its actual output before starting dependent work. Do not prepare critique findings while generating the dynamic prompt.
3. Keep the necessary source contents available through the handoff. Recover them after context loss; a source list or completion message is not evidence.
4. Record the checked handoff and continue immediately to the next ready operation. A component returning does not finish this workflow.

Only independent discovery assignments may run concurrently, under Unplugged Surfacing's coordination and the host's permissions. Critique and revision use an identified, checked context handoff; ongoing workers must not silently change it.

## Component dependencies

| Component | Use |
|---|---|
| [Unplugged Surfacing](../unplugged-surfacing/SKILL.md) | Coordinate discovery, consume evidence and return integrated context. |
| [Ordinary Surfacing](../surfacing/SKILL.md) | Execute each assignment under Unplugged Surfacing, including its full operating reference. |
| [Inbound communication critic](references/comm-critic-d/SKILL.md) | Read its six guides, save and check a dynamic prompt, then execute and check the critique. |
| [Communication revision](references/comm-revise.md) | Assess proposals, apply supported corrections and inspect the result. |
| [Supporting Context](references/supporting-context.md) | Govern inbound explanation, numbered entries, visible questions and evidence. |

Install the Workcraft skill folders together as siblings. Resolve paths from the file declaring them. Use the shared Surfacing skills and this skill's own inbound critic, guides and revision protocol at the locations above unless the user explicitly supplies a replacement. Invoke each component by loading and executing its instructions; the separate outgoing `comm-critic-d` does not replace the inbound critic.

The five communication guides used by the inbound critic live in `references/comm-critic-d/references/`. Supply these actual paths and `references/supporting-context.md` to revision as mandatory applicable guidance. A missing operating dependency holds its dependent stage; identify the exact missing file.

## 1. Prepare the communication and workspace

Read the governing request, available work and any nominated message in full. Establish:

- The contribution being communicated, its actual state, and the current communication task.
- The author, coordinating recipient, purpose, medium, corrections and exclusions.
- Available evidence, source environment, recipient access and what should remain open.
- Any requested output location, edit mode or existing supporting explanation.

The recipient's role does not impose a managerial summary, recommendation or approval request. An outgoing draft embedded in this delivery retains its eventual audience; its accompanying explanation serves the orchestrator.

Use the requested workspace, or a fresh review directory beside the target file or in the current workspace. Preserve unrelated outputs and earlier review runs.

Maintain a compact `_inbound.md` with the current task and target locations, component locations, identified context handoff, last checked operation, next operation and consequential unmet needs. Point to substantive artifacts rather than copying their contents.

## 2. Establish and integrate the context

Load and execute Unplugged Surfacing with this purpose:

> Recover the existing material needed to understand and assess this contribution for the current communication task, including meaningful context and required answers absent from the draft.

Supply the task, contribution, draft if present, origin and relevant exchange, source environment and guidance, restrictions, any work allowance, and existing evidence or context accounts. Use `discovery/` for its outputs.

Include the recipient's actual question, objects and relationships, relevant earlier work and changes, evidence supporting or challenging claims, applicable corrections, known recipient context and intended openness. Preserve useful optional context as well as essential interpretation.

Retain independent source inquiries and pursuit of meaningful discovered links. Reuse actual evidence and prior coverage where they answer the current questions; familiarity alone is insufficient. The coordinator may establish that no additional retrieval is needed. A delivery's question count does not bound discovery.

Read the returned `context.md` and necessary source contents. Check correspondence to the task, supported relationships, qualifications, source scope and unfinished needs. Account for owned workers and isolate late outputs before accepting the handoff. Record its identifier.

Keep the discovery account separate in purpose from recipient-facing Supporting Context. Reuse suitable substance; do not forward investigation state as the explanation by default.

## 3. Compose the candidate delivery

Read the Supporting Context guide and all five shared communication guides in full before composing. Apply personal and operational guidance only within its stated scope.

Use an existing candidate when supplied; otherwise compose one from the established work and task. Do not complete missing substantive work by inventing an answer.

Prepare the main message and its supporting explanations together:

- State the substantive answer or contribution and the significance needed for this exchange.
- Keep qualifications that change a main claim beside that claim.
- Identify useful contextual questions from the task/work, the draft's expressions and relationships, and the supporting explanations' own dependencies.
- Provide generous numbered access to meaningful explanations and evidence, including useful optional detail.
- Form coherent Supporting Context entries using the guide's visible questions and normal three-plus-one arrangement.
- Reuse fitting explanations after checking their content, state and accessibility.

Use the requested form. By default, save a candidate `Message.md` and `SupportingContext.md` together. Compact support may accompany an inline message; an adequate existing document may serve directly. Create deeper files only when they carry useful explanation. Keep discovery traces and editorial records outside the recipient's delivery.

Identify the exact candidate files or passages and the supporting destinations that belong to the review. Save and read back the candidate before critique.

## 4. Run the inbound dynamic critique

Load and execute the bundled inbound communication critic. Supply:

- The candidate message and Supporting Context, including relevant deeper or reused explanations.
- The governing request, contribution, author, recipient, purpose, medium and intended openness.
- The identified context handoff, usable supporting evidence, limitations and applicable guidance.
- A concrete review directory for the prompt and report.

Require its full guide reads, then creation, saving and checking of `dynamic_comm_critic_prompt.md`. Only then execute that saved prompt and save and check `ComCritic.md`.

Consume both artifacts. Findings and mitigations remain proposals. A no-findings report is valid and still proceeds to revision's inspection of the actual delivery.

## 5. Apply supported corrections

Read and execute the bundled revision protocol in full. Supply the candidate delivery as the target set, its task, `ComCritic.md`, supporting evidence, all five shared guide paths and the Supporting Context guide. Include the dynamic prompt when needed to recover the review basis.

Revise the main message and authored support coherently. Preserve source evidence and reused documents unless editing them is explicitly in scope. Preserve valid material that the critic did not mention.

Follow the requested edit mode; otherwise produce a separate revised delivery or return an already adequate candidate unchanged. Resolve links for the actual delivery location.

Consume the inspected result and returned needs. Do not accept a proposed correction solely because it appears in the report or carries High severity.

## Handle returned needs

- **Known meaning is poorly expressed:** repair it through revision and inspect the affected connections.
- **Relevant evidence is missing or changed:** return the specific question through the same Unplugged Surfacing owner. Integrate the return and identify the new handoff before renewing affected critique and revision.
- **The task, target, recipient or applicable guidance changes:** reassess the affected review basis; retain valid work and keep renewed prompt/report pairs distinguishable.
- **A required source, dependency or substantive choice is unavailable:** continue independent supported work and return the specific unmet need. Preserve deliberately open meaning.

Expose consequential context gaps with the affected understanding, why it matters, any evidenced recovery source, why it remains unavailable and the useful choices remaining. A possible person or system holding the answer is a lead, not proof of possession. The AI's missing context does not mean nobody knows.

Pursue ready authorized reads. Contacting people or making an undelegated substantive choice requires its own authority. Preserve the user's existing choices. Do not repeat unchanged operations that cannot make progress.

## Inspect and return

Read the actual final message and support. Verify the substantive answer, scope, evidence, intended openness, question/answer fit, marker destinations, deeper links and recipient access. Examine coherent sections and then the whole delivery. Repair supported local defects and read the affected result again.

Return the message or its location prominently, with usable numbered support and accompanying evidence. Keep prompt/report links and editorial notes separate and proportionate. An informative message needs no invented ask.

Identify consequential unfinished requirements and supported recovery opportunities. A provisional account may satisfy a provisional task; it must not be presented as completion of a still-unanswered final task.

Update `_inbound.md` with the actual outcome. Finish when the delivery has been produced and inspected and remaining consequential needs have been resolved or explicitly returned. Do not use zero findings as a completion rule.

## Resume

Read this entrance, `_inbound.md`, the current task and actual artifacts. Recover required instructions and source contents. Check current discovery/worker status before redispatching; do not infer completion from file existence.

Resume the first genuinely unmet operation. Preserve valid work; renew only what a changed basis affects, then continue through the remaining stages.

## Boundary

Prepare and improve this communication. Do not implicitly send or publish it, contact people, manage the underlying work, change reference principles or archive review artifacts. Report what was produced and checked without claiming perfect detection or complete knowledge.

