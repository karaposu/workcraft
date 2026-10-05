
# AI operations orchestration playbook

**Version 0.8 · 17 September 2026 · Evolving orchestration file added to the working practice · Candidate operating guidance**

## Purpose: what this playbook is for

This playbook describes **how an AI operations manager should decide what to do next to move real work forward**. It treats orchestration as maintaining alignment while work progresses. It captures the orchestration Enes currently supplies: directing investigation, noticing missing understanding, selecting a design approach, coordinating people, reviewing communications, maintaining artifacts and checking results.

Its primary intended user is the **future AI orchestrator**. The human supervisor can use the same guide to inspect its decisions, correct it and retain control of consequential judgments. The aim is for the AI to carry the operational detail and explain the choices that matter, so the supervisor can make informed decisions without memorizing the entire project.

The playbook answers questions such as:

- What must we understand before choosing an approach?
- Does this new information change the plan, the people involved or what we already communicated?
- Can we answer this ourselves, or is a colleague's input needed?
- What can move forward while another part waits?
- Is this output ready to share, and can its recipient understand and act on it?
- What evidence would establish that the intended outcome happened?

Model evaluation supplied the historical examples. The rules are expressed for other operational assignments too. Company-specific tools, people, authority and source locations must be supplied separately. This document does not grant authority, schedule monitoring or implement an autonomous agent.

### How it fits the automation you described

The orchestrator combines communication, Semantic Formulation, context accumulation, artifacts and pulse into a sequence appropriate to the situation. AlignCraft supplies the alignment questions used to examine those activities and their effects; orchestration chooses the interventions that establish, question, restore or preserve alignment. A tool or skill performs a capability; this playbook helps decide **why to use it now, what to give it, and what to check afterward**.

Example: a colleague replies while a recommendation is being drafted. The orchestrator recognizes which open question the reply addresses, reads the full answer, checks what it changes, revises affected work and decides whether another message is still needed. You currently prompt many of those transitions yourself.

The original concept and still-open design questions are retained in the [concept notes](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/ai-operations-manager-concept-notes.md).

## Evidence and limits

The general orchestration pass consolidates **389 orchestration records from 358 of 423 prepared transcript windows**, plus the initial source segment. Those reviewed windows are from the model-evaluation project's Claude history: the early conversation is complete, and seven windows remain in the later conversation. The 58 Codex windows have not received that general pass.

A separate targeted study now documents **77 recovered Traverse inquiry attempts** across the available local Claude and Codex archives: 28 began in August–September and 49 in the earlier July history. Seventy-three reached a documented finding; four paused, failed to launch or were restarted. This study includes three actual Codex inquiries and selected continuations, without marking the whole Codex history reviewed. The [usage catalogue](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md) records every recovered attempt and its limits; the [usage taxonomy](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-taxonomy.md) develops the cross-case guidance. No separate ChatGPT web export was located. These counts are separate from the 389 orchestration records and should not be added to them.

The records include ordinary progress, successful recovery, repeated failures and unresolved outcomes. They are **not 389 independent experiments**, and human approval is not proof that an output was factually correct. The links below point to episodes with exact transcript references; continuations in the [evidence index](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence-index.md) preserve later corrections.

Three kinds of material are kept distinct:

| Kind | Meaning here |
| --- | --- |
| Observed episode | A recorded instruction, response, action or result, with its limits. |
| Candidate operating rule | A recommendation synthesized from those episodes; it still needs testing on further work. |
| User design requirement | A requested feature of the future system, such as evidence alongside supervisor communication. Its implementation and effectiveness may remain untested. |

The numbered moves below are candidate rules. Their supporting episodes also contain mistakes; the rule is not an endorsement of every historical response.

## AlignCraft: the diagnostic foundation

Enes has now explained that the historical interventions were made while continually checking AlignCraft’s six layers and four pillars. That is direct evidence of the overall intent behind this way of working. **The interpretation of any particular episode still needs its own evidence.** We retain what the transcript shows and label the layer mapping as retrospective analysis when the layer was not explicitly named at the time.

AlignCraft is the adopted framework for this playbook. The framework organizes possible misalignments into six layers. Its universal coverage claim is a premise of the methodology, not a finding established by this one-project corpus. Several layers can be involved in one episode, and a question can test alignment without establishing a failure.

### Six layers, applied to operational work

| Layer | Question for the orchestrator | Operational example |
| --- | --- | --- |
| **1. Workspace Alignment** | Is the environment and relevant context set up so the work can be understood and performed? | A resumed session needs current decisions, source locations and usable access; reading a stale handoff is insufficient. |
| **2. Task Alignment** | Do the participants share the intended purpose, depth, scope and success expectation? | The requested deliverable is an operating model; the AI is instead developing one evaluation’s mechanics. |
| **3. Action-Space Alignment** | Is the AI considering the appropriate domain of possible approaches and actions? | It assumes the previous evaluation method is the only route, overlooking a new method or another evidence source. |
| **4. Action-Set Alignment** | Within that space, which concrete actions are preferable and feasible under the actual constraints? | The method is plausible, but the order, owner, access, capacity or prerequisite makes the selected plan unsuitable. |
| **5. Coherence Alignment** | How will this action affect alignments already established, and what must be preserved or reconsidered? | A clearer rewrite restores a question the user explicitly removed; a changed premise leaves several dependent artifacts misleading. |
| **6. Outcome Alignment** | How does what the action actually produced compare with the expected result? | The tool wrote a document, but it is not understandable; a workflow was published, but successful execution is unverified. |

These examples are operational adaptations of the definitions you supplied. Action-Space asks whether the relevant alternatives and methods are in view. Action-Set asks whether the selected actions form an appropriate, feasible plan. The boundary can be uncertain; retain that uncertainty rather than force a label.

### Four pillars: make alignment inspectable

The supplied dependency chain is: **Alignment requires Comparison; Comparison requires Measurement; Measurement requires Visibility; Visibility requires Explicitness.** In practice, work from explicitness toward comparison, then iterate.

| Pillar | What the orchestrator does | Example: preserve a user’s removal during a rewrite |
| --- | --- | --- |
| **Explicitness** | State the reference expectation: the intent, constraint, relationship or result that should hold. | The provider question has been removed from this message. |
| **Visibility** | Expose the relevant actual state, including the AI’s interpretation, selected actions and resulting artifact. | Show the complete revised draft and retain the removal instruction. |
| **Measurement** | Describe the observed state in terms that can be checked against the reference. | Check whether the removed question appears, including a paraphrase. |
| **Comparison** | Identify agreement, a discrepancy or insufficient evidence, then choose the next intervention. | It has reappeared: restore the constraint and recheck the whole draft. |

Measurement need not mean a numerical score. It can establish whether a specified actor, source, condition, output or constraint is present, absent, different or still unverified. Numerical measures need defined units, populations and time windows. No generic “alignment percentage” is inferred from these records.

### The analytical unit is an alignment question

For each relevant intervention, preserve:

1. **Target and relationship:** which work, artifact or handoff is being checked, between whom, at what time.
2. **Reference:** what should hold, who or what establishes it, and whether that reference is itself agreed or provisional.
3. **Visible state and measurement:** what was available at that point and how it was examined.
4. **Comparison:** established match, detected mismatch, suspected mismatch or unresolved question; the relevant layers and why.
5. **Intervention:** what was requested, how it would establish or restore alignment, and what it might disturb elsewhere.
6. **Recheck:** what changed, what was actually verified and which alignments remain open.

Keep a user’s explicit reason distinct from an analyst’s explanation. Do not turn “check this” into “the user had already detected a failure.” Do not insert later discoveries into what was known before the intervention. The [alignment episode analysis](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/aligncraft-episode-analysis.md) applies this structure to 22 selected records, including successful checks, partial repairs and unresolved results. It does not label all 389 records.

### Alignment across people and agents

The same questions apply when a supervisor directs an AI, an orchestrator delegates to another AI, or operational work is handed to a colleague. Give the recipient the relevant context, task, available approaches, selected scope, constraints to preserve and expected result. On return, inspect the result and its effects on the wider work. A subordinate agent’s confident report is still a report; the evidence required depends on the claim.

