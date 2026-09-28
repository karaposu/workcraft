
# What is Workcraft?

**Workcraft is a generic framework for automating work through AI.** Its central hypothesis is that any work can be performed by AI, and that the work can be decomposed through seven concepts: Communication, Semantic Formulation, Context Accumulation, Artifact Operations, Alignment, Pulse and Orchestration.

Workcraft approaches each assignment with this decomposition in mind. It identifies what the work requires under each concept, making it possible to understand, develop and automate those responsibilities individually or in combination. This gives each part a focused treatment while preserving its relationships with the rest of the work.

Automation can therefore progress incrementally. One concept can be automated while others still rely on human involvement. Several automated concepts can then be combined to handle a larger part of the assignment. **The hypothesis is that fully automating all seven concepts for a piece of work, and coordinating them successfully, amounts to fully automating that work.**

The framework applies this approach across domains: software, research, data analysis, visual design, a Blender scene, a presentation, company coordination or a change to a live system. The intended result can be a work product, an operational effect, a supported judgment or a clearer understanding.

Each assignment supplies its objectives, domain knowledge, tools, access, resources and ways to observe results. The seven concepts organize how those means are used to achieve the outcome.

## The seven concepts at a glance

| Concept | Responsibility |
|---|---|
| **Communication** | Make the work understandable to its recipients, with appropriate context, evidence, purpose and faithful meaning. |
| **Semantic Formulation** | Develop and test a coherent answer, interpretation, judgment or approach that fits the task and context. |
| **Context Accumulation** | Discover, understand, reconcile, retain and refresh the information the work depends on. |
| **Artifact Operations** | Create, inspect, modify, organize and maintain the work products and records needed for the task, using appropriate tools. |
| **Alignment** | Compare the intended work and its actual state, then address meaningful mismatches. |
| **Pulse** | Observe relevant sources and pending outcomes over time, detect changes or returns, and make those observations available. |
| **Orchestration** | Decide which actions should happen next and coordinate their dependencies, order, execution and waits. |

These concepts describe interacting responsibilities. One action can involve several concepts, and each concept can require a different depth of treatment for the task.

Communication, Semantic Formulation, Context Accumulation, Artifact Operations and Pulse are the five working capabilities. Orchestration coordinates their use, and Alignment examines their direction and results throughout the work.

## 1. Communication — v1 complete

Communication makes a contribution understandable and assessable for the person or AI receiving it. It covers non-ambiguity, surrounding context, the appropriate view for the exchange, supported claims and preservation of intended openness.

The same recipient may need a technical explanation, an exploratory discussion or an operational update at different times. The current task determines the required emphasis and detail.

### Two principal workflows

| Workflow | Skill package | What it produces |
|---|---|---|
| **Outgoing communication** | [Fixcomm Wild](../artifacts/skills/fixcomm-wild/SKILL.md) | An inspected revision of a message, document or presentation intended for another recipient, with saved critique proposals. |
| **Communication toward the orchestrator** | [Orchestrator Inbound Communication](../artifacts/skills/orchestrator-inbound-communication/SKILL.md) | A composed or revised worker contribution, accompanying Supporting Context and evidence, and saved critique proposals. |

**Fixcomm Wild** starts with an existing outgoing draft. It establishes the relevant context, creates and executes a tailored critique prompt, then applies supported corrections through a separate revision protocol. The calling workflow supplies the initial outgoing draft.

[Ordinary Fixcomm](../artifacts/skills/fixcomm/SKILL.md) is also packaged. It follows the same critique-and-revision structure using ordinary Surfacing directly. Fixcomm Wild adds coordinated discovery when relevant context may be scattered across sources.

**Orchestrator Inbound Communication** serves the coordinating recipient: the human now, or a separate AI orchestrator later. It can start from an existing draft or compose a candidate from established work. It explains the substantive contribution, what it means for the current task, and the evidence and qualifications needed to assess it.

An outgoing draft shown to the orchestrator retains its eventual audience. The explanation accompanying it serves the orchestrator and can contain different contextual detail.

### Component skills, protocol and guides

