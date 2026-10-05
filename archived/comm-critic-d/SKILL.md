
---
name: comm-critic-d
description: Read the communication references, generate a tailored critique prompt, then execute it to identify risks and propose mitigations for outgoing messages, documents or presentations. Produces dynamic_comm_critic_prompt.md and ComCritic.md; leaves the target text unchanged.
---

# comm-critic-d — Dynamic Communication Critique

A thinking discipline for examining whether a communication conveys the meaning its intended recipient needs, faithfully and intelligibly. Turn applicable guidance into tailored questions, then use them to identify supported risks and propose remedies.

Run the following steps in order: **read the references → formulate, save and check the prompt → execute, save and check the critique**. Complete each step before starting the next. Do not draft the critique while generating the prompt, execute the stages in parallel, or write both artifacts together at the end.

## Step 0 — Mandatory reference reading

**At the start of every run, read all five files below in full into the active context before proceeding to Step 1.** Read the actual files; filenames, headings, summaries, selected excerpts and remembered contents do not satisfy this step. If a read is truncated, continue until the entire file has been read. Do not skip or shorten this prerequisite to save time or context.

Resolve these paths relative to this `SKILL.md` file.

| Reference | What it supplies and when its rules apply |
|---|---|
| [Non-ambiguity](references/non-ambiguity.md) | Shared checks for referents, relationships, actions, purposes, context and connected explanations. |
| [Meaning and fidelity](references/meaning-and-fidelity.md) | Shared checks for required answers, supported claims, actual status, intended openness and retained corrections. |
| [Recipient and purpose](references/recipient-and-purpose.md) | Shared checks for the relevant aspect, level of detail, readability, voice and usable supporting references. |
| [Operational communication](references/operational-communication.md) | Supplementary checks applied to progress briefings, decision requests and coordination messages. |
| [Author preferences](references/author-preferences.md) | Supplementary checks applied to outgoing communication in the author's name, respecting each item's narrower conditions. |

Reading is mandatory; applicability remains conditional. Consider every shared concern without manufacturing a finding for every item. These files organise checks, not a fixed category taxonomy.

Read additional task-supplied guides in full when their stated scope applies. Use a replacement reference set only when explicitly instructed. If a required file cannot be read, identify the missing input and stop before generating the prompt; do not invent substitute guidance.

### How to apply the references

- Judge the meaning required for this exchange. Respect shared context, medium conventions and explicit requirements; do not assume either complete reader ignorance or access to the AI's private context.
- Preserve intended openness in findings and proposals. Unresolved choices may stay open while their subject becomes understandable. Do not invent missing substance or infer that an absent explanation proves the author never thought about it.
- Preserve each check's conditions when tailoring the prompt. Several checks may inform one question or finding. Remain open to other supported communication risks beyond the listed checks.
- Current explicit instructions govern the task. Apply personal and organisational guidance within its stated scope; a personal preference is not an organisation-wide policy. Identify unresolved conflicts between applicable guides rather than silently imposing a stronger requirement.

Each check item has four separate fields:

1. **What to examine:** The aspect to inspect.
2. **What counts as a problem:** The condition that warrants a finding.
3. **Why it matters:** The misunderstanding or difficulty it causes.
4. **When it applies—and its limits:** Conditions and boundaries against overreach.

Use all four fields together. Examples are optional aids to understanding, not additional universal requirements.

## Step 1 — Formulate, save and check the dynamic prompt

Read the target text and the request it serves in full. Identify its version, author, recipient, purpose, medium and supporting context. Use supplied instructions and context; ask only when a missing distinction prevents identifying or judging the target.

Distinguish supporting material from what the recipient will actually receive. An outgoing draft shown to the operator still has its outgoing recipient. Previously surfaced context is usable when its relevant contents remain available.

Establish what the communication must convey now, what the recipient can reasonably be assumed to know, and what should remain open. Ground these judgments in the request and available context.

Translate the applicable references into questions or instructions tailored to this text's purpose, claims, relationships and possible omissions. Adapt the emphasis to the kind of communication. Examine required meaning absent from the draft as well as the wording already present.

The generated prompt must carry:

- The target, original request, recipient, purpose and relevant context.
- The reference paths, mandatory reading instructions and applicable guidance with its qualifications. A separate execution or resumption after context loss must repeat the full reference read; source names and summaries are insufficient.
- Explicit instructions to preserve **intended openness** in findings and mitigation proposals. Require missing meaning only when the present communication needs it; do not force decisions or precision that the task deliberately leaves open.
- The tailored examination, the execution instructions and report format below, the output path for `ComCritic.md`, and the boundary that proposals remain unapplied.

Save the prompt as `dynamic_comm_critic_prompt.md`. Read the saved file back and check that it carries the requirements above, usable source locations and the correct target, without dropping an applicable requirement or adding an unsupported demand. Correct the prompt before proceeding. **Step 2 begins only after the saved prompt passes this check.**

## Step 2 — Execute, save and check the critique

Execute the actual saved prompt against the target and its supporting material; do not substitute a remembered or generic critique. Ground each finding in a passage or missing answer, an applicable requirement and a consequence for the reader.

For long texts, examine coherent chunks one at a time with the context needed to interpret them. Finish the local review before examining the whole communication for missing answers, inconsistent claims and broken connections between sections. Do not substitute a whole-text skim for the chunk review or treat isolated chunks as the complete review.

Assess proposed mitigations against the same facts, intent and intended openness as the findings. Combine duplicate findings; do not manufacture risks or alternatives to fill the report.

Save the result as `ComCritic.md` using the format below. Read the saved report back: verify the reviewed target, required finding fields, support for each risk and that proposals preserve the facts, intent and intended openness. Correct report defects before returning it. If no risks were found, do not create empty risk records to satisfy the format.

## Report format

Begin with a brief summary identifying the reviewed text and its main risks. If none were identified, say so without inventing findings.

Use a section for each risk, with these fields:

- **Risk:** a plain explanation followed by a precise account of the problem and its supporting basis.
- **Category:** the applicable communication concern from the references, or a clear description of a supported concern they do not yet name.
- **Severity:** Low, Medium or High, with a reason tied to the consequence for the intended reader.
- **Impact:** the misunderstanding, difficulty or mistaken action the problem could cause.
- **Context:** prerequisite background needed to understand this finding; avoid repeating the risk explanation.
- **Affected areas:** the relevant passage and location, or the required answer missing from the communication.
- **Mitigation:** concrete, supported proposals. For Medium and High risks, consider quick, robust and long-term remedies; include distinct options only when they are meaningful. Explain what makes a robust or long-term option useful.

## Output and boundary

Save both artifacts together in the requested output directory; otherwise use a new review folder beside the target file, or in the current workspace for inline text. Return links to the prompt and report with a short summary.

Stop at findings and proposals. Do not rewrite or send the target, apply mitigations, modify the references or perform the underlying operational task. Context surfacing and folding corrections into the text belong to the surrounding workflow.

Manager principles, task framing, operator-specific reporting and delivery orchestration are outside this skill. Operational checks assess how work is communicated; they do not direct the critic to run that work.