**Framework source:** the AlignCraft explanation supplied by Enes in this conversation on 16 September 2026. The author’s [accessible book introduction](https://karaposu.github.io/alignstack/) currently uses the name AlignStack and presents the same six definitions and four pillars. This playbook retains the supplied name AlignCraft. The operational mappings and episode diagnoses below are our analysis.

## The operating cycle

### Before executing the task: make the orchestration explicit

Establish the task's purpose and examine its requirements through the five capabilities. Then create the task's initial `orchestration.md`: concrete action cards, their contribution to the outcome, dependencies and whether each can proceed now. Preserve provisional parts and the questions that would clarify them. The [working format](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-file-format.md) is the initial proposal for the next month of practice.

Use this file to make the next useful actions inspectable. Define immediate work sufficiently to proceed, while allowing later actions to become more specific as their inputs become available. Reuse established results rather than repeating work to populate the file.

### During execution: act, inspect and update

1. **Recognize the event and alignment question.** What changed, what is being questioned, and which layers might be affected?
2. **Make the reference explicit.** Recover the intended state and the sources that establish it; clarify it if necessary.
3. **Make the actual state visible and measurable.** Inspect the relevant context, interpretation, plan or result using suitable criteria.
4. **Compare and choose an intervention.** Decide whether to establish missing alignment, investigate uncertainty, repair a mismatch, preserve an existing alignment or continue.
5. **Act within the applicable scope and authority.** Use the relevant playbook move; anticipate effects on other established alignments.
6. **Recheck and reconcile.** Compare the resulting state with the expectation, assess disturbance elsewhere, and update the work, evidence and communications.

Maintain all six layers throughout the work. They are not six gates passed once at project start. A later action can reopen an earlier alignment. Keep checks proportionate to the situation, while retaining relevant unresolved questions instead of silently treating them as satisfied.

The cycle applies across asynchronous activities. One part of a task may wait for a response while another progresses. Retain the pending dependency, choose useful independent work, and consume returning information before deciding whether to resume, revise or redirect the affected work. After a consequential result, return or correction, update the affected cards, their dependencies, readiness and the next proposed action in the orchestration file. Preserve a short account of why the plan changed. The [concept notes](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/ai-operations-manager-concept-notes.md) explain this working direction and its month-long calibration.

### Minimum working state

The orchestrator should be able to explain these items without rereading the entire archive:

| Item | What must be clear |
| --- | --- |
| Outcome | What useful change or decision the work serves, and for whom. |
| Current work | What is being discovered, designed, decided, executed or verified. Different parts can be at different stages. |
| Evidence | What is observed, reported, inferred or unknown; sources, dates, entity identities and scope. |
| Applicable direction | Which instructions and decisions apply now, what they authorize, and what they supersede. |
| People | Who knows, performs, decides, supports or needs notification; the evidence for each role. |
| Dependencies | The exact input or event needed, who owns the next action, and what remains independently possible. |
| Artifacts | Where current understanding, detailed evidence, work tracking and operational records belong. |
| Next move | The proposed action, why it helps now, and what result would let work proceed. |
| Alignment state | The current questions at the six layers, their reference expectations, supporting evidence and unresolved discrepancies. |

For the next month of practice, maintain the relevant task-level state in `orchestration.md` and link to detailed sources or existing records. The [initial format](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-file-format.md) provides action cards and a current-position view. These information needs do not require a separate file or a mandatory field for every row above; the useful level of detail is part of the calibration.

## 1. Start or resume with reconciled context

**Use when:** taking up a new assignment, returning after a gap, changing sessions or inheriting work.

**Alignment being examined:** Workspace; Coherence when earlier decisions must survive the restart.

**Comparison to make:** Compare the resumed understanding with the latest applicable context and preserved decision history. Reading files supplies visibility; resolving contradictions establishes whether the working state is aligned.

Recover the assignment, recent decisions, current plan and relevant open conversations from the prepared context. Follow source links where summaries conflict or omit decisive detail. Preserve why the direction changed, and identify which earlier claims or instructions have been superseded. Check for relevant human actions outside the assistant's own tool history.

Then state where the work actually stands and choose a next action. A recent file date or a promise to read everything is insufficient: the understanding must agree with the newest applicable evidence.

**Check:** the resumed plan does not revive withdrawn recipients, completed asks, superseded scopes or invented dependencies. Keep useful historical reasoning identifiable as history.

**Evidence:** A handoff repeated obsolete archive scope and a departed contact; the next conversation consumed it and repeated the errors. Later checks also found direct human actions missing from the assistant's ledger. [ORC-0222](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:5865) [ORC-0223](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:5903) [ORC-0253](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:6616)

## 2. Choose the next move for the stage of the work

**Use when:** deciding what to investigate or do next, especially when the task remains unclear.

**Alignment being examined:** Task, then Action-Space and Action-Set.

**Comparison to make:** Compare the requested purpose and stage with the proposed work. First expose the appropriate kinds of action; then choose a feasible next set. Investigating unknown problems and executing a defined solution need different criteria.

Identify what is missing for the next meaningful advance:

- **Understanding:** establish the problem, actual process, relevant entities or meaning of a proposed step.
- **Decision:** prepare options, trade-offs and a recommendation for the person who can decide.
- **Execution:** carry out an established action and verify its result.

Discovery can legitimately begin before the exact problems or priorities are known. Give it a purpose, such as revealing operational gaps for prioritization. Do not require it to name the answer it exists to discover.

Choose work at the right level: deciding which project deserves effort differs from deciding the steps inside that project. Keep a view of major outcomes so small posting and housekeeping tasks do not obscure the purpose.

**Check:** the action produces something the current stage needs. If substantial effort would commit to one interpretation, create a small reviewable example or initial framing first.

**Evidence:** The user corrected a discovery method that assumed known problems, separated missing context from presumed fixes, and asked for the major remaining outcomes. A five-project sample exposed structure questions before the remaining nineteen were created. [ORC-0038](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:1071) [ORC-0053](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:1525) [ORC-0104](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:2833) [ORC-0108](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:2929) [ORC-0301](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:7763)

## 3. Investigate with a purpose and visible coverage

**Use when:** gathering context, checking a hypothesis or supporting a claim about the operation.

**Alignment being examined:** Workspace and Action-Space, with Action-Set for search selection.

**Comparison to make:** Ask whether the context is sufficient and whether relevant ways to obtain evidence are in view. Make searched and unsearched scope visible, then compare it with the premises needed for the next action.

State the question and the evidence that could answer it. Use the company source map, then follow actual relationships: a work item to its decision, a workflow to its inputs and outputs, a record to its consumers, a person to their stated role. Check existing mechanisms before designing replacements.

For comparisons, resolve exact identities, hosts, versions, time periods and populations on both sides. Similar names, stale exports, incomplete pagination and transformed text can create apparent defects. Check what an empty result means before interpreting it as absence.

**When to stop:** proceed once the next bounded action has adequate evidence for its material premises and the remaining uncertainty is explicit. If an unchecked source could change the action, target, scope or authority, inspect it or narrow the action. Record inaccessible or uninspected areas. Do not keep expanding a search merely because more information exists.

This stopping test is proposed guidance; the logs do not establish an optimal search budget or guarantee complete discovery.

**Evidence:** Existing documentation changed the proposed work; stale comparisons invalidated a handoff; a wrong response field manufactured missing replies; a table-based audit missed a live consumer without a row. [ORC-0080](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:2240) [ORC-0057](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:1636) [ORC-0190](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:5062) [ORC-0248](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:6501) [ORC-0303](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:7809)

## 4. Keep each claim within what its evidence establishes

**Use when:** interpreting sources, computing findings, writing status or making a recommendation.

**Alignment being examined:** The layer addressed by the claim; especially Workspace facts and Outcome claims.

**Comparison to make:** Make the claim and its evidence standard explicit. Inspect and measure the supporting state, then compare what the evidence establishes with what the wording asserts. Do not assign every unsupported statement to one layer regardless of its subject.

Distinguish direct observation, a person's report, an inference, an estimate, a proposal and an unknown. Attach those distinctions to the claim itself, especially when it enters another artifact.

Ask what was actually measured. A count of rows differs from a count of workflows or linked pairs. A configuration setting differs from observed execution; execution differs from useful output or business use. A recent edit does not establish who made a specific change. A missing result does not establish nonexistence.

If a proxy is useful, explain what it approximates and which comparison it can support. Avoid turning a range from two heuristics into a statistical confidence interval.

**Check:** the wording remains true if the reader opens the cited source. Summaries and published documents retain uncertainty that matters to their conclusions.

**Evidence:** Missing detector output became a justified 'not detected' category; a heuristic cost allocation was authorized but unvalidated; the daily auditor was configured but recent successful execution was unobserved. [ORC-0017](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:511) [ORC-0266](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:6929) [ORC-0289](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:7472) [ORC-0380](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:9780)

## 5. Let new context reopen the whole plan

**Use when:** a meeting, reply, direct check or user correction changes a material premise.

**Alignment being examined:** Coherence, potentially reopening any other layer.

**Comparison to make:** Compare the new evidence with the premises supporting existing decisions and artifacts. The intervention must restore the affected relationships, then check whether its own changes have disturbed other alignments.

Read enough of the source to understand the answer and its conditions. Match it to the correct earlier request, even if other work intervened. Reassess:

- The problem and intended outcome.
- Proposed options and the recommendation.
- Scope, order and dependencies.
- Roles and authority.
- Evidence, readiness and claims already communicated.
- Affected artifacts and work other people may now be doing.

The eventual edit may be small. Decide its size after assessing the impact. Propagate both the correction and its evidence status; copying an inference into several files does not make it stronger.

**Check:** the current plan and dependent records agree, and any necessary correction to prior recipients has a chosen route. Merely saving a meeting summary does not satisfy this check.

**Evidence:** Full colleague answers withdrew cost and activity claims; a delayed meeting changed permitted archiving and task order; an unfinished rubric had been promoted to approval throughout a design. [ORC-0143](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:3850) [ORC-0213](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:5642) [ORC-0285](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:7380) [ORC-0352](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:9053) [ORC-0384](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:9880)

## 6. Apply Semantic Formulation to develop and test the appropriate fit

> **Semantic Formulation is the work of developing a coherent answer, judgment or approach that fits a particular problem, purpose and context—using semantic calculation, integrating its results and testing the resulting whole.**

This is the adopted name for the capability previously called Design. Semantic calculation is the reasoning performed; Traverse supplies its structured method; Semantic Formulation develops the usable result, including integration and checks of the combined fit. It includes developing and testing the substance through investigation, comparison and critique.

**Use when:** a part of the work requires semantic calculation—an answer, interpretation, judgment or approach needs to be developed and tested for its fit with the problem, purpose and context.

> **Semantic calculation is the work of developing and testing an answer, interpretation, judgment or approach for its fit with a particular problem, purpose and context. Traverse is the structured method used to do that work.**

The orchestrator's trigger is **“This part of the work requires semantic calculation.”** It then specifies what needs to be worked out and what the result needs to fit. The calculation may itself establish the relevant dimensions, criteria or relationships—for example, how to compare two approaches or how to critique a proposal. The threshold for selecting the full Traverse process remains a separate question.

**Alignment being examined:** Task, Action-Space and Action-Set; Coherence and Outcome across the designed operation.

**Comparison to make:** Make the required operation explicit before selecting mechanisms. Expose alternative approaches and each proposed transition, check feasibility, then compare the resulting walkthrough with what another operator would need to carry it through.

### Focused calculation before assembly

The user's approach to Semantic Formulation is to identify work requiring semantic calculation, give it focused attention through Traverse, consume the findings and then compose the larger result. The subject may be the meaning of a requirement, the right technical approach, a data structure, a component relationship, a comparison or a critique. It needs attention because assembly would otherwise depend on working out its answer along the way.

For each selected inquiry:

1. Frame what needs to be worked out, what it needs to fit and why its answer is needed for the overall task. Include developing the basis for fit when that remains unresolved.
2. Supply the relevant environment, constraints, evidence and related design commitments.
3. Use the actual Traverse method for the inquiry; preserve its finding, assumptions and unresolved questions.
4. Compare the result with the requested fit before relying on it.
5. Revisit dependent gaps, then assemble the developed parts and check their combined coherence.

A missing fact may require retrieval or a colleague’s input, and an organizational choice may require the responsible decision-maker. Keep those dependencies visible while developing the design. Separate inquiries can affect each other; choose their boundaries accordingly.

**Existing capability:** the inspected local Traverse runner uses Articulate-Simple → Surfacing → Sensemaking → Decomposition → Innovation → Critique → Routelister → Conclude, with sequential saved handoffs and iteration. Routelister exposes possible onward routes; the surrounding orchestrator selects what to pursue. The [design concept notes](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/ai-operations-manager-concept-notes.md) distinguish the user’s reported experience, the inspected mechanism and the remaining integration questions. No new inquiry was run for this documentation update.

The role division is: **the orchestrator identifies and sequences work requiring semantic calculation; Traverse performs the structured calculation; the orchestrator integrates the findings and checks the whole.** The historical uses include question clarification, definitions, coverage maps, structures, methods, comparisons, critique, technical investigation and transferable principles. A completed inquiry can legitimately return better questions or a generic framework when that is the requested result.

### Brief the inquiry and assess its return

Use two descriptors: **what is unresolved** and **what treatment it needs**. The usage study distinguishes task framing, conceptual boundaries, coverage, purpose/consumers, structure, process, relationships, measurement/evidence, technical feasibility and choice/fit. Any of these may need defining, comparing, challenging, verifying, reframing or connecting to the wider work.

Before a run, make the question, intended use, requested depth and return type explicit. Include relevant context, constraints, earlier corrections and affected dependencies. During discovery, the purpose may be to expose unknowns; do not require an already-defined problem or decision before allowing useful investigation. The historical discovery inquiry had to correct precisely that mistake.

On return, check whether the result answers the actual question at the requested level; separate source observations, candidate designs and still-open assumptions; and identify what can use the finding now. A sample-planning framework can be a completed conceptual deliverable while a specific plan and prepared sample remain outstanding. Conversely, a proposed runtime guarantee needs behavior evidence before it becomes a verified capability.

Keep findings revisable. The card chain shows that applying a structure to a second and third concept can expose first-example bias and require changes to the template and sibling artifacts. A user correction can also reveal that a technically coherent answer missed the intended dimension. Reopen that framing and reconcile the dependent work, rather than adding more detail inside the old answer.

**Evidence:** the [taxonomy's inquiry chains and output distinctions](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-taxonomy.md) link to the exact cases. A recorded conclusion establishes availability of a finding; its conceptual fit, practical usability and any subsequent implementation are separate claims requiring suitable checks.

### Carry the assembled operation through

Walk through a concrete case from entry to its eventual outcome. Identify how work is noticed, selected, assigned, performed, judged, put into use, supported and revisited. At each transition, explain the actor, required input, decision, resulting record and next action.

Identify what requires semantic calculation before filling the document with mechanisms. For example: eligible for what, who decides, what exactly is being compared, what does a parallel run do, and what happens after a switch? Distinguish questions needing retrieval or a person's decision from those whose answer must be developed and tested; keep their dependencies visible.

Separate present capability from proposed additions and later improvements. Choose the smallest practical arrangement using existing practices, while explaining what must be added. A tool preference should follow the required job, operating constraints and alternatives.

**Check:** the assembled result retains the relevant findings and their constraints; conflicts or coupled gaps have been addressed or left explicit. Someone can follow the operating case without inventing an actor, handoff or success criterion. For a pilot, distinguish proving the method from validating a particular business outcome; transfer of a result needs its own justification.

**Evidence:** The manager rejected a framing that explained one evaluation but not its repeatable operation. Further work exposed undefined transitions and separated the pilot's methodological purpose from a deployment verdict. [ORC-0343](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:8827) [ORC-0348](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:8953) [ORC-0314](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:8084) [ORC-0330](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:8473) [ORC-0382](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:9830)

## 7. Choose people and questions from evidence

**Use when:** proposing outreach, assigning work or interpreting a colleague's answer.

**Alignment being examined:** Workspace for role evidence; Action-Set for the selected recipient and ask.

**Comparison to make:** Expose the evidence for a person’s knowledge, responsibility and authority. Compare it with what the proposed request requires. A recipient may be a useful starting point without being the sole owner or final decision-maker.

Explain why the communication is needed and why this recipient is appropriate. Separate knowledge of a mechanism, responsibility for operating it, implementation access and decision authority. A person mentioning a topic, editing a page or fixing one bug establishes only that involvement.

Answer what can reasonably be learned from available sources first. Give the recipient the remaining question, necessary context and the decision their answer will support. If their remit is unclear, discover it before sending detailed instructions. Respect existing ownership, while recognizing explicit reassignment or delegation when it occurs.

**Check:** every proposed ask has a useful purpose and a supported recipient. The message does not quietly ask a technical owner to settle policy or ask a fallback owner to reapprove work already delegated elsewhere.

**Evidence:** The user repeatedly narrowed questions to what colleagues could answer, challenged ownership assumptions and distinguished notification from additional approval. [ORC-0014](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:436) [ORC-0069](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:1951) [ORC-0194](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:5158) [ORC-0203](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:5402) [ORC-0287](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:7426) [ORC-0339](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:8699)

## 8. Manage asynchronous work and genuine dependencies

**Use when:** waiting for a response, planning a follow-up or refreshing the day's work.

**Alignment being examined:** Coherence and Action-Set; Outcome when verifying a requested result.

**Comparison to make:** Compare the recorded dependency with the actual send, reply and execution state. Updating a wait or choosing parallel work must preserve the current mandate and other commitments.

Track the exact question or action, its destination, whether it was sent, what response arrived and who currently owns the next move. Before nudging, check the correct conversation and any available operational result. The human may have replied directly; the requested work may be complete without acknowledgment.

Distinguish required input from helpful optional contribution. Continue useful independent work within the applicable mandate. If optional silence should no longer delay progress, make that a scoped decision; do not turn it into endorsement or reuse it as permission in another situation.

A future pulse should bring relevant changes into this same cycle, including indirect references and new decisions. Define the checks per task and context: what needs revisiting, which conversation or result to inspect, when or under which condition to check, and what a change could affect. Checks may follow an action, a response, a task-specific revisit condition or an appropriate interval. There is no selected universal cadence. Its source scope and coverage must be visible. A discrete sweep or a statement that the assistant is watching does not establish continuous monitoring.

For example, while a question to a colleague is pending, continue a Semantic Formulation inquiry that does not depend on the answer. When a relevant reply is detected, consume it alongside the current context, reassess the affected work and update the appropriate artifacts. The implications of the reply determine whether it should change the current focus or a later step.

**Check:** no one is described as blocking an unsent request; waits and urgency use real dates; new replies change the plan where needed.

**Evidence:** An unsent follow-up was incorrectly attributed to Jeremy; a proposed chase was withdrawn after completion evidence; bounded silence was explicitly allowed for optional contributors; a sweep recovered a managerial hold. [ORC-0073](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:2053) [ORC-0206](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:5474) [ORC-0249](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:6524) [ORC-0260](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:6791) [ORC-0335](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:8599)

## 9. Make alignment proportionate to the actual decision

**Use when:** direction, authority or the next commitment is uncertain.

**Alignment being examined:** Task and Action-Set, checked against actual authority.

**Comparison to make:** Make the applicable instruction and conditions explicit, inspect the proposed next action, and compare their scope. Preserve delegated authority as well as real limits; neither an unnecessary approval loop nor an unsupported assumption of approval restores alignment.

Return to the original request and later applicable decisions. Identify what is a suggestion, an example, a preference, conditional support, approval or an explicit hold. Preserve the scope and conditions of each.

Prepare enough concrete work for the decision-maker to assess the issue: the problem, useful alternatives, relevant trade-offs, recommendation and what following it would entail. Use an early artifact or example when that will reveal disagreement before a large investment.

Exercise authority already delegated. Ask when a material decision remains outside it; do not manufacture another approval layer from a title, a document location or a generic checklist. A request to prepare or announce a plan also needs interpretation within its actual scope.

**Check:** the next action matches the instruction's meaning. Discussion venue does not determine decision ownership, and silence is not assumed approval without an applicable agreed mechanism.

**Evidence:** Illustrative tiers were not mandated taxonomy; only part of a priority list was agreed; qualified support for keys carried a process prerequisite; an unnecessary fallback approval was removed. [ORC-0051](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:1442) [ORC-0067](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:1900) [ORC-0119](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:3195) [ORC-0316](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:8130) [ORC-0339](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:8699) [ORC-0354](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:9103)

## 10. Communicate so each audience can do its part

**Use when:** explaining work to the supervisor, drafting for colleagues or reporting to management.

**Alignment being examined:** Outcome for reader comprehension; Task for audience purpose; Coherence across revisions.

**Comparison to make:** Specify what the reader should understand or do. Inspect the complete message, identify missing referents and retained constraints, and compare it with that purpose. Recheck that improving one aspect has not undone a prior correction.

| Audience | What the communication must enable |
| --- | --- |
| Supervisor | Understand the situation, evidence, interpretation, options and consequences well enough to judge the proposal. |
| Person carrying out work | Understand the exact request, relevant objects, role, dependencies and how to return a useful result. |
| Manager | Understand the outcome, recommendation, trade-off, required decision or useful next step with an appropriate amount of detail. |

Keep the supervisor's explanation and evidence alongside the outgoing draft. They have different purposes and may have different lengths. Name the objects behind terms and counts; explain why a number matters. Preserve links to supporting detail when shortening.

Apply corrections to the whole relevant draft. Check active exclusions and human edits before sharing; shortening one artifact must not accidentally modify another. A platform character limit is not a test of reader comprehension.

**Check:** the reader can explain what happened or is proposed, why it matters and what response is needed without hidden conversational context. Do not claim a clarity pass verifies factual accuracy.

**Evidence:** Separate review context helped the supervisor understand an outgoing draft; a recipient requested a much shorter post; compression removed an evidence link; a later rewrite restored a question the user had explicitly deleted. [ORC-0176](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:4705) [ORC-0183](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:4873) [ORC-0232](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:6112) [ORC-0233](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:6135) [ORC-0329](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:8436) [ORC-0381](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:9805) [ORC-0386](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:9930)

### The accompanying evidence note

Your design requires evidence alongside communication to the supervisor. A compact candidate format is:

> **Alignment question and reference:** What should hold, at which layer, and why that is the applicable expectation.  
> **Observed state and evidence:** What we can inspect, with source links, dates and the criteria used.  
> **Comparison:** What agrees, what differs and what remains unknown; separate observation from interpretation.  
> **Proposed intervention:** The next action, why this action or recipient fits, and which existing alignments it could affect.  
> **Recheck:** What result would show the issue is resolved, and any remaining uncertainty.

For routine updates, this can be short or link to a maintained record. It should expose the basis of judgment without copying the full investigation into every message. The format is proposed; the need for traceability comes directly from your concept.

## 11. Execute concrete actions and reconcile uncertain outcomes

**Use when:** making an authorized change, publishing, sending or recovering from an interruption.

**Alignment being examined:** Action-Set, Coherence and Outcome.

**Comparison to make:** Check that the concrete action is feasible and within scope, identify what it must preserve, then compare the actual destination or behavior with the intended effect. An uncertain receipt calls for investigation before another side effect.

Establish the exact target, intended change and relevant current state. Confirm the needed capability and access before relying on the plan. For shared or staged work, reread the destination where intervening edits would matter and preserve the human's changes. Apply a bounded operation with a suitable recovery route.

After a tool error, distinguish a failed action from a failed receipt or failed verification. Check the destination before retrying a consequential write. For batches, retain separate completion and exception states.

**Check:** verify the actual destination and intended content or configuration. If claiming operational success, obtain behavior evidence as well. A published version can be confirmed while a successful run remains outstanding.

**Evidence:** Readback prevented a duplicate after a model error; another send created a duplicate when verification failure was mistaken for write failure; the later lesson was applied successfully. Staged workflow publication verified version IDs but did not establish runtime success. [ORC-0170](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:4540) [ORC-0232](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:6112) [ORC-0251](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:6570) [ORC-0283](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:7334) [ORC-0370](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:9523)

## 12. Maintain artifacts for their readers and future use

**Use when:** creating a deliverable, recording a decision, revising a shared draft or persisting context.

**Alignment being examined:** Coherence and Workspace, with Outcome for delivery and retrieval.

**Comparison to make:** Make each artifact’s role and current authority explicit. Compare local, published and historical states with the decisions they represent. Matching copies establish synchronization, not factual correctness or future usefulness.

Choose the artifact's job and its expected home. Detailed evidence, current work tracking, recipient summaries and lasting facts about operational entities may need different views. Keep them connected through stable identities and source links.

Preserve meaningful history and identify the current version. When copying or publishing, distinguish factual freshness from synchronization: copies can match and still be wrong. Keep an existing review location when continuity matters, and reread live human edits before updating it.

Retain one work item when its intended outcome continues but its implementation route changes. Record why the route changed. Avoid creating a new document merely because drafting is easier than updating the established one.

**Check:** future readers can find the decision through the relevant work or entity, understand its scope and see what superseded it. Use the company's established homes; the evidence does not require universal Airtable or Linear adoption.

**Evidence:** Journal audits exposed both stale facts and publication drift; a cost issue was reopened when the outcome remained unfinished; the manager emphasized connected operational records beyond temporary work tracking. [ORC-0156](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:4183) [ORC-0258](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:6745) [ORC-0363](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:9349) [ORC-0376](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:9673) [ORC-0378](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:9730) [ORC-0379](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:9755)

## 13. Close against the intended outcome

**Use when:** declaring work done, closing a ticket, reporting readiness or handing over support.

**Alignment being examined:** Outcome, with Coherence for remaining commitments and support.

**Comparison to make:** Define what completion means for this scope. Measure the achieved state against that definition and retain the uncompleted tail. Closing a work item must not erase operational responsibility or imply unverified effects.

Return to the outcome and the scope actually owned. Separate preparing a proposal, obtaining a decision, requesting execution, completing a change and verifying its effect. Close the bounded work that is complete while preserving named remaining verification or operational responsibility.

For an operation that will keep running, identify who supports it, what shows it remains useful, and what would prompt reassessment. Keep a no-change decision with its reason when that is the useful outcome.

**Check:** 'done' names what is done and is supported by appropriate evidence. Repairing a document, updating a board or receiving a positive message cannot substitute for the business result.

**Evidence:** The user challenged 'complete' when record quality remained deficient; a scoped retention ticket closed while longer-term verification remained; fixing the account of work was distinguished from completing it. [ORC-0211](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:5594) [ORC-0259](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:6768) [ORC-0264](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:6883) [ORC-0364](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:9374)

## 14. Turn corrections into scoped learning and check for recurrence

**Use when:** the same failure repeats or a correction appears useful beyond one sentence.

**Alignment being examined:** The layer of the original issue, plus Coherence and Outcome for retained learning.

**Comparison to make:** Make the correction and its scope explicit. Check the next relevant output against it and against other active expectations. A rule written to memory is an action; reliable application is a separate outcome.

Preserve the original output, correction, situation and resulting change. Identify the underlying failure, then formulate a rule with a scope and a checkable behavior. Apply it to the current artifact and relevant future examples.

Do not infer that a saved instruction has changed behavior. Check whether the next output retains the correction and still satisfies the other requirements. Keep exclusions and prior human edits active across rewrites. Revise a generalized rule if it conflicts with later needs; one manager's reaction does not establish a universal communication law.

**Check:** the next relevant case improves without reintroducing a removed premise, creating an unnecessary approval, or sacrificing another material constraint.

**Evidence:** A saved ambiguity rule failed immediately on another phrase; source-backed correction collections were later reused; broad managerial rules nevertheless overgeneralized local feedback; a deleted question returned during a clarity rewrite. [ORC-0179](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:4777) [ORC-0198](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:5254) [ORC-0333](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:8549) [ORC-0334](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:8574) [ORC-0345](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:8878) [ORC-0386](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:9930)

## Three worked examples

### A. A colleague appears not to have answered

**Alignment reading:** Workspace evidence was misread, creating an Action-Set problem: a reminder was proposed on a false premise. Explicitness identifies the actual response sought; visibility exposes the correct thread; measurement checks the returned replies; comparison determines whether waiting is real.

**Situation:** The work list says a definition is waiting on a colleague.

**Orchestration:** Open the correct thread and validate the response format. Check whether the answer addresses the original question, then update the draft and dependency state before deciding whether another message is useful.

**Historical lesson:** The parser read the wrong field and manufactured an empty response set. Replies had already arrived. Sending a reminder would have acted on a tool interpretation error. [ORC-0248](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:6501)

### B. New management context arrives after a plan is written

**Alignment reading:** The manager’s required deliverable exposes a Task mismatch and changes the relevant Action-Space and Action-Set. Coherence requires reconsidering the work already built around the earlier interpretation. Compare the revised framing against the operating transitions the manager needs to understand; a document write alone does not establish Outcome alignment.

**Situation:** A substantial proposal is ready, but the manager explains that it lacks the repeatable operating process.

**Orchestration:** Reinterpret the required deliverable, pause work that assumes its acceptance, walk through a concrete operating case, preserve genuine questions and revise the established review artifact. Explain the change in a form the manager can use.

**Historical lesson:** The substantive gap changed the work direction. Later positive feedback followed a revised framing and usable summary, but the exact method and subsequent sequencing still needed discussion. [ORC-0343](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:8827) [ORC-0375](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:9649) [ORC-0381](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:9805) [ORC-0388](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:9980)

### C. A tool errors after a message may have been sent

**Alignment reading:** Outcome alignment is uncertain, rather than disproven by the error. Make expected delivery explicit, inspect the destination, check the complete message and compare it with the intended post. That check protects Coherence by avoiding a duplicate when the first action succeeded.

**Situation:** The assistant's turn fails and the supervisor believes the update was not posted.

**Orchestration:** Inspect the destination, resolve any message formatting or continuation differences, then retry only if the outcome warrants it.

**Historical lesson:** The message had been delivered despite the failed turn. In a different episode, retrying after failed verification produced a duplicate. A later recovery successfully used readback before retrying. [ORC-0170](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:4540) [ORC-0232](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:6112) [ORC-0251](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:6570)

## What this adds to the original concept

The seven concepts still provide a useful organizing model. AlignCraft now provides the diagnostic foundation across them. The historical actions can be read as attempts to establish alignment, expose it for comparison, question it, repair it or preserve it as work changes:

| Original concept | More specific responsibility exposed by the episodes |
| --- | --- |
| Context accumulation | Reconcile versions, verify identities and populations, and retain the limits of discovery. |
| Semantic Formulation | Recognize work requiring semantic calculation, use focused Traverse inquiries to develop and test the appropriate fit, and integrate their findings into a coherent result whose parts fit each other and the environment. |
| Communication | Justify the recipient and action, preserve audience context, and distinguish review evidence from outgoing text. |
| Artifacts | Maintain a current view plus history; propagate changed premises; connect decisions to the entities they affect. |
| Alignment | Apply Workspace, Task, Action-Space, Action-Set, Coherence and Outcome checks through Explicitness, Visibility, Measurement and Comparison. Authority is one relevant consideration, rather than the full meaning of alignment. |
| Pulse | Recognize relevant changes and reconcile them with active work and open requests. Cadence and implementation remain open. |
| Orchestration | Select the next useful action, manage asynchronous dependencies, verify effects, repair mistakes and learn from recurrence. |

These responsibilities need not become separate agents. The playbook specifies behavior; architecture remains a later decision.

## How to use and improve this first version

For the next month of supervised practice, give AI the assignment, company context and its actual authority. Develop the capability view and then the initial orchestration file before task execution. Use the action cards to inspect the proposed coordination and choose useful work. During execution, retain the alignment cycle and update the file when results, returns or corrections change the plan. Preserve both the current position and the meaningful history so the month can calibrate the format and the coordination behavior it represents.

Useful checks include:

- Is the reference expectation explicit and supported, rather than invented by the orchestrator?
- Does the analysis distinguish a preventive question, a confirmed mismatch and an unverified outcome?
- Are the layer diagnosis and intervention justified by the episode, including effects on other layers?

- Does new evidence change all affected work, rather than just a summary?
- Are fewer unnecessary questions, reminders and approvals created?
- Does the supervisor understand recommendations without repeatedly reconstructing their references?
- Do corrections survive later rewrites and resumed sessions?
- Are completion claims supported at the level they assert?

These are proposed evaluation questions, not measured improvements from this analysis. A historical next action is evidence to assess, not an automatically correct answer.

### Still open

- Calibrating the operational interpretation of the six layers, particularly the Action-Space/Action-Set boundary.
- Connecting Traverse to the orchestrator: detecting and scoping gaps, managing dependencies, choosing when to assemble and checking fit across findings.
- The actual boundaries of autonomous action and escalation.
- How to store, refresh and retrieve the minimum working state reliably.
- How detailed the orchestration cards should be, how to express provisional work and readiness, and which file fields prove useful during real tasks.
- How to present evidence notes with enough detail and little repetition.
- Pulse sources, task-specific triggers and revisit timing. The earlier general 30–60 minute framing is superseded by context-dependent checks; the actual schedules and detection mechanisms remain to be designed.
- Whether these rules transfer to the remaining Codex material, other projects and new work.

The unreviewed Codex material continues the same project and may overlap these episodes. It can challenge this synthesis, but it should not automatically be treated as an independent test set. Keep related episodes together and hide later outcomes when testing a decision at an earlier point in time.

**Next development step:** use the initial orchestration-file format on real tasks during the proposed month, preserve meaningful changes and refine the format and coordination rules from that experience. The 22 historical alignment readings remain supporting material. Use actual observations to establish which parts of the working approach have become more dependable and which still need refinement.





------



# Orchestration file: working format

**Version 0.1 · 17 September 2026 · Initial format for calibration through real tasks**

## Purpose and position in the framework

An `orchestration.md` file makes the coordination of a particular task explicit. It shows what to do, why each action matters, what it contributes to the intended outcome, what it depends on and whether it can proceed now. It preserves uncertain parts as uncertain and changes as the work produces new understanding.

The working approach is:

**Understand the task → examine its requirements through the five capabilities → create the initial orchestration file → perform suitable actions, check their results and revise the file.**

The capability view establishes what the task requires from Context Accumulation, Communication, Semantic Formulation, Artifacts and Pulse. The orchestration file connects those requirements through concrete actions. An action can use several capabilities; numbering actions gives them stable identities, while their dependencies determine the order in which they can proceed.

For the proposed month of practice, Enes and AI will use this file while carrying out real tasks. The format, level of detail and maintenance rules will be calibrated through that use. The fields below are an initial proposal implementing Enes's requested view, rather than a final schema.

## What one file contains

Place `orchestration.md` with the task's existing working material. Maintain one current file for that task and link to detailed sources and deliverables where they already live.

### 1. Task and intended outcome

State what the task is trying to achieve, what result is required and the relevant scope or constraints. Link to the capability analysis and source context when available. Keep assumptions and unresolved questions identifiable.

### 2. Current position

Give the reader a compact view of:

- actions that can proceed now;
- actions waiting for a particular result or event;
- parts requiring clarification;
- the next proposed action or actions and why they are useful now;
- the latest material change to the plan.

This is a view of the action cards below. It should remain consistent with them. A short index table can provide navigation without repeating their full explanations.

### 3. Action cards

Each card describes a meaningful action at the level needed to direct the work. The following fields are the proposed starting set:

| Field | What the reader should understand |
|---|---|
| **ID and title** | A stable reference, such as A01, and a concrete action. |
| **What to do** | The action's actual scope. Broad instructions such as “do context” need to identify the question and relevant subject. |
| **Why it matters / contribution to the outcome** | What progress the action would make and why that progress is needed for this task. |
| **Expected result** | The understanding, answer, change or artifact the action should produce, and what would establish that result. |
| **Capabilities involved** | Which capabilities contribute to the action. These explain its role in the framework. |
| **Depends on** | The specific result, input or event needed. Reference another card by ID and explain the required contribution. Identify external dependencies explicitly. |
| **Can it proceed now?** | Yes, no, partly or uncertain, with a reason grounded in the current situation. For “partly,” name the independent portion. |
| **How well defined is it?** | What is clear, what is provisional and what remains unresolved. Explain what would clarify the uncertain part. |
| **Progress and actual result** | What has been attempted or completed, what actually resulted, and a link or other basis for that account. Leave future results unstated. |

“Why it matters” should connect the action to this task's outcome. It should not be a generic explanation of why research, communication or documentation is useful.

The expected result need not be a new document. It can be an established fact, a resolved interpretation, an answer from someone, a corrected draft or a verified outcome.

### 4. Relationships between actions

Make dependencies readable both in the cards and in a compact relationship view when the task warrants one. For example:

```text
A01 and A02 can proceed independently.
A03 needs the current-state account from A01 and the supported rationale from A02.
A04 needs the account developed in A03.
If A04 exposes an unsupported claim, revisit the relevant source or interpretation.
```

This is an illustration of the representation, not a plan for an active task. A graph is optional. The essential content is the relationship and its reason.

Distinguish a necessary dependency from a preferred order. If two actions could proceed independently but one is more useful first, explain that choice rather than recording a false dependency.

### 5. Material changes and results

Keep a compact history of changes that affect understanding or coordination. Record what changed, which cards were affected, why, and the relevant source, result or human correction. Preserve enough of the previous expectation to understand the change later.

This history should distinguish a proposal made by AI, a direction supplied by Enes, what was actually done and what was learned afterwards. A later explanation must remain identifiable as later.

Minor wording edits need not each become a history entry. Split, replaced or abandoned actions should retain a short route from their original IDs to the actions that supersede them.

## Representing work that is still unclear

The initial file can contain actions at different levels of definition. Specify the immediate useful actions sufficiently to carry them out. Describe later work provisionally where its details depend on what those actions reveal.

For an uncertain part, record the question or condition that prevents greater specificity. Identify a clarification or investigation action when that would make progress possible. Where the route depends on a future result, state the condition and leave the later route open until there is a basis for choosing it.

Three distinctions matter:

- **A well-defined action may be waiting.** Its scope is clear, but a necessary input has not arrived.
- **A provisional action may be partly possible.** Observations can sometimes be collected before the basis for interpreting them is settled.
- **An unclear part may have a clear next inquiry.** Establishing what is unknown is useful progress even when the final approach cannot yet be specified.

Readiness and definition should therefore be explained separately. More detail becomes justified as the work progresses; later cards can be added, split, revised or retired. The record should also permit new information to reopen an earlier assumption.

## Maintaining the file during execution

Use the current file to select the next useful action. After a consequential action, returned answer, discovery or correction:

1. Record what actually became known or changed, with an appropriate source or result reference.
2. Compare that result with what the action was expected to establish.
3. Reassess affected dependencies, readiness and provisional assumptions.
4. Revise, add, split or retire cards where the new understanding warrants it.
5. Update the current position and explain the next useful move.

The amount of updating should follow the significance of the change. The file supports the work; maintaining it should not require Enes to become a full-time recorder.

For a waiting dependency, include the source or event that would resolve it and what should prompt another check. Pulse brings a relevant return into the work; Context Accumulation interprets it; Orchestration updates the affected actions. Describing a check does not establish that a scheduled monitor has been created.

## Starting template

The template is deliberately editable during the practice period. Fill it with the task's actual meaning and known state.

```markdown
# Orchestration: [task name]

## Task and intended outcome

[What we are trying to achieve, the required result and relevant boundaries.]

Related context and capability analysis: [links]

## Current position

- Can proceed now: [card IDs and short reasons]
- Waiting: [card IDs and exact missing results or events]
- Needs clarification: [card IDs and unresolved questions]
- Next proposed action: [ID, action and reason]
- Latest material change: [what changed and why]

## Action cards

### A01 — [concrete action]

- **What to do:** ...
- **Why it matters / contribution to the outcome:** ...
- **Expected result:** ...
- **Capabilities involved:** ...
- **Depends on:** [card IDs and the required results, external condition, or none established]
- **Can it proceed now?** [yes / no / partly / uncertain, with the reason]
- **How well defined is it?** [what is clear, provisional or unresolved]
- **Progress and actual result:** [current progress; result and evidence when available]

## Relationships

[Which actions depend on which results, what can proceed independently,
and where the route depends on information not yet available.]

## Material changes and results

| When | Affected cards | What changed | Reason or evidence |
|---|---|---|---|
```

## What the month of practice should calibrate

For each real task, create the initial file, use it to coordinate the work and preserve meaningful changes as the task develops. Periodically improve the format when its use exposes a concrete problem. At the month's review, examine:

- Whether the cards identified useful actions at an appropriate level of detail.
- Which dependencies were missing, unnecessary or misunderstood.
- Whether readiness explanations supported sensible choices about what could proceed.
- How provisional parts became clearer, and whether important uncertainty was concealed too early.
- Whether new results changed all affected cards and the next action appropriately.
- Which fields helped Enes understand and direct the work, and which added maintenance without helping.
- Which corrections or choices still depended on Enes's judgment.

Use those observations to refine both the file's format and the rules for creating and maintaining it. The desired outcome is a more trustworthy way to represent and conduct orchestration, with the confidence earned by the work actually observed.

## How this contributes to automation

The file gives a future AI orchestrator a persistent account of the task's intended outcome, possible actions, dependencies, current readiness, uncertainty and results. It gives Enes a visible account of the coordination the AI proposes and performs.

Automation would use that account repeatedly: select a suitable action, carry it out within the task's scope, inspect the result and update what can happen next. The month of practice develops the representation and the coordination behavior together. The eventual runtime and extent of autonomous execution remain separate implementation questions.

## Framework references

- [Main concept notes](ai-operations-manager-concept-notes.md)
- [Orchestration playbook](orchestration-playbook-v1.md)
- [Automation development priorities](automation_ladder.md)


# Automation ladder

**17 September 2026 · Working implementation priorities for the AI operations orchestrator**

## Purpose

Order the development of the capabilities needed to automate the orchestration Enes currently supplies. The order reflects his main pain point, the recurring interventions in the reviewed work logs and the capabilities already available.

This is a priority order for development, not a ranking of the concepts' overall importance. It does not specify a technical architecture or implementation schedule.

## Priority order

| Priority | Capability | Why it belongs here | What the automation needs to handle |
| --- | --- | --- | --- |
| **1** | **Communication** | Enes identifies communication as his largest source of misalignment and repeated intervention. | Explain the situation to the supervisor with supporting evidence; prepare communications suited to their recipients and purposes; preserve intent, constraints and corrections through revisions. |
| **2** | **Context Accumulation** | The reviewed logs repeatedly show stale information, unresolved contradictions and new information failing to change subsequent work. Communication depends on an accurate account of the situation. | Retrieve relevant context, interpret it, distinguish its evidence status, reconcile changes and retain the current account across sessions and artifacts. |
| **3** | **Pulse** | Enes often supplied the prompt to check replies, revisit dependencies or notice changed circumstances. | Identify what each task needs checked, with timing or triggers suited to the context; notice responses and changed outcomes, and bring them back into the work. |
| **4** | **Artifacts** | Generating artifacts is a lower immediate priority than communication and reliable context. It is a capability that can be developed further once those needs are clearer. | Produce, place, link and maintain useful records and deliverables. Basic records are needed earlier; broader artifact automation can follow. |
| **5** | **Semantic Formulation integration** | Traverse already supplies a structured method for semantic calculation. The remaining automation work concerns when to use it and how to consume and combine its results. | Identify work requiring semantic calculation, prepare suitable inquiries, select subsequent work, integrate findings and test the combined fit. |

## Why Context Accumulation is the second priority

The recurring problem was broader than failing to find information. Enes repeatedly had to make the AI consume relevant context, interpret what it changed, discard outdated conclusions and carry corrections into subsequent work.

The common pattern was:

> The AI had received or read the information, but its account of the situation—and what it proposed next—had not reliably caught up.

### Evidence from the reviewed logs

| Recurring failure | Recorded example |
| --- | --- |
| **Using stale context to recommend a current action** | The AI compared fresh workflow data with a sixteen-day-old table export and prepared a handoff about problems that had partly already been repaired. Enes's challenge changed the investigation and stopped that handoff. [ORC-0190](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:5062) |
| **Reading context without reconciling it** | A resumed conversation read many files but repeated superseded scope, an outdated recipient and questions that were no longer unanswered. [ORC-0223](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:5903) |
| **Promoting a proposal into an established fact** | The AI treated an unfinished moderation rubric as approved and used that assumption to claim readiness. Enes corrected both its status and the conclusions depending on it. [ORC-0352](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:9053) |
| **Failing to preserve a changed direction** | After consuming a meeting and recognizing major changes to the plan, later summaries returned to older decisions and worklists. [ORC-0213 and continuation](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence.md:5642) |

Reliable Context Accumulation therefore includes acquisition, interpretation, reconciliation, retention and use. Reading more files alone does not establish that the current working account is correct.

## Communication and context must develop together

Several communication failures began with an incorrect account of the situation. A clearly written message can still ask an answered question, attribute responsibility incorrectly or present a draft as an agreed decision.

The first communication automation needs enough context support to establish:

- What happened, according to which source?
- What is agreed, proposed, disputed or still unknown?
- What has changed since the previous account?
- Which conclusions, communications and next actions must change with it?

The ladder orders where to focus development effort. The initial communication capability still needs the context and records required to work reliably. Similarly, Semantic Formulation can be integrated later because Traverse already exists, while its use continues to require suitable context.

## Orchestration and Alignment apply throughout

**Orchestration** coordinates the capabilities asynchronously. A task can be waiting for a person's answer while independent Semantic Formulation or artifact work continues. When the answer arrives, the orchestrator ensures it is consumed, reassesses its implications, updates affected artifacts and resumes or redirects the relevant work. It retains the relationship between active work, waiting dependencies and returning information.

**Alignment** checks whether the context, task interpretation, available approaches, selected actions, effects on other work and actual outcomes fit the relevant expectations. AlignCraft provides the six layers and four pillars for these checks.

Both apply from the beginning of the ladder. Their detailed automation can develop alongside each capability.

The proposed practice now includes an explicit task-level `orchestration.md` from the start. This minimal working artifact makes actions, dependencies, readiness and provisional parts visible while the framework is used. Broader artifact automation remains the fourth development priority; the orchestration file is the record needed to coordinate and learn from the work now.

## Pulse depends on the task and context

Pulse includes checking for responses and revisiting the outcome of earlier actions. Its timing and triggers depend on what is being checked and why. There is no selected universal “every five minutes” or “every thirty minutes” cadence.

For each task or subtask, identify what needs another check, the relevant source or result, when or under which condition to check, and what a change could affect. Pulse detects a relevant development; Context Accumulation interprets and reconciles it; Orchestration decides whether it calls for communication, artifact updates, further Semantic Formulation or another action.

## Working direction for task automation

Enes is exploring an approach that first decomposes a task or subtask into its requirements for the five capabilities:

1. What context is needed, and which contextual questions need answering?
2. What must be communicated to the supervisor and to other people, for which purposes and in what form?
3. Which artifacts are required, and what should cause their creation or revision?
4. Which checks or returns does the task need, with what context-dependent timing or triggers?
5. What requires Semantic Formulation?

On 17 September, applying this view to a task exposed the need for a further step before execution: create an evolving **orchestration file** that turns those requirements into concrete action cards and relationships. Each card explains what to do, why it advances the task, what it depends on and whether it can proceed now. Some parts can be defined while others remain provisional and become clearer as results arrive.

The proposed month of practice will use these files while carrying out real tasks, preserving meaningful changes and calibrating their format, action granularity, dependency descriptions and updating behavior. The [initial format](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-file-format.md) is a starting proposal; the [main concept notes](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/ai-operations-manager-concept-notes.md) explain its role in future automation.

This task-level practice is distinct from the ladder's order of capability development. The five capabilities contribute to the work as needed; the orchestration file represents how their actions depend on one another and change over time.

## Basis and limits

- Communication first is Enes's stated priority and reported experience. His estimate that communication accounted for about 80% of misalignment is a personal estimate, not a measured result from the corpus.
- Context Accumulation second is a qualitative judgment supported by recurring reviewed episodes. The full set of interventions has not been classified by capability to establish a frequency ranking.
- The general orchestration study contains 389 records from 358 reviewed transcript windows, plus the initial source segment. Records include ordinary progress, preventive checks, failures and recoveries; related records may describe the same evolving work.
- Pulse, Artifacts and Semantic Formulation integration follow as the working implementation sequence accepted in this discussion. Their relative positions are development choices, not demonstrated differences in failure frequency.

## Related documents

- [AI operations manager concept notes](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/ai-operations-manager-concept-notes.md)
- [Orchestration playbook](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-playbook-v1.md)
- [Orchestration evidence index](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/orchestration-evidence-index.md)
- [Traverse usage taxonomy and Semantic Formulation vocabulary](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-taxonomy.md)


---


# How you use Traverse: an evidence-based taxonomy

**16 September 2026 · Historical study, agreed Semantic Formulation vocabulary and candidate guidance for the future orchestrator**

## Agreed vocabulary: Semantic Formulation, semantic calculation and Traverse

> **Semantic Formulation is the work of developing a coherent answer, judgment or approach that fits a particular problem, purpose and context—using semantic calculation, integrating its results and testing the resulting whole.**

Semantic Formulation is the adopted name for the operating-model capability previously called Design. It includes developing and testing the substance of the result through investigation, comparison and critique, as well as integrating findings. A definition, judgment, framework or operating model can each be the result.

> **Semantic calculation is the work of developing and testing an answer, interpretation, judgment or approach for its fit with a particular problem, purpose and context. Traverse is your structured method for doing that work.**

You introduced “semantic calculation” after reviewing this study and accepted this definition. It names the activity that connects the different uses: working through meanings, relationships, possibilities and consequences to develop and test an appropriate fit. Technical investigation, process design, comparison, critique and relating things can all involve semantic calculation.

This refines the earlier framing around “meaning gaps.” You rejected “understanding gap” as too broad: missing understanding may simply require retrieving context. Semantic calculation is required when an answer, approach or basis for judgment still needs to be developed and tested using the relevant context. Retrieval and empirical investigation can supply inputs and checks within that work.

**The calculation can also establish what “fit” should mean.** The relevant dimensions, criteria or relationships may need to be worked out before candidates can be evaluated. For a comparison, that includes deciding which dimensions make the comparison meaningful. For a critique, it includes establishing which criteria and challenges would reveal whether the proposal fits.

- **Capability:** Semantic Formulation—the broader work of developing a usable result, integrating findings and checking their combined fit.
- **Activity:** semantic calculation.
- **Method:** Traverse.
- **Aim:** develop and test the appropriate fit.
- **Orchestrator trigger:** “This part of the work requires semantic calculation.”

The orchestrator then specifies what needs to be worked out and what the result needs to fit. The threshold for choosing the full Traverse process remains a separate design question. This is the agreed conceptual definition for the operating model; the historical cases and classifications below remain retrospective evidence and analysis.

## What the historical study contributes

The history shows how semantic calculation is used to define concepts, design processes and artifacts, choose technical approaches, investigate feasibility, challenge previous conclusions, connect components and decide which question deserves attention next. Its return can be a better question, a definition, a taxonomy, a framework, a specification, a grounded judgment or a technical finding with explicit limits.

The most useful classification therefore has two dimensions:

1. **What needs to be worked out?** The subject of the calculation, including the problem, purpose and context it must fit.
2. **What do you want Traverse to do about it?** Define, enumerate, compare, challenge, verify, reframe, design, connect or generalize.

For example, “skill complexity” is a subject. Defining complexity, checking whether it can be measured, challenging an earlier answer and designing a composition analyzer are different uses. Your history contains all of them.

## Evidence and scope

The [full catalogue](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md) documents **77 inquiry attempts**, with a question, context, output, continuation, limitation and transcript references for each.

| Start period | Claude Code | Codex | Attempts | Reached a documented finding |
| --- | ---: | ---: | ---: | ---: |
| 1 August–16 September | 25 | 3 | **28** | **25** |
| Earlier July history | 49 | 0 | **49** | **48** |
| Total | **74** | **3** | **77** | **73** |

One July inquiry resumed and concluded in August; it is counted once by its start date. The four remaining attempts paused, failed to launch or were restarted. **These are completion counts, not success rates.** Several completed findings were subsequently corrected.

Discovery covered 88 local Claude/Codex JSONL files, approximately 520.7 MB. Each recovered inquiry received a contextual review; unrelated turns were not all reread. Copied records, resumptions, skill reviews and mentions in work updates were distinguished from fresh inquiries. All 105 human candidate rows were reconciled. The [structured data](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-study-data.json) preserves full recovered requests, classifications, source hashes and the search ledger.

**Coverage limit:** the OpenAI evidence is Codex history. No separate ChatGPT web export was located. This is a catalogue of recovered uses in the available archives, not a guarantee about deleted logs, other devices or unexported conversations.

The categories and orchestrator recommendations below are retrospective analysis. They are grounded in these cases but are not a claim that you explicitly named every category at the time or that this one user's history exhausts possible uses.

## 1. Ten subjects of semantic calculation

These families describe **what needs to be worked out**. They can overlap. The historical catalogue retains its G1–G10 gap-family tags, with one primary tag for navigation and optional secondary tags. The labels describe the subject; semantic calculation names the activity.

| Family | The unresolved question | What resolving it can produce | Historical examples |
| --- | --- | --- | --- |
| **G1 · Task intent and framing** | What are we actually trying to understand? What stage, depth and deliverable does this request require? | A corrected question, scope, stage declaration or useful set of follow-up questions. | Interpreting a management request before research; correcting a decision-stage gate imposed during discovery; asking better questions about a surprising score. [T049](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1227) [T063](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1547) [T037](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:951) |
| **G2 · Concept meaning and boundaries** | What is this thing? What belongs to it, and how is it different from adjacent things? | A definition, distinctions, conceptual model and boundary cases. | Benefit versus Outcome; audit versus evaluation layer; a general ruler versus a local ruler; a definition artifact versus the runtime that judges. [T010](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:330) [T039](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:997) [T076](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1848) [T047](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1181) |
| **G3 · Coverage and variation** | Which kinds, dimensions, cases or perspectives are missing? Do the categories cover what matters? | A taxonomy, coverage map, catalogue, alternative views or documented omissions. | Benefit paradigms, harm categories, the SkillOps map and benchmark-check attributes. [T021](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:583) [T023](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:629) [T029](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:767) [T050](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1252) |
| **G4 · Purpose and useful consumption** | What is this for? Who uses the result, and what useful change can follow? | Use situations, consumer relationships, a rationale or near-term benefit opportunities. | What scores are for; compare/decide/watch/show; how conceptual knowledge becomes useful profiles; immediate uses of existing evaluation work. [T038](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:974) [T035](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:905) [T024](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:652) [T040](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1020) |
| **G5 · Structure and output contracts** | What must this artifact contain? How should its parts be arranged and expressed? | Sections, fields, schemas, templates, examples and a definition of the returned output. | Axis-card structure, design-file contents, task-to-methodology output and general-ruler sections. [T003](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:169) [T031](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:813) [T069](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1683) [T077](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1871) |
| **G6 · Method and operating process** | How does the work happen? In which sequence, through which handoffs, with what repetition and stopping conditions? | A procedure, cycle, scenario walkthrough or staged operating model. | Method refinement; the missing judging process; daily discovery work; the model-evaluation operation from intake through live use. [T006](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:238) [T025](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:675) [T064](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1570) [T074](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1800) |
| **G7 · Relationships and composition** | How do parts depend on one another, share information and form a coherent whole? | Interfaces, ownership/consumption distinctions, dependency maps and composition rules. | SkillOps contracts, development versus value dependencies, dossier/card boundaries and the company knowledge workspace. [T032](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:836) [T033](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:859) [T042](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1066) [T070](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1706) |
| **G8 · Measurement and evidence** | What exactly is being judged? Which evidence can support it? What does a number or verdict establish? | Measurement definitions, question banks, judging rules, sample frameworks and explicit limits. | Boolean scoring; paper case versus actual use; intricacy versus stakes; a safety-heavy decision rule; evaluation sample planning. [T026](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:698) [T027](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:721) [T041](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1043) [T072](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1752) [T075](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1825) |
| **G9 · Technical capability and feasibility** | What exists and can run? Which assumptions, constraints and blockers hold in the real environment? | Capability maps, technical options, implementation contracts, probe results and remaining experiments. | Isolated execution, materializing installed skills, the computation script, Promptfoo source capabilities and runtime architecture. [T057](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1409) [T058](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1432) [T061](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1501) [T067](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1637) [T071](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1729) |
| **G10 · Choice, fit and adequacy** | Which alternative or next question fits? Does this existing proposal withstand challenge? | A comparison, a revised proposal, a rejected assumption, criteria for a choice or a prioritized next inquiry. | Quarterback versus Traverse; consequential lifecycle conditions; testing a shared template; selecting the uncertainty that unlocks more work. [T052](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1300) [T053](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1321) [T013](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:401) [T034](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:882) |

### The boundary between meaning and technical questions

The distinction is useful, but the cases cross it repeatedly:

- **Meaning affects measurement.** “Complexity,” “importance” and “strength of a written case” looked related but required different evidence. Choosing a number before separating them would answer the wrong question. [T037](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:951) [T041](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1043)
- **Technical facts can change a conceptual design.** Isolation options and the availability of installed skill material changed what an experiment could claim and how preparation should work. [T057](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1409) [T058](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1432)
- **A definition can expose a missing operation.** A benefit profile sounded useful, but the user could not find the actual judging procedure. Written commitments had been mistaken for an available process. [T024](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:652) [T025](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:675)
- **A structural question can become a fit audit.** Applying the shared card template to Situation and Outcome exposed assumptions inherited from Benefit and changes that needed propagation to sibling artifacts. [T013](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:401) [T015](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:447)

For the future orchestrator, **semantic calculation** names the common activity. The stored record should still say whether the work is conceptual, structural, procedural, empirical, technical or a combination, and what fit is being sought. These distinctions help choose sources and assess the return. A missing fact may require retrieval, while developing the appropriate approach requires working through what those facts imply for the particular problem.

## 2. Inquiry moves: what you ask Traverse to do

The gap family identifies the subject; the move identifies the requested treatment. One run often uses several moves.

| Move | Typical intent in your requests | Example |
| --- | --- | --- |
| **Clarify** | Work out what the request really asks, or formulate better questions. | The confusing score comparison explicitly called for better-defined questions before answers. [T037](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:951) |
| **Define** | Develop the meaning, identity and boundaries of a concept. | Define a general evaluation ruler from first principles. [T076](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1848) |
| **Enumerate** | Find kinds, views, dimensions, cases and omissions. | Develop the harm catalogue after first establishing the conceptual scaffold. [T022](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:606) [T023](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:629) |
| **Decompose** | Separate things bundled into one phrase or choice. | Separate machine state, human intent and stale information in a status-change rule. [T065](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1593) |
| **Design** | Develop a structure, method, interface or candidate solution. | Specify the output of a task-to-methodology decomposition skill. [T069](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1683) |
| **Compare** | Examine alternatives against their purposes and constraints. | Compare Quarterback and Traverse, or local versus n8n runtime responsibilities. [T052](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1300) [T071](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1729) |
| **Challenge** | Test a prior answer, external feedback, taxonomy or hidden assumption. | Critique the reporting method and whether recurring reports make sense. [T060](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1478) |
| **Verify** | Inspect source code, existing artifacts, live state or actual behavior. | Read Promptfoo source for usable capabilities; probe isolation assumptions. [T067](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1637) [T057](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1409) |
| **Reframe** | Replace an inadequate framing while preserving the user's real concern. | Reopen skill complexity because a structural answer missed functional composition. [T046](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1158) |
| **Connect** | Relate an idea to its consumers, neighboring components or wider operation. | Distinguish build independence from dependencies for useful value. [T033](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:859) |
| **Prioritize** | Identify which uncertainty or route deserves attention next. | Select the next fuzzy parts of the daily work cycle. [T064](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1570) |
| **Generalize** | Extract a reusable method or principle from concrete experience. | Derive project-agnostic AI Operations Manager principles and pitfalls. [T073](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1777) |

These are purposes visible in the requests and results. They are **not replacement stages for Traverse's internal pipeline**. A “compare” inquiry still uses the actual method; the label tells the surrounding orchestrator what the inquiry is trying to achieve.

## 3. What triggers an inquiry in the history

You do not launch Traverse only when a blank section needs filling. Repeated triggers include:

| Trigger | Why it deserves attention | Examples |
| --- | --- | --- |
| A vague term carries important consequences | Different interpretations would produce different systems or judgments. | “Benefit,” “audit,” “card,” “general ruler.” [T010](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:330) [T039](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:997) [T047](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1181) [T076](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1848) |
| A plausible plan hides unanswered commitments | Actors, criteria, evidence or handoffs would otherwise be invented during execution. | The full evaluation scenario. [T074](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1800) |
| An answer is complete but misses the intended question | Additional detail in the same frame will not repair the mismatch. | Discovery versus decision; functional composition versus structural counts. [T063](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1547) [T046](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1158) |
| A concrete example breaks the general pattern | The template or taxonomy may encode the first example's assumptions. | Situation and Outcome expose shared-template defects. [T013](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:401) [T015](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:447) |
| A result seems surprising | The premise, comparison class or meaning of the measure may be wrong. | The simple-versus-complex skill score comparison. [T037](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:951) |
| A claimed capability lacks an actual procedure or mechanism | The design may describe an aspiration as something already available. | The judging process and computation script. [T025](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:675) [T061](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1501) |
| A technical premise could change the architecture | Reasoning must be grounded in what the environment supports. | Isolation and skill-materialization questions. [T057](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1409) [T058](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1432) |
| The next useful question is unclear | Depth needs to be directed toward something that helps the wider work. | The keystone inquiry and near-term benefit inquiry. [T034](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:882) [T040](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1020) |
| A local lesson may be useful elsewhere | Experience needs a reusable form while preserving its limits. | Manager principles and the domain-boundary test. [T073](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1777) [T043](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1089) |

The final trigger can also be **an unfinished result inside the loop**. The Codex general-ruler inquiry made a focused refinement pass when critique found that its candidate described a good guide's qualities more clearly than its usable contents. That was internal iteration within one inquiry, not a second human invocation. [T076](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1848)

## 4. Repeated sequences across inquiries

### A. Define → structure → apply → check fit → revise the shared structure

The card work provides a concrete version of your “develop the parts, then assemble” approach:

1. Define Benefit at the meaning level. [T010](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:330)
2. Work separately on its structure, then extract the artifact. [T011](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:353)
3. Define Situation and apply the shared pattern. [T012](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:378)
4. Check whether the pattern fits and repair Benefit-specific assumptions. [T013](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:401)
5. Define Outcome, then check its structure and the effects on the template and sibling cards. [T014](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:424) [T015](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:447)

This is more than a sequence of independent blocks. **Applying a part tests the shared design, and a repair can need propagation backward and sideways.** The September ruler chain repeats a smaller version: define → identify sections → write the guide → review the assembled artifact → add comparability and a miniature example. [T076](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1848) [T077](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1871)

### B. Apparent result → question clarification → targeted inquiries → revised measurement model

The surprising skill score did not immediately produce a new scoring formula. It led to better questions, then inquiries about what a score is for and how complexity might be measured. Later work separated intricacy, stakes, evidence modes and warrantedness. The user then reopened an answer that still missed functional composition. [T037](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:951) [T038](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:974) [T041](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1043) [T044](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1112) [T045](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1135) [T046](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1158) [T048](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1204)

**A useful result may be the map of questions that should now be investigated.** Automatically forcing every inquiry to end in a final answer would remove a use you explicitly requested.

### C. Options → approach → challenge → technical probes → revised preparation design

The experiment-execution chain moved from a failed launch and an option field to a proposed execution approach. You challenged the design's treatment of skills, asked whether the runtime assumptions were actually possible, and then investigated a materialization blocker. Environment inspection changed the premise; subsequent corrections changed what the preparation could claim. [T054](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1342) [T055](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1363) [T056](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1386) [T057](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1409) [T058](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1432)

**Some inquiries need empirical work inside them, and some return an experiment or external question rather than settling feasibility.** A strong argument about a runtime is insufficient evidence that its flags, authentication and loading behavior work as assumed.

### D. Concrete feedback → transferable principles → application to an operating scenario

The manager-versus-engineer inquiry extracted reusable principles from model-evaluation work and management feedback. A subsequent framing guide applied those principles outside the loop. The operating-scenario inquiry then worked through a concrete case, retaining real open decisions. You subsequently corrected intake so the design would not depend permanently on one person. [T073](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1777) [T074](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1800)

**Generalizing and applying are different jobs.** The generic principle needs a concrete fit check when it returns to operational work.

## 5. The output is part of the task definition

The history shows several legitimate return types:

| Requested return | What counts as useful completion at that level |
| --- | --- |
| Better question or question set | The uncertainty is separated into useful questions without pretending they have been answered. |
| Definition or conceptual model | The meaning, distinctions, boundaries and relevant examples are developed enough for the intended use. |
| Taxonomy or coverage map | Relevant kinds and variation are organized, with scope and omissions visible. |
| Framework or method | Someone can see how to approach a class of tasks, what information it needs and what it should produce. |
| Structure or output contract | Contents, relationships and sufficient examples explain the expected artifact. |
| Comparison or recommendation | Alternatives, relevant criteria and the reasons for the conclusion are explicit. |
| Technical finding | Claims distinguish inspected capability, observed behavior, proposed implementation and remaining probes. |
| Operating scenario | Stages, actors, records, handoffs, existing capabilities and unresolved commitments are understandable. |
| Reusable principles | Lessons transfer beyond the original project, with their basis and limits retained. |

### The sample-planning correction is especially important

After the sample inquiry, the assistant repeatedly explained that actual comments and checked answers were still missing. You clarified that the intended product was **the generic understanding of how sample planning should work**. That was a valid conceptual deliverable. It needed a clearer name and distinction from its applications. [T075](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1825)

The resulting separation was:

**Sample-planning framework → a plan for a particular evaluation → prepared examples and expected outcomes.**

The orchestrator should report all three statuses separately. It should not call an abstract framework operationally proven. It should also not describe the requested framework as unfinished merely because no concrete sample has been assembled.

## 6. What the corrections reveal

Your interventions are part of the evidence for how Traverse is used, rather than noise around the findings.

- **An accepted label can conceal inadequate depth.** Benefit had already received a meaning inquiry, but you later found the artifact too shallow and requested foundations, taxonomies and further views. A prior “done” status did not settle the depth needed for the next use. [T010](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:330) [T020](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:560)
- **A tidy answer can narrow away the question.** The initial complexity answer favored structural facts; your follow-up recovered the intended functional composition. [T041](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1043) [T046](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1158)
- **The assistant can invent the wrong choice.** The status inquiry showed that “strict versus loose” was not the right design variable. Later owner evidence also revised the assumed role of automation. [T065](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1593)
- **A method can apply its own rules at the wrong stage.** Requiring a named problem and consuming decision prevented the discovery work whose purpose was to find those things. [T062](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1524) [T063](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1547)
- **Examples can expose false generality.** The shared card template needed changes when it encountered a second and third kind of card. [T013](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:401) [T015](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:447)
- **Inherited conclusions need active reconsideration.** Card identity, naming and the relationship between defining and rendering a judgment changed across the inquiry chain. Treating the earliest answer as an immutable constraint would preserve its mistakes. [T044](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1112) [T047](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1181)
- **Pausing is an observed outcome.** One overlapping axis inquiry and one ambiguity inquiry stopped after articulation. A later request did not resume the ambiguity run because its framing questions remained unresolved. These are incomplete attempts in the catalogue, not successful findings. [T004](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:192) [T066](/Users/nsstorm/Documents/Codex/2026-09-15/i-think-we-can-i-want/outputs/traverse-usage-catalogue.md:1614)

This evidence supports treating Traverse as a developed inquiry capability with revisable outputs. It does not establish that it can replace the surrounding judgment you currently provide.

## 7. How the future orchestrator could use this taxonomy

This is a proposed integration approach derived from the history. It is not an implemented controller or a new instruction to run Traverse now.

### Before launching

Create a compact inquiry brief that records:

1. **What requires semantic calculation and why.** State what needs to be worked out and what it needs to fit. Include developing the dimensions or criteria for fit when those are unresolved, along with what currently looks unclear, surprising, inconsistent or incomplete.
2. **The intended use of the result.** Which design, artifact, decision or further investigation will consume it? During discovery this may be “make the unknowns visible,” without an already-selected downstream decision.
3. **The gap families and inquiry moves.** For example: measurement/evidence + reframe + design; technical feasibility + verify + compare.
4. **The requested level and return type.** Definition, structure, process, technical finding, generic framework, concrete application or a connected combination. Do not silently convert one into another.
5. **The context and constraints.** Relevant sources, previous findings, explicit exclusions, permitted evidence and the user's corrections.
6. **The live uncertainties.** Distinguish what reasoning can develop from what requires an observation, experiment, local expertise or another person's decision.
7. **The relationships.** What earlier conclusions may need retesting, what other parts could be affected, and which questions are too coupled to investigate separately.

These fields need not become a large form for every use. Their purpose is to prevent the misframings observed in the record.

### When the inquiry returns

Inspect five things:

1. **Answer fit:** Did it answer the actual question at the requested level? Use the latest user clarification as part of the reference.
2. **What now exists:** State the result plainly: “We now have a definition and structure,” “We have a candidate method,” or “This runtime behavior was observed.”
3. **Grounding:** Which claims are source observations, reasoned proposals, examples, test results or still-open assumptions?
4. **Consequences for the wider work:** What can use the result now? Which artifacts, interfaces or inherited conclusions need revision?
5. **The appropriate next action:** Apply it, combine it, test it, obtain missing evidence, reopen the framing, or stop because the commissioned understanding is sufficient.

Select onward routes in light of the broader objective. A route map is a set of possibilities; its existence does not make every route a commitment. Your history repeatedly shows selection, deferral, external application and later reopening between inquiries.

### Keep three levels of completion visible

- **The inquiry concluded:** its finding is available.
- **The intended understanding or design is adequate for its next use:** its fit has been checked at that level.
- **An application or operation has been verified:** implementation, use and resulting behavior have appropriate evidence.

These levels answer different questions. A framework request can finish at the second level. A claim that a data-handling guarantee works needs the third. “Run all the stages” by itself settles only the first, and even that needs the recorded outputs rather than a bare completion claim.

### Fit with AlignCraft

The taxonomy describes the inquiry content and treatment; AlignCraft describes which alignment is being examined. They should be used together rather than forced into a one-to-one mapping.

For example, the discovery correction primarily concerns **Task Alignment**; runtime alternatives concern **Action-Space** and **Action-Set Alignment**; propagating template changes concerns **Coherence Alignment**; and the framework-versus-prepared-sample distinction concerns **Outcome Alignment** against the requested deliverable. Source availability and context preparation concern **Workspace Alignment**. These are retrospective mappings, not additional observations or a separate evaluation of the full corpus.

## 8. Counts and limits of the taxonomy

The table uses one primary family per attempt for navigation. Secondary families and inquiry moves are available in each catalogue record and the structured data.

| Gap family | August–September | July supplement | Total primary tags |
| --- | ---: | ---: | ---: |
| G1 Task intent and framing | 2 | 3 | 5 |
| G2 Concept meaning and boundaries | 2 | 9 | 11 |
| G3 Coverage and variation | 2 | 4 | 6 |
| G4 Purpose and useful consumption | 0 | 5 | 5 |
| G5 Structure and output contracts | 2 | 3 | 5 |
| G6 Method and operating process | 5 | 4 | 9 |
| G7 Relationships and composition | 2 | 6 | 8 |
| G8 Measurement and evidence | 3 | 8 | 11 |
| G9 Technical capability and feasibility | 6 | 1 | 7 |
| G10 Choice, fit and adequacy | 4 | 6 | 10 |

These counts describe the recovered corpus. The July supplement contains a dense chain from one skill-management design effort, so it should not be read as a representative sample of all your work. Related inquiries are not statistically independent. Moving a borderline case between two families would change the counts without changing the substantive interpretation.

What remains unestablished is the threshold for choosing a full Traverse over a shorter investigation, the relative cost and benefit of different inquiry depths, and the reliability of automated gap detection and route selection. This study gives concrete examples and candidate distinctions for developing those rules; it does not supply a validated automatic routing policy.

## Conclusion

The broader capability is **Semantic Formulation**. It uses semantic calculation, performed through Traverse, to develop and test the appropriate fit, integrate findings and check the resulting whole. Specify what needs to be worked out, what it needs to fit and which inquiry moves can help, then judge the return against the intended deliverable and its next use.

Your historical pattern is not simply “identify a missing definition, run Traverse, continue.” It includes discovering new questions, developing concepts and structures separately, testing technical premises, correcting misframings, checking the fit of assembled parts and revisiting completed findings when the next use exposes a weakness. That is the design behavior the future orchestrator should learn to support.