| Component | Responsibility | Packaging |
|---|---|---|
| **Unplugged Surfacing** | Form context inquiries, investigate across sources, consume the evidence and maintain an integrated task account. | Independent [outgoing copy](../artifacts/skills/fixcomm-wild/references/unplugged-surfacing/SKILL.md) and [inbound copy](../artifacts/skills/orchestrator-inbound-communication/references/unplugged-surfacing/SKILL.md). |
| **Ordinary Surfacing** | Bring relevant material from a bounded source territory into the AI's context and save a trace of the inspected scope. | [Outgoing copy](../artifacts/skills/fixcomm-wild/references/surfacing/SKILL.md) and [inbound copy](../artifacts/skills/orchestrator-inbound-communication/references/surfacing/SKILL.md), each with its full operating reference. |
| **comm-critic-d** | Read applicable guidance, generate and check a dynamic critique prompt, then execute it and save supported risks and proposed remedies. | Separate [outgoing entrance](../artifacts/skills/fixcomm-wild/references/comm-critic-d/SKILL.md) and [inbound entrance](../artifacts/skills/orchestrator-inbound-communication/references/comm-critic-d/SKILL.md), each owned by its package. |
| **comm-revise** | Assess critique proposals, apply supported corrections and inspect the resulting communication. | Independent [outgoing protocol](../artifacts/skills/fixcomm-wild/references/comm-revise.md) and [inbound protocol](../artifacts/skills/orchestrator-inbound-communication/references/comm-revise.md). |
| **Communication reference guides** | Supply checks for non-ambiguity, meaning and fidelity, recipient and purpose, operational communication and scoped author preferences. | Independent copies within each package. Applicability follows the guide and the actual task. |
| **Supporting Context guide** | Govern the orchestrator's numbered explanations, visible questions, evidence, depth and usable associations. | Additional [inbound guide](../artifacts/skills/orchestrator-inbound-communication/references/supporting-context.md). |

Both principal packages own their dependency files. Shared components were copied exactly at creation; they are ordinary independent files, so later changes can be made separately. Neither package requires the other package to be installed.

The dynamic critic produces `dynamic_comm_critic_prompt.md` and `ComCritic.md`. The report contains risks, categories, severity, impact, prerequisite context, affected areas and proposed mitigations. It does not apply its own proposals. Revision performs that separate judgment and correction step.

### Supporting Context for the orchestrator

The main message should already convey the contribution and its important qualifications. Numbered references provide access to supporting explanations and evidence without assuming that the recipient remembers the worker's investigation.

A supporting entry has a reference number, an informative title and visible questions with answers underneath. Its normal arrangement is:

- Up to three questions tailored to what the entry explains.
- One question about how its subject fits with earlier or related work.

Simple entries use fewer questions. One question may need several facts in its answer; several independent asks should not be hidden under one heading.

Useful context must survive the arrangement. Remove duplicate questions, keep supporting details with their answer, and use coherent additional entries or deeper explanations when helpful. Preserve an explicit exception if the normal question count would otherwise damage understanding.

References should be generous where they provide meaningful contextual access, including optional depth. The visible question count does not limit context discovery. A source link must not make the reader reconstruct the explanation from raw records.

### What “v1 complete” establishes

**Communication v1 is complete in design and packaging.**

The workflows, component responsibilities, reference guidance, critique artifacts and supported-revision process are authored and packaged. The new inbound package has passed structural and portability checks. Communication has enough defined structure to enter practical use and improve through observed failures.

This milestone concerns preparation and quality of the communication. Orchestration still decides when communication is needed and who should receive it. Tools carry out authorized delivery; Pulse detects relevant replies; Context Accumulation integrates their meaning; Orchestration decides what changes next.

Practical communication reliability and the process for turning recurring corrections into better guidance will be developed through use. A completed package does not establish that every important defect will be detected.

## 2. Semantic Formulation

**Semantic Formulation develops a coherent answer, interpretation, judgment or approach that fits a particular problem, purpose and context.** It includes working out the relevant criteria, testing alternatives, integrating conclusions and checking their combined fit.

The activity is called **semantic calculation**. It is needed when the substance still has to be worked out: what a concept means, which approach fits, how parts relate, or whether a proposed solution is sound.

**Traverse** supplies a structured method:

**Articulate-Simple → Surfacing → Sensemaking → Decomposition → Innovation → Critique → Routelister → Conclude.**

Articulation establishes the question without prematurely closing meaningful ambiguity. Surfacing supplies relevant material. Sensemaking clarifies meaning. Decomposition separates tractable questions and their dependencies. Innovation develops alternatives. Critique tests them. Routelister exposes possible onward directions. Conclude produces a usable finding.

