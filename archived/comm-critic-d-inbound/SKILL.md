

---
name: comm-critic-d-inbound
description: Generate and execute a tailored critique of a worker AI's communication to its orchestrator, including Supporting Context and numbered associations. Produces dynamic_comm_critic_prompt.md and ComCritic.md with supported risks and proposed remedies; leaves the delivery unchanged.
---

# comm-critic-d-inbound — Orchestrator Inbound Critique

Examine whether the coordinating recipient can understand and assess this particular contribution using the actual delivery, its task and the available work context.

Run **read the guides → formulate, save and check the prompt → execute, save and check the critique**. Finish each step before the next. Findings are proposals; do not draft corrections or the critique report while preparing the prompt.

## 0. Mandatory guide reading

At every invocation, read all six guides below in full into active context. Complete truncated reads. Headings, excerpts, summaries and remembered contents do not satisfy this prerequisite.

| Guide | Application |
|---|---|
| [Non-ambiguity](../comm-critic-d/references/non-ambiguity.md) | Apply shared referent, relationship and explanation checks to this inbound delivery. |
| [Meaning and fidelity](../comm-critic-d/references/meaning-and-fidelity.md) | Required answers, supported claims, status, corrections and intended openness. |
| [Recipient and purpose](../comm-critic-d/references/recipient-and-purpose.md) | The aspect, useful detail, voice and usable references required by this exchange. |
| [Operational communication](../comm-critic-d/references/operational-communication.md) | Apply when the contribution is an operational briefing, coordination message or genuine request. |
| [Author preferences](../comm-critic-d/references/author-preferences.md) | Apply only to communication authored in the author's name within each item's scope, not simply because the author receives the message. |
| [Supporting Context](../orchestrator-inbound-communication/references/supporting-context.md) | Inbound contribution, generous reference access, visible questions, evidence and supporting explanations. |

Resolve paths from this file. These shared checks apply under this entrance's inbound scope. Reading is mandatory; each item's application remains conditional. Use all four fields of a check together, including its limits.

Read additional applicable task guidance in full. Use an explicitly substituted set only when instructed. If a required guide cannot be read, identify it and hold prompt generation. Current task instructions govern; return genuinely unresolved guidance conflicts without silently imposing a stronger rule.

## 1. Formulate, save and check the dynamic prompt

Read the governing request, actual contribution and target delivery in full: main message, Supporting Context and pertinent deeper or reused explanations. Establish the reviewed version, author, recipient, purpose, medium, corrections and **intended openness**.

For an embedded outgoing draft, preserve its eventual recipient and keep orchestrator explanations outside that draft.

Use the identified discovery handoff and necessary source contents. Distinguish what is delivered or demonstrably available to the recipient from worker-private context. Do not assume either total ignorance or remembered access to the whole investigation.

Examine contextual needs in both directions:

- From the task and underlying work to the delivery, including omitted subjects and useful available explanation.
- From expressions, claims and relationships to the meaning, evidence, history or qualification they depend on.
- From supporting answers to the prerequisites they themselves assume.

Translate the applicable guides into tailored questions and instructions. Question selection is provisional: execution can reject, refine or extend it. A question may reveal useful support without yet establishing a defect.

The generated prompt must contain:

- The current task, contribution, exact target set, recipient, purpose, constraints and evidence handoff.
- Usable guide and source locations, mandatory full-guide reading instructions, and relevant conditions rather than bare check names. After context loss or in a separate execution, repeat the guide reads and recover needed source contents.
- The tailored local and whole-delivery examination, including reference coverage, entry questions, evidence and actual access.
- Explicit protection of **intended openness** in findings and proposals. Require missing meaning only when warranted for this communication; do not invent reasons, decisions or required precision.
- The execution duties and report format below, a concrete `ComCritic.md` output path, and the proposal-only boundary.

Save `dynamic_comm_critic_prompt.md`. Read the saved prompt back. Check target identity, usable inputs, applicable requirements, grounds for contextual questions and preservation of openness. Remove unsupported demands and correct missing instructions before execution.

## 2. Execute, save and check the critique

Execute the actual checked prompt against the target and evidence. For each candidate concern:

1. Establish what understanding matters to this exchange, including its explicit requirement for generous contextual access.
2. Identify the actual omission, distortion, unsupported assumption or reading difficulty.
3. Examine whether the exchange or usable support already provides an adequate explanation.
4. Retain a finding only when a concrete communication difficulty remains; explain its consequence at the certainty the evidence supports.

Do not turn every possible question into a risk. Do not remove useful optional support merely because it does not change an immediate decision.

For long deliveries, examine coherent sections with their needed context, then examine the whole account and its linked support. A whole-document skim does not replace local review; an isolated section is not the complete delivery.

Check question premises as well as answers. Distinguish one explanatory purpose from independent asks concealed under a heading. Check ordinary three-plus-one entries without forcing filler, false certainty or lossy splits. Assess whether markers, answers, evidence and qualifications agree.

Preserve the difference between a missing explanation, an unavailable fact and an intentionally open choice. Return specific new evidence needs to the caller's discovery owner; do not create a separate investigation or supply plausible answers.

Evaluate each proposed remedy against the same task, evidence and openness as the finding. Remedies may clarify, qualify, relocate, add or link a supported explanation, or identify the substance still needed. Do not manufacture ownership, next steps or a decision.

Save `ComCritic.md`. Read it back and check the target basis, support for every retained risk, report fields and proposed meaning. Merge duplicate findings. Correct report defects before returning. A no-findings report is valid; no coverage certificate or findings quota is required.

## Report format

Begin with a brief summary identifying the reviewed delivery and its principal risks. If none were identified, state that without empty risk records.

For each risk, use:

- **Risk:** Plain explanation and precise account of the problem and its basis.
- **Category:** Applicable communication concern, or a clear name for a supported concern not yet named by the guides.
- **Severity:** Low, Medium or High, with a reason tied to the recipient's actual difficulty.
- **Impact:** The misunderstanding, missing connection or mistaken use it could cause.
- **Context:** Background needed to understand this finding.
- **Affected areas:** Passage, entry, marker or missing answer, with a recoverable location.
- **Mitigation:** Concrete supported proposals. For Medium and High risks, consider quick, robust and long-term remedies; include distinct options only when meaningful.

Make the finding's grounds and proposed improvement understandable through these fields. Do not add a mandatory per-check ledger or a separate approval judgment.

## Return and boundary

Save the prompt and report together in the caller's review directory. If none is supplied, use a fresh review directory beside the target or in the workspace for inline text. Return both locations, a short summary and consequential unmet prerequisites.

Stop at criticism and proposals. Do not rewrite the delivery, apply remedies, contact people, send or publish content, modify guides or perform the underlying work. Discovery and supported revision remain with the caller.