The method can repeat when the original question remains unanswered. Its saved outputs make the reasoning and remaining uncertainty inspectable. Routelister lists directions; selecting which direction to pursue belongs to Orchestration.

**Current position:** the capability and its method are established and have been used to develop framework components. The remaining integration work includes recognizing when a task needs a full inquiry, supplying its basis, coordinating related inquiries and checking the assembled result. Reasoning does not replace missing observations, specialist execution or an undelegated human decision.

## 3. Context Accumulation — partially implemented

**Context Accumulation makes the understanding needed by the work available, reliable enough for its use, retained and refreshable.** It includes source discovery, relevant history, relationships, domain knowledge, evidence quality, contradictions and changes over time.

### What Unplugged Surfacing already supplies

Unplugged Surfacing provides a substantial implementation within a particular task:

- Recover the task's origin, surrounding exchange, meaningful identities and context leads.
- Form questions from the task and investigate available sources independently, including sources not directly linked from the starting material.
- Follow relevant discovered connections across sources.
- Coordinate bounded ordinary Surfacing assignments, using parallel workers where useful and permitted.
- Read returned evidence, reconcile supported relationships and retain qualifications, contradictions and unknowns.
- Save integrated understanding, source locations, actual coverage and unfinished needs in `context.md`.
- Accept an existing account, resume work, retain valid evidence and renew the investigation when questions or facts change.
- Issue a checked context handoff and preserve its basis when later discoveries affect work that already consumed it.

Ordinary Surfacing and Unplugged Surfacing have different outputs. The ordinary skill's trace records what was inspected and its relevance; it does not contain the source contents. The coordinator's `context.md` carries integrated task understanding and usable evidence.

The component is currently bundled in the communication packages, but its inputs are generic: a task, purpose, starting material, source environment, bounds and output location. It can support research, technical investigation or other work without a communication draft.

### What remains for the broader capability

Context Accumulation across a continuing body of work still needs arrangements for:

1. **Future discovery:** deciding which understanding should survive and how another task finds the relevant prior accounts.
2. **Maintenance:** deciding who refreshes shared understanding, when renewal happens and which historical states remain useful.
3. **Propagation:** recognizing which plans, artifacts, communications or active tasks depend on changed understanding and making sure those consumers reconsider it.

The existing component already provides task-level persistence and refresh. The unfinished work concerns their use across tasks and consumers. Updating a context account alone does not update every dependent plan.

**Current position: partially implemented.** Reuse Unplugged Surfacing as the existing task-level foundation. Develop broader continuity around it as actual work establishes the need; a new universal memory platform is not a prerequisite for using what exists.

## 4. Artifact Operations

**Artifact Operations creates, inspects, modifies, organizes and maintains the work products needed to accomplish a task, using the appropriate tools.** It includes choosing the right form, working on the content, placing it where it belongs, connecting it to related work and maintaining its state.

The work products themselves are **artifacts**: source code, a Figma file, a Blender scene, a dataset, a spreadsheet, a presentation or a report. They also include context accounts, critique reports and task coordination records.

Artifact operations include creating a document, editing a spreadsheet, modifying a design, building or rendering a scene, changing source code, and exporting or updating a deliverable. An operation can use an application's interface, a script, an API or MCP. The interface is the means of performing the operation.

Classify tool use by the responsibility it serves. Searching for background information serves Context Accumulation; editing a work product serves Artifact Operations.

Completion depends on the requested outcome. A document describing a system change does not establish that the system changed. A native design file may itself be the requested deliverable, but its contents still need appropriate inspection.

**Current position:** the role is defined and concrete framework artifacts and skill packages exist. Broader implementation needs domain-specific creation, inspection, placement and maintenance capabilities, with clear ownership when shared artifacts change.

## 5. Alignment

**Alignment keeps the intended work and its actual state comparable throughout execution.** AlignCraft supplies six layers:

1. **Workspace:** the environment, access and context support the work.
2. **Task:** the purpose, scope, depth and expected result are understood.
3. **Action-Space:** relevant approaches and possible actions are being considered.
4. **Action-Set:** the selected actions are appropriate and feasible under the actual constraints.
5. **Coherence:** changes preserve or deliberately revisit relationships and commitments elsewhere in the work.
6. **Outcome:** observed results are compared with what was intended.

Four pillars make that examination usable: **Explicitness → Visibility → Measurement → Comparison**, followed by an appropriate response and recheck.

Measurement can be qualitative. A useful comparison might establish that an important qualification is absent, a source is outdated or a result remains unverified. Numerical scores require meaningful definitions and evidence.

**Current position:** the alignment model is established and informs the operating guidance. Its continuous application across autonomous tasks still needs integration with actual actions, observations and interventions. An alignment question can investigate uncertainty without assuming a failure has already occurred.

## 6. Pulse

**Pulse observes what is happening around the work over time.** It checks relevant sources and pending outcomes, detects new information or changes, and makes those observations available to the work.

Examples include a colleague's reply, a completed render, feedback on a design, changed source data or the result of a deployment. Checks can follow an event, an elapsed interval or a task-specific condition.

Each Pulse check has a subject, a source, a timing or trigger condition, and a destination for relevant observations. There is no universal polling interval.

Its result is an observation: a reply has arrived, a render has finished, a source has changed, or a checked condition remains unresolved. Context Accumulation incorporates the relevant information into the current understanding.

Pulse and Orchestration are separate concepts. Pulse supplies observations about what happened. Orchestration uses those observations and the task's current understanding to decide what should happen next.

**Current position:** the purpose and task-dependent model are defined. Actual scheduling, source detection, persistence of pending checks and delivery of returns into active work remain implementation work.

## 7. Orchestration

**Orchestration decides and coordinates the work to be done.** It uses the task's goals, current understanding, dependencies and available capabilities to choose actions, arrange their order and determine what can proceed.

Observations from Pulse are one input to those decisions. Orchestration determines whether to resume waiting work, change priorities, request more investigation, revise an approach or continue the current activity.

It maintains the distinction between work that can proceed, work waiting on a dependency and work whose meaning still needs clarification. Independent work can continue while another part waits.

### The task's evolving orchestration file

For work needing explicit coordination, maintain an `orchestration.md` with concrete action cards and their relationships. Each card should make clear:

- What needs to be done and the expected result.
- Why it matters and how it contributes to the task outcome.
- What it depends on, including other actions or external inputs.
- Whether it can proceed now, with the reason.
- What remains provisional or unclear.
- What actually happened and what that result changes.

A dependency names the contribution required from another action; a preferred order is not automatically a dependency. Existing adequate results should be reused rather than recreated to fill a plan.

Some actions can be defined precisely at the start. Others become clearer as context and results arrive. Preserve that unevenness. A clear action can still be blocked; a provisional action may still contain useful work that can begin.

### The operating cycle

1. Understand the task and the outcome it needs.
2. Examine what the five working capabilities must contribute, using Alignment across them.
3. Make the next actions, dependencies and unresolved parts explicit.
4. Select ready work and execute it through suitable skills, tools or performers.
5. Inspect the actual result and compare it with the intended result.
6. Incorporate returning information and revise the affected context, artifacts, communication and next actions.

The cycle continues while useful authorized work can proceed. Keep waiting dependencies visible while independent work progresses. A task can finish, wait on a genuine dependency, reach an explicit stopping condition or continue as an ongoing responsibility. An acknowledgement, saved file or sent message only establishes the result it actually demonstrates.

**Current position:** an initial playbook and the task-level orchestration-file approach have been developed. Selecting and invoking capabilities automatically, managing persistent waits, reconciling returns and operating the complete cycle still require a general runtime and practical calibration.

## How the concepts work together

Context Accumulation supplies understanding. Semantic Formulation develops the answers and approaches still requiring thought. Artifact Operations uses specialized skills and tools to create, inspect and maintain work products. Communication makes the contribution usable by its recipients. Pulse observes relevant changes and returns. Alignment examines fit throughout. Orchestration decides how to coordinate these responsibilities toward the task's outcome.

For example, Pulse detects that feedback on a design has arrived and makes the feedback available. Context Accumulation connects it to the current brief and earlier decisions. Orchestration then decides which work should change and whether it can proceed now. Semantic Formulation may resolve a design question; Artifact Operations then uses the appropriate tool to change the native design file. Alignment checks the result, and Communication explains the change with the appropriate support.

The required depth follows the task. These concepts provide a way to notice missing responsibilities without requiring every action to produce seven reports.

