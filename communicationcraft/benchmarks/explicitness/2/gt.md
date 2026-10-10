


# Reference findings — ambiguity and missing meaning

## Status and scope

**Curated v1: 53 distinct expected issues across 42 independent cases.** This is a source-backed development reference, not a human-adjudicated or exhaustive gold standard. It was curated from the historical Claude/Codex correction collection at the author's request. Missing meaning is explicitly included alongside multiple-interpretation ambiguity.

Each expected issue identifies the affected original words, the missing meaning, the minimum clarification needed and a boundary against overreach. Each case supplies the author's exact correction and source addresses. Later AI replies are evidence of attempted repair, not automatically accepted fixes. The clarification targets below are curator-written interpretations, not quotations or claims that the author approved a final rewrite.

The test object is **the excerpt and setting in `01-ambiguous-passages.md`**, not an unseen full conversation. In particular, standalone headings/questions are labelled as such. A wider original context may resolve some gaps; do not transfer these labels unconditionally to the full source text. Original excerpts were taken verbatim either from a public assistant message or from the author's explicit quotation of the version being corrected; the source field is recorded for every passage.

This set contains selected positive cases. It supports checking whether a detector recovers the documented issues. It cannot establish a general false-positive rate, and an additional supported finding is not automatically wrong just because it is absent here. It is development material: the historical collection also informed the communication guidance, so this is not an independent holdout set for guidance derived from it.

## How to compare detector output

- Match by case and missing meaning, not exact label wording or a particular pattern ID.
- A finding must identify the real gap; repeating “unclear” or the whole passage is insufficient.
- Combine duplicate phrasings of the same finding. Keep distinct meanings separate even at the same location.
- Treat proposed fixes separately from detection. A correct finding does not justify invented facts, thresholds, owners or dates.
- Preserve legitimate uncertainty. A clarification may need to say what remains undecided or ask a targeted question.
- Review unmatched findings manually. Do not use this positive-only list as proof that every unlisted span is clean.
- Keep all cases from the same source episode together if creating development/test partitions later. Repeated corrections and quoted originals must not cross that split.

## Case index

| Case | Source topic | Source provider | Expected issues | Source episode |
|---|---|---|---:|---|
| C001 | System authentication | codex | 2 | [NA-0011](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:694) |
| C002 | Package installation | codex | 1 | [NA-0028](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:1759) |
| C003 | System architecture | codex | 1 | [NA-0031](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:1997) |
| C004 | Skill evaluation vocabulary | claude | 1 | [NA-0041](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:2603) |
| C005 | Human reviewers | claude | 1 | [NA-0042](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:2643) |
| C006 | Evaluation scope | claude | 1 | [NA-0044](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:2726) |
| C007 | Evaluation standards | claude | 2 | [NA-0048](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:2869) |
| C008 | Evaluation results | claude | 1 | [NA-0060](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:3301) |
| C009 | Skill-evaluation progress | claude | 3 | [NA-0075](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:3926) |
| C010 | Running evaluations | claude | 1 | [NA-0134](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:6600) |
| C011 | Agreement between judges | claude | 1 | [NA-0150](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:7452) |
| C012 | Human versus model judgment | claude | 1 | [NA-0159](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:7877) |
| C013 | Workflow records | claude | 1 | [NA-0168](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:8233) |
| C014 | Inventory measurement | claude | 1 | [NA-0180](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:8783) |
| C015 | Usage visibility | claude | 1 | [NA-0207](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:9774) |
| C016 | Cost allocation | claude | 1 | [NA-0262](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:11757) |
| C017 | Retention decision | claude | 2 | [NA-0274](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:12171) |
| C018 | Sequencing a change | claude | 1 | [NA-0280](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:12372) |
| C019 | Selecting workflows | claude | 1 | [NA-0291](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:12848) |
| C020 | Workflow output and access | claude | 1 | [NA-0308](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:13495) |
| C021 | Workflow ownership | claude | 1 | [NA-0338](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:14724) |
| C022 | Management decisions | claude | 1 | [NA-0343](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:14975) |
| C023 | Progress and completion | claude | 1 | [NA-0345](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:15056) |
| C024 | Prompt provenance | claude | 2 | [NA-0380](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:16415) |
| C025 | Prompt migration | claude | 2 | [NA-0390](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:16816) |
| C026 | Workflow identity | claude | 1 | [NA-0430](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:18412) |
| C027 | Credential changes | claude | 1 | [NA-0437](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:18697) |
| C028 | Evaluation layers | claude | 1 | [NA-0443](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:18900) |
| C029 | Meeting briefing | claude | 2 | [NA-0447](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:19035) |
| C030 | Experiment responsibility | claude | 1 | [NA-0462](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:19585) |
| C031 | Rollout testing | claude | 1 | [NA-0483](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:20485) |
| C032 | Model lifecycle | claude | 1 | [NA-0487](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:20670) |
| C033 | Trial scope | claude | 1 | [NA-0500](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:21163) |
| C034 | Evaluation decisions | claude | 3 | [NA-0502](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:21237) |
| C035 | Testing a preparation method | codex | 1 | [NA-0552](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:23273) |
| C036 | Airtable credential preparation | codex | 2 | [NA-0566](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:23856) |
| C037 | Creating credential records | codex | 1 | [NA-0583](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:24509) |
| C038 | Keys and saved connections | codex | 1 | [NA-0584](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:24543) |
| C039 | Comparison terminology | codex | 1 | [NA-0587](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:24678) |
| C040 | Implementation scope | codex | 1 | [NA-0594](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:25050) |
| C041 | Summaries across records | codex | 1 | [NA-0596](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:25125) |
| C042 | Locations of linked evidence | codex | 1 | [NA-0597](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:25178) |

## Reference findings

### C001 — System authentication

**Historical correction (author, verbatim):**

> but this is only done when there is domain contxt? or always? make this more explicit

**Additional author correction (NA-0012, verbatim):**

> and also wdym by session token? what session? codex? or storyos? who genertas this

**Evidence and provenance:**

- Passage 1: [NA-0011](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:694), `request` field; public user message at recorded source line 1781. The author quoted the target wording; the exact document version was not separately recovered for this set.
- Correction: [NA-0011](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:694), user message line 1781, 2026-07-16T14:31:36.822Z.
- Related corrections or follow-ups: [NA-0012](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:731). These are supporting episode evidence, not extra counts of the same issue.

#### GT-001 — Which system the session belongs to

- **Affected wording:** "session token".
- **Expected finding:** The reader cannot tell whether this is a Codex conversation token or StoryOS authentication, and therefore how the described path relates to ordinary Codex use.
- **Clarification target:** Identify the system and authentication session; explain the issuer or source if necessary. Do not invent a deployment or token implementation.
- **Boundary:** Do not claim every use of Codex invokes StoryOS.

#### GT-002 — Which context is added under which conditions

- **Affected wording:** "then route code adds workspace and permission context before doing domain work.".
- **Expected finding:** The sequence does not establish which steps are common to authenticated requests and which depend on the route or domain operation.
- **Clarification target:** State the applicability of session, permission and domain context separately, using established source facts.
- **Boundary:** Do not require domain context on every request or guess exceptions.

### C002 — Package installation

**Historical correction (author, verbatim):**

> signed/versioned manifests
>
> wdym ?

**Evidence and provenance:**

- Passage 1: [NA-0028](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:1759), `before` field; public assistant message at recorded source line 2765. The excerpt is an exact substring of the recorded public assistant message.
- Correction: [NA-0028](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:1759), user message line 2771, 2026-07-16T16:40:21.152Z.

#### GT-003 — The installation artifact and its qualifiers are unexplained

- **Affected wording:** "signed/versioned manifests".
- **Expected finding:** A manifest, its version and its signature are named without explaining what information the artifact carries or what the installer does with it.
- **Clarification target:** Explain a manifest as a description of an exact installation package and distinguish release identification from publisher verification.
- **Boundary:** An illustrative format is acceptable; do not present an invented schema as the current product schema.

### C003 — System architecture

**Historical correction (author, verbatim):**

> what will be a StoryOS operating-context layer ? what makes it different?

**Evidence and provenance:**

- Passage 1: [NA-0031](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:1997), `before` field; public assistant message at recorded source line 3135. The excerpt is an exact substring of the recorded public assistant message.
- Correction: [NA-0031](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:1997), user message line 3141, 2026-07-17T08:33:25.186Z.

#### GT-004 — How the proposed layer actually participates

- **Affected wording:** "operating-layer model with an additive Codex interface".
- **Expected finding:** The diagram and list of responsibilities do not explain how a concrete work request uses the operating context, or what it contributes beyond the direct provider tools.
- **Clarification target:** Describe how a request obtains applicable operating guidance and how that guidance relates to the actual business data and tools.
- **Boundary:** Do not turn a proposed design into an already implemented capability.

### C004 — Skill evaluation vocabulary

**Historical correction (author, verbatim):**

> the axes is ambigious ... what axes? maybe they need name?

**Evidence and provenance:**

- Passage 1: [NA-0041](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:2603), `before` field; public assistant message at recorded source line 2614. The excerpt is an exact substring of the recorded public assistant message.
- Correction: [NA-0041](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:2603), user message line 2616, 2026-07-20T18:47:00.789Z.

#### GT-005 — Which axes the heading means

- **Affected wording:** "the axes".
- **Expected finding:** The heading presumes an identifiable set of axes but does not name the set or the quantities in it.
- **Clarification target:** Identify the skill-quality axes and, if needed for this heading, their members.
- **Boundary:** Established shorthand can be acceptable when its definition is actually supplied to the reader.

### C005 — Human reviewers

**Historical correction (author, verbatim):**

> panel ? what panel? ambigius also

**Evidence and provenance:**

- Passage 1: [NA-0042](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:2643), `request` field; public user message at recorded source line 2634. The author quoted the target wording; the exact document version was not separately recovered for this set.
- Correction: [NA-0042](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:2643), user message line 2634, 2026-07-20T18:48:32.193Z.
- Related corrections or follow-ups: [NA-0041](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:2603). These are supporting episode evidence, not extra counts of the same issue.

#### GT-006 — Who participates in the panel

- **Affected wording:** "a panel".
- **Expected finding:** The term does not identify whether the panel consists of people, models, skill users or another group, or their role in evaluation.
- **Clarification target:** Introduce the judging panel and explain what a panelist does.
- **Boundary:** The initial missing letter is a historical quotation artifact, not a scored typo.

### C006 — Evaluation scope

**Historical correction (author, verbatim):**

> i dont understand be more clear

**Evidence and provenance:**

- Passage 1: [NA-0044](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:2726), `before` field; public assistant message at recorded source line 2946. The excerpt is an exact substring of the recorded public assistant message.
- Correction: [NA-0044](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:2726), user message line 2953, 2026-07-21T09:46:46.167Z.

#### GT-007 — What differs between the two options

- **Affected wording:** "gate-first (default) or assess-included?".
- **Expected finding:** The labels do not make explicit which questions would be answered under each option and what work would be added by including assessment.
- **Clarification target:** Explain the admission/value question and the output-quality question, then state which option includes which.
- **Boundary:** Do not treat a provisional option as approved or supply an arbitrary schedule.

### C007 — Evaluation standards

**Historical correction (author, verbatim):**

> Writing the quality bars , this is per skill? or they are meta and all applicable? and wdym by cards???

**Evidence and provenance:**

- Passage 1: [NA-0048](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:2869), `before` field; public assistant message at recorded source line 2967. The excerpt is an exact substring of the recorded public assistant message.
- Correction: [NA-0048](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:2869), user message line 2976, 2026-07-21T09:58:32.000Z.

#### GT-008 — Whether the standards are shared or specific to each skill

- **Affected wording:** "Writing the quality bars".
- **Expected finding:** The author asks whether the quality bars are written once for all skills or separately for each skill; the excerpt combines a general label with a task-specific example without resolving the levels.
- **Clarification target:** Distinguish any shared definition from the criteria instantiated for an individual skill.
- **Boundary:** Do not infer one universal checklist or one document per skill merely from the word bars.

#### GT-009 — What a card is and how it relates to a quality bar

- **Affected wording:** "(the cards)".
- **Expected finding:** The parenthetical treats the artifact name as an explanation, but does not say whether the card is a definition, test, checklist or output.
- **Clarification target:** Explain the artifact’s role and the information it supplies.
- **Boundary:** No particular final name is required; later naming changes are not additional issues here.

### C008 — Evaluation results

**Historical correction (author, verbatim):**

> it is really unclear what retro means retro pass means it is extremely vague what they are ...

**Evidence and provenance:**

- Passage 1: [NA-0060](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:3301), `request` field; public user message at recorded source line 5435. The author quoted the target wording; the exact document version was not separately recovered for this set.
- Correction: [NA-0060](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:3301), user message line 5435, 2026-07-22T09:31:33.517Z.

#### GT-010 — What a retrospective verdict means

- **Affected wording:** "retro-PASS".
- **Expected finding:** The labels do not explain what retro changes about PASS/PARK/ROUTE/NO: a hypothetical judgment about an existing skill versus an instruction to adopt or remove it.
- **Clarification target:** Explain the retrospective question and its observational status before interpreting the counts.
- **Boundary:** Do not score the visual line breaks as errors or infer that a verdict authorized a live action.

### C009 — Skill-evaluation progress

**Historical correction (author, verbatim):**

> when this happened? to which skill?

**Additional author correction (NA-0076, verbatim):**

> what is  SELs shape , why these 4 things
>
> and what is three axis hytpotehsis, it belongs to these 4 some how?

**Evidence and provenance:**

- Passage 1: [NA-0075](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:3926), `before` field; public assistant message at recorded source line 9052. The excerpt is an exact substring of the recorded public assistant message.
- Correction: [NA-0075](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:3926), user message line 9054, 2026-07-24T07:32:23.921Z.
- Related corrections or follow-ups: [NA-0076](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:3964). These are supporting episode evidence, not extra counts of the same issue.

#### GT-011 — Which experiment the reported result comes from

- **Affected wording:** "tested on a real skill, which scored 82".
- **Expected finding:** The statement reports a score and fixes without identifying the skill or the occasion of the test, preventing the reader from locating what was actually tried.
- **Clarification target:** Identify the tested skill and enough timing or experiment context to distinguish the run.
- **Boundary:** The score and historical test are not independently revalidated by this dataset.

#### GT-012 — The listed elements have unexplained, different roles

- **Affected wording:** "the SEL's shape (gate · assess · prove, effectiveness-vs-conformance boundary)".
- **Expected finding:** Three evaluation activities and a boundary are compressed into one parenthetical, so the reader cannot tell whether they are four equivalent parts or how they relate.
- **Clarification target:** Distinguish the three activities from the boundary and state the question each answers.
- **Boundary:** Do not flag lists merely for mixing types when their roles are explained.

#### GT-013 — Which axes and how they relate to the evaluation activities

- **Affected wording:** "the three-axis hypothesis with its pre-committed falsifiers".
- **Expected finding:** The reader is given a second conceptual set without its members or its relationship to gate/assess/prove.
- **Clarification target:** Name the quality dimensions and explain their role in the judgments described.
- **Boundary:** Do not demand a full method specification; the missing relationship is the target.

### C010 — Running evaluations

**Historical correction (author, verbatim):**

> what do  you mean? explain better

**Evidence and provenance:**

- Passage 1: [NA-0134](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:6600), `before` field; public assistant message at recorded source line 2725. The excerpt is an exact substring of the recorded public assistant message.
- Correction: [NA-0134](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:6600), user message line 2750, 2026-08-06T08:05:05.809Z.

#### GT-014 — What unresolved design choice is being referred to

- **Affected wording:** "the unit of one judging invocation".
- **Expected finding:** The phrase does not reveal whether the unresolved unit is a question, question group, whole question bank, skill or session.
- **Clarification target:** State the actual choice about how much judging work belongs in one model conversation.
- **Boundary:** Keep the choice unresolved; identifying it does not require choosing an option.

### C011 — Agreement between judges

**Historical correction (author, verbatim):**

> what is the split set ?

**Evidence and provenance:**

- Passage 1: [NA-0150](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:7452), `before` field; public assistant message at recorded source line 5040. The excerpt is an exact substring of the recorded public assistant message.
- Correction: [NA-0150](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:7452), user message line 5048, 2026-08-07T12:37:04.299Z.

#### GT-015 — What is splitting and what belongs to the set

- **Affected wording:** "split set".
- **Expected finding:** Question IDs are listed, but the term split does not explicitly say that independent judges disagreed on their answers.
- **Clarification target:** Define the set as questions with non-unanimous judgments and distinguish that from a change to the tested skill.
- **Boundary:** Do not infer that disagreement proves a question is defective.

### C012 — Human versus model judgment

**Historical correction (author, verbatim):**

> not udnerstabdle , wdym by works throught the questions? u mean manually answers them ?

**Evidence and provenance:**

- Passage 1: [NA-0159](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:7877), `request` field; public user message at recorded source line 5224. The author quoted the target wording; the exact document version was not separately recovered for this set.
- Correction: [NA-0159](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:7877), user message line 5224, 2026-08-07T13:18:06.639Z.

#### GT-016 — Who actually answers the questions

- **Affected wording:** "works through the questions".
- **Expected finding:** Opening a session manually does not establish whether the person or a model supplies the judgments inside it.
- **Clarification target:** State explicitly whether the person is the judge or launches a model that answers.
- **Boundary:** Do not infer the actor just from by hand, which may modify opening the session.

### C013 — Workflow records

**Historical correction (author, verbatim):**

> i dont understand anything what this means...

**Evidence and provenance:**

- Passage 1: [NA-0168](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:8233), `before` field; public assistant message at recorded source line 746. The excerpt is an exact substring of the recorded public assistant message.
- Correction: [NA-0168](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:8233), user message line 749, 2026-08-11T11:02:24.898Z.

#### GT-017 — What information is compared to establish currency

- **Affected wording:** "cross-checked against n8n/spend rather than the table grading itself".
- **Expected finding:** Systems and a metaphor are supplied instead of a concrete comparison: what the row claims, which independent observation is checked and what disagreement means.
- **Clarification target:** Name an example of a table claim and the external observation used to verify it.
- **Boundary:** The repair must not assume that spend alone establishes every operational fact.

### C014 — Inventory measurement

**Historical correction (author, verbatim):**

> not clear , use better understandable language

**Evidence and provenance:**

- Passage 1: [NA-0180](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:8783), `request` field; public user message at recorded source line 1719. The author quoted the target wording; the exact document version was not separately recovered for this set.
- Correction: [NA-0180](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:8783), user message line 1719, 2026-08-12T08:17:34.879Z.
- Related corrections or follow-ups: [NA-0181](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:8811). These are supporting episode evidence, not extra counts of the same issue.

#### GT-018 — How the counted unit relates to an independent inventory check

- **Affected wording:** "if rows silently define the unit, the audit grades the registry against itself".
- **Expected finding:** The compressed guideline does not explain how using table rows as the definition of a workload would prevent the audit from detecting real work absent from that table.
- **Clarification target:** Explain the relationship among keys, actual workflows and records, and why the real-work inventory must be established independently before comparing it with the records.
- **Boundary:** Do not demand a settled workload definition where the instruction is to investigate it; explain the comparison the instruction calls for.

### C015 — Usage visibility

**Historical correction (author, verbatim):**

> bc it is too ambigius, make sure it has enough context of what we aer talking about and why we are asking it to him

**Evidence and provenance:**

- Passage 1: [NA-0207](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:9774), `before` field; public assistant message at recorded source line 4619. The excerpt is an exact substring of the recorded public assistant message.
- Correction: [NA-0207](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:9774), user message line 4623, 2026-08-17T16:08:10.657Z.

#### GT-019 — What see means and which keys are in scope

- **Affected wording:** "which keys does the management key actually see?".
- **Expected finding:** The headline does not say whether seeing means retrieving key secrets, listing keys or including their usage in a report, nor establish the relevant provider/account scope.
- **Clarification target:** State that the question concerns visibility of usage/spend for the relevant API keys and accounts, with the necessary local background.
- **Boundary:** Do not ask for secret values or invent which accounts are actually visible.

### C016 — Cost allocation

**Historical correction (author, verbatim):**

> idk what is  Moderation family per-flow cost split .. make it less ambigious

**Evidence and provenance:**

- Passage 1: [NA-0262](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:11757), `request` field; public user message at recorded source line 8851. The author quoted the target wording; the exact document version was not separately recovered for this set.
- Correction: [NA-0262](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:11757), user message line 8851, 2026-08-24T09:39:04.678Z.

#### GT-020 — What cost is being split and what result is needed

- **Affected wording:** "Moderation family per-flow cost split".
- **Expected finding:** The compressed title and key-level amount do not plainly state the proposed allocation of a shared bill to individual workflows and why that is needed.
- **Clarification target:** Explain that several workflows share a key and the task is to establish each workflow’s cost.
- **Boundary:** Do not treat a historical amount or proposed allocation method as verified current fact.

### C017 — Retention decision

**Historical correction (author, verbatim):**

> PII stance for what? why it is used? why it matters ?  what is a named signer?

**Evidence and provenance:**

- Passage 1: [NA-0274](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:12171), `before` field; public assistant message at recorded source line 10183. The excerpt is an exact substring of the recorded public assistant message.
- Correction: [NA-0274](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:12171), user message line 10185, 2026-08-25T10:52:37.214Z.

#### GT-021 — What data-handling decision is being discussed

- **Affected wording:** "the PII stance".
- **Expected finding:** The phrase does not explain which information or retention change the stance concerns.
- **Clarification target:** Name the contemplated handling or retention of personal data and the scope of the decision.
- **Boundary:** This labels missing meaning only; it does not endorse the historical claim that a legal/privacy sign-off was required.

#### GT-022 — What contribution or responsibility is expected of that person

- **Affected wording:** "a named signer".
- **Expected finding:** The wording names a role without saying what the person would approve or take responsibility for.
- **Clarification target:** State the actual requested decision and responsibility; leave the responsible person open if not established.
- **Boundary:** Do not invent a mandatory signer or expand someone’s authority.

### C018 — Sequencing a change

**Historical correction (author, verbatim):**

> then parts, wdym by then?

**Evidence and provenance:**

- Passage 1: [NA-0280](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:12372), `before` field; public assistant message at recorded source line 10820. The excerpt is an exact substring of the recorded public assistant message.
- Correction: [NA-0280](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:12372), user message line 10920, 2026-08-25T15:53:47.763Z.

#### GT-023 — Which event permits or precedes the configuration change

- **Affected wording:** "**Then:**".
- **Expected finding:** After a bullet about a later pseudonymization design, then can refer either to that work or to approval of the immediate retention option.
- **Clarification target:** State the particular decision or prerequisite after which Jeremy/Art act.
- **Boundary:** Do not impose a new dependency or infer that the later design must finish first.

### C019 — Selecting workflows

**Historical correction (author, verbatim):**

> wdym by next tier of AI workflows?

**Evidence and provenance:**

- Passage 1: [NA-0291](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:12848), `before` field; public assistant message at recorded source line 12003. The excerpt is an exact substring of the recorded public assistant message.
- Correction: [NA-0291](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:12848), user message line 12044, 2026-08-27T09:11:19.853Z.

#### GT-024 — Which workflows qualify for the next group

- **Affected wording:** "the next tier of AI workflows where evaluation is realistic".
- **Expected finding:** Next tier and realistic do not identify a population or a usable inclusion criterion.
- **Clarification target:** Name the intended workflow group or the supported criterion by which it will be chosen; if not decided, say so.
- **Boundary:** Do not invent workflow names, quantities or an evaluation threshold.

### C020 — Workflow output and access

**Historical correction (author, verbatim):**

> wdym by writing? u mean logs? or results?

**Additional author correction (NA-0309, verbatim):**

> also this part is ambigiuos too,

**Evidence and provenance:**

- Passage 1: [NA-0308](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:13495), `before` field; public assistant message at recorded source line 12486. The excerpt is an exact substring of the recorded public assistant message.
- Correction: [NA-0308](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:13495), user message line 12488, 2026-08-27T13:51:39.259Z.
- Related corrections or follow-ups: [NA-0309](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:13527), [NA-0317](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:13794). These are supporting episode evidence, not extra counts of the same issue.

#### GT-025 — How the accessible and destination sets overlap

- **Affected wording:** "our Airtable token reaches 15 bases, these workflows write into 10, and 9 of those sit outside it".
- **Expected finding:** The reader must reconstruct the relation between fifteen accessible bases, ten destination bases and the nine inaccessible destinations.
- **Clarification target:** State the permission-set relationship directly: how many destination bases are accessible and how many are not.
- **Boundary:** Do not infer that all fifteen accessible bases are workflow destinations or add the later no-date-field finding.

### C021 — Workflow ownership

**Historical correction (author, verbatim):**

> Four rows in the Workflows table are yours
>
>
> this is again ambigious...

**Evidence and provenance:**

- Passage 1: [NA-0338](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:14724), `before` field; public assistant message at recorded source line 14795. The excerpt is an exact substring of the recorded public assistant message.
- Correction: [NA-0338](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:14724), user message line 14815, 2026-08-28T08:32:00.441Z.

#### GT-026 — What relationship yours asserts

- **Affected wording:** "are yours".
- **Expected finding:** The wording does not distinguish records created by the recipient, records assigned to them, or workflows for which they are recorded as owner.
- **Clarification target:** State the specific relationship indicated by the relevant ownership field or evidence.
- **Boundary:** Do not infer authority to archive from a possessive phrase alone.

### C022 — Management decisions

**Historical correction (author, verbatim):**

> what decision? be explicit,  just bc summary doesnt mean it shouldnt be undersabble....

**Evidence and provenance:**

- Passage 1: [NA-0343](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:14975), `request` field; public user message at recorded source line 15197. The author quoted the target wording; the exact document version was not separately recovered for this set.
- Correction: [NA-0343](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:14975), user message line 15197, 2026-08-28T09:32:19.843Z.

#### GT-027 — What decision is being requested

- **Affected wording:** "decision #7".
- **Expected finding:** A filing number and evidence-status claim do not state the substantive choice Duncan needs to make.
- **Clarification target:** State the question or alternatives; use the number as a reference after the meaning.
- **Boundary:** Do not infer a decision merely from an issue number or fabricate a preferred option.

### C023 — Progress and completion

**Historical correction (author, verbatim):**

> hmm, wdym  complete? it doesnt make sense? we only work with status oclumn and it is not finsihed no ?

**Evidence and provenance:**

- Passage 1: [NA-0345](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:15056), `before` field; public assistant message at recorded source line 15461. The excerpt is an exact substring of the recorded public assistant message.
- Correction: [NA-0345](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:15056), user message line 15530, 2026-08-28T15:55:23.691Z.

#### GT-028 — Which dimension of completeness has been achieved

- **Affected wording:** "The Workflows table is complete for the first time.".
- **Expected finding:** The first bullet can imply fully accurate and populated records, while its evidence concerns inventory coverage and the next bullet reports unresolved status errors.
- **Clarification target:** Qualify completion as coverage of workflows and retain the limits on field completeness or accuracy.
- **Boundary:** Do not label the specific coverage result false solely because other work remains.

### C024 — Prompt provenance

**Historical correction (author, verbatim):**

> why this matter, this is for what? give some context

**Evidence and provenance:**

- Passage 1: [NA-0380](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:16415), `before` field; public assistant message at recorded source line 4678. The excerpt is an exact substring of the recorded public assistant message.
- Passage 2: [NA-0380](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:16415), `before` field; public assistant message at recorded source line 4678. The excerpt is an exact substring of the recorded public assistant message.
- Correction: [NA-0380](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:16415), user message line 4680, 2026-09-02T10:06:27.016Z.

#### GT-029 — What makes one stored prompt authoritative

- **Affected wording:** "runtime-loaded → table is truth; everything else → n8n is truth until migrated".
- **Expected finding:** The shorthand does not explain the distinction between a workflow fetching its live prompt from a table and a table merely holding a copy of an inline prompt.
- **Clarification target:** Explain the actual source used during execution and how that establishes which version an evaluation should use.
- **Boundary:** Do not claim the table’s prompt content is factually correct merely because it is the version executed.

#### GT-030 — Why this audit matters to the intended work

- **Affected wording:** "Exactly the evidence decision #6 needed".
- **Expected finding:** The report assumes the reader knows the purpose of the prompt-source decision and how these results affect model evaluation.
- **Clarification target:** Connect prompt identity to comparing models under the intended prompt and inputs.
- **Boundary:** Do not introduce an unrelated plan or validate the historical audit arithmetic.

### C025 — Prompt migration

**Historical correction (author, verbatim):**

> chooses per row? u mean per workflow?  why u think they are stale?  and migrate the workflow to runtime loading.  what this means even?

**Evidence and provenance:**

- Passage 1: [NA-0390](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:16816), `request` field; public user message at recorded source line 5274. The author quoted the target wording; the exact document version was not separately recovered for this set.
- Correction: [NA-0390](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:16816), user message line 5274, 2026-09-02T12:25:32.005Z.
- Related corrections or follow-ups: [NA-0391](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:16863), [NA-0392](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:16888). These are supporting episode evidence, not extra counts of the same issue.

#### GT-031 — The unit of the owner’s decision

- **Affected wording:** "each owner chooses per row".
- **Expected finding:** The wording leaves unclear whether the decision is independent for every stored prompt row or concerns a workflow’s prompt-loading design, potentially affecting several rows.
- **Clarification target:** Name the actual decision unit and explain how its prompt records relate to it.
- **Boundary:** Do not equate eighteen prompt rows with eighteen workflows or eighteen independent decisions.

#### GT-032 — What operation the proposed migration changes

- **Affected wording:** "migrate the workflow to runtime loading".
- **Expected finding:** The phrase does not say what the workflow will load, from where, or how this differs from the current inline prompt.
- **Clarification target:** Explain that a workflow would retrieve prompt text from the specified table when it runs, rather than use text embedded in its node.
- **Boundary:** Do not silently authorize a migration or choose which copy should become authoritative.

### C026 — Workflow identity

**Historical correction (author, verbatim):**

> The writing workflows that used to read it are switched off. wdym? this refers to what?

**Evidence and provenance:**

- Passage 1: [NA-0430](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:18412), `before` field; public assistant message at recorded source line 7042. The excerpt is an exact substring of the recorded public assistant message.
- Correction: [NA-0430](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:18412), user message line 7051, 2026-09-03T20:31:46.038Z.

#### GT-033 — Which workflows are being described

- **Affected wording:** "The writing workflows".
- **Expected finding:** The sentence names a functional class but does not identify which workflows it includes or how they differ from the live readers discussed elsewhere.
- **Clarification target:** Name the relevant writing workflows or give an unambiguous identifying description.
- **Boundary:** No need to demand a link for every name; do not adopt inconsistent counts in the later response.

### C027 — Credential changes

**Historical correction (author, verbatim):**

> wdym ? be clear? date for what?

**Evidence and provenance:**

- Passage 1: [NA-0437](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:18697), `before` field; public assistant message at recorded source line 8243. The excerpt is an exact substring of the recorded public assistant message.
- Correction: [NA-0437](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:18697), user message line 8246, 2026-09-04T08:36:48.651Z.

#### GT-034 — Which change the date is for

- **Affected wording:** "a cutover date that works".
- **Expected finding:** The timing request does not explicitly name the transition from a shared key to the individual workflow keys.
- **Clarification target:** Name the switch the date schedules and distinguish its effect on future attribution from earlier estimates.
- **Boundary:** Do not invent a date or imply the switch has already happened.

### C028 — Evaluation layers

**Historical correction (author, verbatim):**

> which 4 layer approach?

**Evidence and provenance:**

- Passage 1: [NA-0443](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:18900), `before` field; public assistant message at recorded source line 8900. The excerpt is an exact substring of the recorded public assistant message.
- Correction: [NA-0443](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:18900), user message line 8909, 2026-09-07T08:59:34.283Z.

#### GT-035 — Which four layers were reviewed

- **Affected wording:** "the four-layer approach".
- **Expected finding:** The count and generic name do not identify the judging stages whose structure the colleague found sensible.
- **Clarification target:** Name or briefly describe the four evaluation layers and distinguish that feedback from approval of every evaluation detail.
- **Boundary:** Do not inflate confirmation of a structure into blanket approval.

### C029 — Meeting briefing

**Historical correction (author, verbatim):**

> test plan, test plan of what???

**Evidence and provenance:**

- Passage 1: [NA-0447](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:19035), `before` field; public assistant message at recorded source line 8955. The excerpt is an exact substring of the recorded public assistant message.
- Correction: [NA-0447](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:19035), user message line 8958, 2026-09-07T09:22:31.721Z.
- Related corrections or follow-ups: [NA-0448](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:19067). These are supporting episode evidence, not extra counts of the same issue.

#### GT-036 — What the plan is intended to test

- **Affected wording:** "the test plan".
- **Expected finding:** The compressed briefing names a plan without explicitly identifying the model comparison or evaluation-method trial it concerns.
- **Clarification target:** State the evaluation the plan will specify at the detail needed for the audience.
- **Boundary:** Do not confuse a plan with a completed test or invent its settings.

#### GT-037 — What the metaphor refers to

- **Affected wording:** "the \"answer key\" for judging moderation".
- **Expected finding:** Answer key could mean a labelled set of examples, a rubric, workflow rules or an expert’s confirmation; the briefing does not identify which.
- **Clarification target:** Name the actual criteria or reference material being discussed and preserve its status.
- **Boundary:** Do not present a draft definition as an approved set of correct answers.

### C030 — Experiment responsibility

**Historical correction (author, verbatim):**

> it is not clear who is the owner of running the experiment

**Evidence and provenance:**

- Passage 1: [NA-0462](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:19585), `before` field; public assistant message at recorded source line 9909. The excerpt is an exact substring of the recorded public assistant message.
- Correction: [NA-0462](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:19585), user message line 9917, 2026-09-07T14:58:48.453Z.

#### GT-038 — Who will actually run the experiment

- **Affected wording:** "The idea is to try it on something real and calibrate it.".
- **Expected finding:** The author’s tool preference and planning role are expressed, but responsibility for carrying out the trial is not identified or explicitly left open.
- **Clarification target:** Separate ownership of the plan from ownership of execution and state what remains unassigned.
- **Boundary:** Do not assign the experiment to the author or a colleague without evidence.

### C031 — Rollout testing

**Historical correction (author, verbatim):**

> it is like un understandable why three. It doesn't make sense. In which context?

**Evidence and provenance:**

- Passage 1: [NA-0483](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:20485), `before` field; public assistant message at recorded source line 12828. The excerpt is an exact substring of the recorded public assistant message.
- Correction: [NA-0483](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:20485), user message line 12946, 2026-09-08T16:19:11.263Z.

#### GT-039 — What three counts and why these runs are being performed

- **Affected wording:** "Three parallel runs in shadow".
- **Expected finding:** It is unclear whether three means models, repeated trials, workflow executions or periods, and what that number establishes before switching.
- **Clarification target:** Explain the current-versus-candidate comparison and the intended repetition unit; leave an unsupported number or criterion open.
- **Boundary:** Do not invent a rationale for exactly three or treat a suggested threshold as established.

### C032 — Model lifecycle

**Historical correction (author, verbatim):**

> Model's what state? like, be clear, like, what state are you talking about?

**Evidence and provenance:**

- Passage 1: [NA-0487](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:20670), `before` field; public assistant message at recorded source line 13043. The excerpt is an exact substring of the recorded public assistant message.
- Correction: [NA-0487](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:20670), user message line 13045, 2026-09-08T16:36:09.566Z.

#### GT-040 — Which kind of state the model record should show

- **Affected wording:** "the model's state".
- **Expected finding:** State could refer to deployment, provider availability, technical status or progress through consideration and evaluation.
- **Clarification target:** Identify the decision/process stage meant, without confusing it with the workflow’s production state.
- **Boundary:** A short explanation or examples suffice; no universal lifecycle schema is required.

### C033 — Trial scope

**Historical correction (author, verbatim):**

> what is the point with hulu? explain to me pls, wdym proved??

**Evidence and provenance:**

- Passage 1: [NA-0500](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:21163), `before` field; public assistant message at recorded source line 15021. The excerpt is an exact substring of the recorded public assistant message.
- Correction: [NA-0500](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:21163), user message line 15023, 2026-09-09T14:52:10.848Z.
- Related corrections or follow-ups: [NA-0501](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:21195). These are supporting episode evidence, not extra counts of the same issue.

#### GT-041 — What a Hulu trial would establish and why it is mentioned

- **Affected wording:** "Hulu proves the mechanics only; each brand gets its own verdict.".
- **Expected finding:** The sentence abruptly introduces Hulu and mechanics without explaining the trial’s relationship to testing the evaluation procedure and judging models on each brand’s work.
- **Clarification target:** Explain the scope of a first trial and distinguish checking the method from transferring a quality verdict to other brands.
- **Boundary:** Do not imply that such a trial already proved anything merely because the historical sentence uses proves.

### C034 — Evaluation decisions

**Historical correction (author, verbatim):**

> which providers may receive client text before we've adopted them.

**Additional author correction (NA-0503, verbatim):**

> what do you mean? what is account team?

**Additional author correction (NA-0506, verbatim):**

> Why are you just calling it six? Like, how you will understand these are questions.

**Evidence and provenance:**

- Passage 1: [NA-0502](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:21237), `before` field; public assistant message at recorded source line 14959. The excerpt is an exact substring of the recorded public assistant message.
- Passage 2: [NA-0502](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:21237), `before` field; public assistant message at recorded source line 14959. The excerpt is an exact substring of the recorded public assistant message.
- Correction: [NA-0502](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:21237), user message line 15116, 2026-09-09T15:03:54.335Z.
- Related corrections or follow-ups: [NA-0503](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:21275), [NA-0504](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:21303), [NA-0506](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:21389). These are supporting episode evidence, not extra counts of the same issue.

#### GT-042 — Which people the recipient should understand as the account team

- **Affected wording:** "the account team is told".
- **Expected finding:** The team label lacks an identifying role relative to the client and workflow.
- **Clarification target:** Identify the people responsible for the relevant client account at the organization.
- **Boundary:** Do not invent individual names or turn notification into an approval requirement.

#### GT-043 — What adopted means for a model provider in this decision

- **Affected wording:** "before we've adopted them".
- **Expected finding:** The term blurs prior production use, formal approval, an agreement and permission to send evaluation data.
- **Clarification target:** State the particular provider/data-use decision meant and identify unresolved authorization rather than substituting the vague adoption label.
- **Boundary:** No historical legal or contract claim is treated as verified here.

#### GT-044 — What the number refers to

- **Affected wording:** "Six are in the document".
- **Expected finding:** The count does not identify its objects as questions or decisions, leaving the reader to recover them from a linked document.
- **Clarification target:** Name the set as the outstanding decision questions and give the relevant subjects or a precise reference appropriate to the message.
- **Boundary:** Do not require every background question to be reproduced if the needed ones are made explicit.

### C035 — Testing a preparation method

**Historical correction (author, verbatim):**

> explain how does this practical check works? what we check what kind of things and why and whwat we are trying to understand or establish

**Evidence and provenance:**

- Passage 1: [NA-0552](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:23273), `before` field; public assistant message at recorded source line 4334. The excerpt is an exact substring of the recorded public assistant message.
- Correction: [NA-0552](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:23273), user message line 4341, 2026-09-14T13:55:34.353Z.

#### GT-045 — How the method is applied and what would count as its contribution

- **Affected wording:** "examined their context, the workflow’s instructions and the recorded decisions to see whether the method worked in practice.".
- **Expected finding:** The paragraph names material and a method but not what the framework’s questions were used to do or how that use was assessed.
- **Clarification target:** Describe the operation linking framework questions to the records and the intended evidence of usefulness.
- **Boundary:** Do not replace assessment of the framework with merely completing the underlying model evaluation.

### C036 — Airtable credential preparation

**Historical correction (author, verbatim):**

> your handoff is, give some context there, and, like, what it means by handoff.

**Evidence and provenance:**

- Passage 1: [NA-0566](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:23856), `before` field; public assistant message at recorded source line 5681. The excerpt is an exact substring of the recorded public assistant message.
- Correction: [NA-0566](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:23856), user message line 5688, 2026-09-14T17:58:23.970Z.
- Related corrections or follow-ups: [NA-0567](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:23894). These are supporting episode evidence, not extra counts of the same issue.

#### GT-046 — Which earlier material the question relies on

- **Affected wording:** "Your handoff".
- **Expected finding:** The phrase does not identify the plan or exchange containing the proposed field values, so the recipient must reconstruct what is being referenced.
- **Clarification target:** Name the relevant plan for the separate workflow keys and enough timing or content to identify it.
- **Boundary:** Do not invent a date; it may be a suitable identifier only if supported.

#### GT-047 — Where the field and compared choices belong

- **Affected wording:** "the **Linked Account** field".
- **Expected finding:** Airtable records are mentioned broadly, but the draft does not identify the table containing the field whose choices are being compared.
- **Clarification target:** Locate the field in the Credentials table and explicitly distinguish the two named values.
- **Boundary:** Do not infer that a missing choice must be created; ask what the proposed value meant.

### C037 — Creating credential records

**Historical correction (author, verbatim):**

> I can complete the Airtable records.  wdym by this ?

**Evidence and provenance:**

- Passage 1: [NA-0583](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:24509), `before` field; public assistant message at recorded source line 27. The excerpt is an exact substring of the recorded public assistant message.
- Correction: [NA-0583](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:24509), user message line 34, 2026-09-15T18:23:01.264Z.

#### GT-048 — What complete requires the author to do

- **Affected wording:** "complete the Airtable records".
- **Expected finding:** The phrase can mean finish existing rows, create new rows, fill fields or establish links; the promised operation is not identified.
- **Clarification target:** State that the work is to create the credential records and link them to the relevant workflows, if that is the established plan.
- **Boundary:** Do not imply those records already exist merely because complete is used.

### C038 — Keys and saved connections

**Historical correction (author, verbatim):**

> why Christine is also we are asking to prepare for an N8N credentials?

**Evidence and provenance:**

- Passage 1: [NA-0584](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:24543), `before` field; public assistant message at recorded source line 27. The excerpt is an exact substring of the recorded public assistant message.
- Correction: [NA-0584](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:24543), user message line 44, 2026-09-15T18:24:11.760Z.

#### GT-049 — How the two colleagues’ actions differ

- **Affected wording:** "prepare the four n8n credentials".
- **Expected finding:** Creating API keys and preparing n8n credentials sound like duplicate work because the draft does not explain that one creates secrets at the provider and the other adds saved connections that use them.
- **Clarification target:** Explain the relationship among provider keys, stored key details, Airtable records and n8n connections at the level needed for this request.
- **Boundary:** Do not assign the colleague a second key-creation task or expose any secret.

### C039 — Comparison terminology

**Historical correction (author, verbatim):**

> it sounds like we are comparing workflows. But actually we are comparing models, no?

**Evidence and provenance:**

- Passage 1: [NA-0587](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:24678), `before` field; public assistant message at recorded source line 8402. The excerpt is an exact substring of the recorded public assistant message.
- Correction: [NA-0587](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:24678), user message line 8409, 2026-09-16T08:34:34.573Z.

#### GT-050 — What objects are compared

- **Affected wording:** "Workflow comparison".
- **Expected finding:** The option name implies comparing workflows even though the description concerns a candidate model and a baseline within a particular workflow.
- **Clarification target:** Name model comparison as the operation and retain the workflow as its scope.
- **Boundary:** Do not erase the separate eligibility-check distinction.

### C040 — Implementation scope

**Historical correction (author, verbatim):**

> implementation details of what? airtable change  implementation details.

**Evidence and provenance:**

- Passage 1: [NA-0594](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:25050), `before` field; public assistant message at recorded source line 8788. The excerpt is an exact substring of the recorded public assistant message.
- Correction: [NA-0594](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:25050), user message line 8805, 2026-09-16T10:23:15.730Z.

#### GT-051 — Which implementation is to be reviewed

- **Affected wording:** "the implementation details".
- **Expected finding:** The paragraph mentions both putting a structure in place and building a Skill, leaving the implementation-details request open between them.
- **Clarification target:** Identify the proposed Airtable changes as the subject of the requested confirmation.
- **Boundary:** Do not ask for approval of an unrelated Skill implementation.

### C041 — Summaries across records

**Historical correction (author, verbatim):**

> There are two things there. There are two active candidates. I don't understand. It's not understandable why.

**Evidence and provenance:**

- Passage 1: [NA-0596](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:25125), `before` field; public assistant message at recorded source line 8861. The excerpt is an exact substring of the recorded public assistant message.
- Correction: [NA-0596](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:25125), user message line 8868, 2026-09-16T10:29:58.834Z.

#### GT-052 — What the two displayed entries represent

- **Affected wording:** "Freeform — Preparing evidence — confirm references; FX — Reviewing results — agree outcome".
- **Expected finding:** The condensed value does not make clear that one candidate model can have separate assessments for two workflows; the reader can mistake the entries for two candidate models.
- **Clarification target:** Explain the record being viewed and distinguish the candidate-model identity from its workflow-specific assessments.
- **Boundary:** Dashes themselves are not an error; the issue is the unstated relationship and unit.

### C042 — Locations of linked evidence

**Historical correction (author, verbatim):**

> It is in different table? It is in linear?

**Evidence and provenance:**

- Passage 1: [NA-0597](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:25178), `before` field; public assistant message at recorded source line 8873. The excerpt is an exact substring of the recorded public assistant message.
- Correction: [NA-0597](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md:25178), user message line 8880, 2026-09-16T10:31:22.220Z.

#### GT-053 — Where the underlying assessment records live

- **Affected wording:** "the linked assessment records".
- **Expected finding:** The phrase does not identify whether the supporting records are in another Airtable table, Linear or elsewhere.
- **Clarification target:** Identify the Model Evaluations table in Airtable and distinguish its assessment records from linked Linear work items.
- **Boundary:** Do not imply the summary is the sole storage location or create another copy of the assessment.

## Curation decisions

- This selection is anchored in the author's specific clarification requests, including “of what?”, “which one?”, “what happens?”, “who does it?” and “for what purpose?”. General dissatisfaction alone was not treated as a sufficient label.
- Repeated attempts to fix one local ambiguity are retained as linked evidence, not new scored issues. Examples include the repeated missing-row references, repeated workflow-selection corrections and successive clarification of credential setup.
- The final context review removed the standalone framework questions, the “five” lead-in and the status-dictionary example from scored cases because their surrounding text could supply the proposed missing meaning. The workflow-output paragraph retains only its set-overlap issue: its next sentence already identifies the writing as results. A historical complaint is not automatically a valid positive label under the supplied context.
- Multiple vague words that resolve through the same missing relationship are counted together. For example, “enough context … usable” is one sufficiency issue, not a separate score for every word.
- Some public replies only reported that a document was edited; some were interrupted. No unseen revised paragraph has been reconstructed or presented as an accepted repair.
- The abandoned “ghost rows” explanation was not used as a reliable substantive basis; later history changed its factual account. Pure tone preferences, unwanted meeting offers and requests to change the underlying operational decision are not scored as ambiguity here.
- Business facts, historical counts, access claims and legal/privacy assertions inside examples were not revalidated. Expected findings concern what the wording communicates, and clarification targets avoid treating unverified claims as facts.
- A user complaint establishes that the wording caused a recorded difficulty. It is not, by itself, proof that every wider reading or every possible recipient must find it ambiguous. This set therefore fixes the excerpt-level reading conditions and retains limits on each finding.

## Source files

- [Readable historical collection](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.md).
- [Full selected public messages and response windows](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-examples.json).
- [Original archive manifest](/Users/nsstorm/Desktop/projects/AIOpsMan/research/evidence/nonambiguity/nonambiguity-sources.json).

## Verification

- 42 case IDs paired exactly between the two files.
- 53 unique expected-issue IDs; every affected span exists in its input case.
- All excerpts and correction quotations checked as exact substrings of the saved source collection.
- Provider coverage by case: claude: 31, codex: 11.
- Source episode links resolve to the corresponding NA identifier in the readable collection.
- Input contains no answer labels, historical correction quotes, repair wording or source links added by the curator. Original embedded links remain historical text and are not to be opened during detection.
- Additional original-archive check: 88 unique public messages referenced; 50 match the original public text at the recorded archive line, 38 rely on the saved collection because their original archive path is unavailable. No conflicting text was found among the accessible originals.
- Source JSON SHA-256: `061d9045e9d9de8e50714e5ab8bc2bffce3bbb8f51b72288506647ee8cd65b3f`.

## Additions accepted on 2026-10-04 (GT-054 to GT-070)

Found among detector items that matched none of GT-001 to GT-053, proposed by Opus 5.5 reviewers, accepted by the author. Full rows in `proposals/proposals.md`.

#### GT-054 — C003 (proposal P1-01)

- **Affected wording:** "when guarantees are needed"; "ordinary work"; "important repeatable workflows".
- **Expected finding:** Which work the recommendation routes through StoryOS-managed workflows and which goes straight to provider tools. The reader cannot tell what "guarantees" are guarantees of (approval recorded, a quality standard applied, evidence kept, a fixed procedure followed), and the diagram's criterion (guarantees needed) and the paragraph's criterion (important and repeatable) may define the same set or two different sets: a one-off but approval-bound request is managed under the first reading and direct under the second.
- **Clarification target (example):** Example only: "Work goes through a StoryOS-managed workflow when the company needs [a stated guarantee, for instance a recorded approval or retained evidence]; other work uses provider tools directly. [State whether 'important repeatable workflows' is the same set or a subset.]"
- **Found by:** fast-opus (#13, #14, #16), slow-opus (#19, #21, #25, #27), strong-opus (#21, #22, #25, #26), plain-opus (#13, #14, #17), slow-haiku (#3, #4); 5 of 7

#### GT-055 — C008 (proposal P1-02)

- **Affected wording:** "14/20 predictions correct".
- **Expected finding:** Whose predictions these were, what they predicted, and what they were checked against. Competing readings: someone predicted each skill's verdict before judging and 14 matched the retro verdicts; the method or a hypothesis predicted some other outcome per skill; or the predictions concern something outside the verdict counts above. The reader also cannot tell how the 14/20 relates to the 18/2/0/0 tiles.
- **Clarification target (example):** Example only: "14 of 20 [stated predictions, e.g. the verdict expected for each skill before it was judged] matched the verdict it received."
- **Found by:** fast-opus (#57), slow-opus (#66), strong-opus (#67, #68), plain-opus (#55), fast-haiku (#17), strong-haiku (#9); 6 of 7

#### GT-056 — C009 (proposal P1-03)

- **Affected wording:** "SEL".
- **Expected finding:** What SEL stands for or names: the thing whose "shape" is listed as a completed foundation. The stakeholder cannot tell whether it is the whole evaluation method, a lifecycle a skill passes through, a document or a system, so a third of the "foundations are complete" claim has no identifiable subject.
- **Clarification target (example):** Example only: "the [expanded name of SEL, e.g. the skill evaluation method]'s shape: three activities, gate, assess and prove, ..."
- **Found by:** fast-opus (#58), slow-opus (#69), strong-opus (#70), plain-opus (#57), strong-haiku (#10); 5 of 7

#### GT-057 — C009 (proposal P1-04)

- **Affected wording:** "Benefit-case score"; "the design file's case".
- **Expected finding:** What the 0–100 score measures, and therefore what "scored 82" says about the skill. Competing readings: the score rates the skill's actual benefit (so the skill is good), or it rates the written case made for the skill's benefit (so its justification is strong, saying nothing about real-world delivery). The update itself then separates "the design file's case" from "the skill's real-world delivery" without saying which of the two the battery scored, and refers to "the design file" as an existing object before saying that per-skill design files are only proposed.
- **Clarification target (example):** Example only: "a 0–100 score of how strongly the written case for a skill's benefit is made [if that is what it measures], not of the benefit the skill delivers in use. ... We also separated these two objects: the case argued in a skill's design file, and the skill's real-world delivery."
- **Found by:** fast-opus (#68, #71), slow-opus (#76, #78), strong-opus (#79, #83, #86), plain-opus (#64, #66), fast-haiku (#23), strong-haiku (#18); 6 of 7

#### GT-058 — C011 (proposal P1-05)

- **Affected wording:** "v0.6", "v0.7".
- **Expected finding:** What is versioned, and so whether the two runs are true repeats. Competing readings: v0.6 and v0.7 are only labels for the first and second run of an unchanged setup, so the non-overlapping split sets show judging instability; or they are two versions of the judging sheet, question bank or prompt, so the different split sets (and the 94% to 88% drop) may come from the change between versions. The setting says "repeated judging runs", while version numbers suggest something changed.
- **Clarification target (example):** Example only: "v0.6 and v0.7 are [the two runs of the same unchanged judging sheet / two versions of the judging sheet, differing in ...]."
- **Found by:** fast-opus (#81), slow-opus (#87), strong-opus (#94), plain-opus (#75), fast-haiku (#27); 5 of 7

#### GT-059 — C020 (proposal P2-01)

- **Affected wording:** "is this still used"; "settles it"; "the workflow has either stopped or nobody is using what it produces".
- **Expected finding:** The recipient cannot tell what "used" means, so cannot tell what an old newest-record date would show. Reading A: "used" means the workflow still runs and delivers results; then a March date shows it has stopped delivering. Reading B: "used" means someone consumes the results; the check measures results arriving, not results being read, so it cannot settle B. The conclusion clause names both readings ("stopped" and "nobody is using what it produces") and gives no link between the newest-record date and the second one, while the sentence says the check "settles it" "outright".
- **Clarification target (example):** *Example only:* "The one check I couldn't run would show whether each workflow is still producing results: the date of the newest record in its Airtable table. If a table's newest record is from March, the workflow has produced nothing since then. That shows whether results are still arriving, not whether anyone reads them."
- **Found by:** fast-opus #128, strong-opus #160 and #161, plain-opus #121 and #122, strong-haiku #51 (4 of 7)

#### GT-060 — C023 (proposal P3-01)

- **Affected wording:** "for the first time" / "the first complete register in over a month".
- **Expected finding:** Whether the table has ever had this coverage before. The headline says it is complete for the first time ever; the closing sentence says it is the first complete register in over a month, which implies it was complete before 27 July. The reader of the progress bullet cannot tell which claim governs, so cannot tell whether this is a new state or a restored one.
- **Clarification target (example):** (Example) "Every live workflow now has a row in the Workflows table, for the first time since [the date coverage was last complete, or: the first time ever — to be confirmed]."
- **Found by:** plain-opus #132 (1 of 7)

#### GT-061 — C024 (proposal P3-02)

- **Affected wording:** "the 26 unresolved pairs", "the 16 archived-target and 11 no-URL rows", "resolve", "clean".
- **Expected finding:** What the remaining work items are and what is done to them. "Pairs", "archived-target" and "no-URL" are audit categories never introduced; nothing says that 26 + 16 + 11 = 53 are the untrusted items of the headline, so the reader cannot tell whether the next work covers all the untrusted prompts or only part. "Resolve" and "clean" leave the operation open: matching a row to its workflow prompt, correcting text, archiving or deleting rows are all plausible and lead to different end states for the table.
- **Clarification target (example):** (Example) "Of the 53 untrusted rows: 26 are [what an unresolved pair is], which we will [operation]; 16 point at workflows n8n has archived and 11 have no workflow link [to confirm], which we will [archive / delete / fix — to be stated] once the rule is agreed."
- **Found by:** fast-opus #154, #155; slow-opus #159, #160, #161; strong-opus #195, #196, #197, #198; plain-opus #144, #145; fast-haiku #58; strong-haiku #60 (6 of 7)

#### GT-062 — C025 (proposal P3-03)

- **Affected wording:** "The 18 stale copies", "refresh it".
- **Expected finding:** What the 18 are copies of, and what makes them stale: stale against which version (the prompt the workflow runs now, a later table edit, a document) and by what test (text differs, older timestamp, workflow changed since). The same missing reference version leaves "refresh it" without a source. The author's own correction asks it: "why u think they are stale?"
- **Clarification target (example):** (Example) "The 18 table rows whose prompt text differs from the prompt their workflow currently runs [comparison to be confirmed]: … retire the row, or overwrite it with the running prompt and …"
- **Found by:** fast-opus #158, #161; slow-opus #165, #166, #169; strong-opus #202, #203, #206; plain-opus #149, #152; fast-haiku #59; strong-haiku #61 (6 of 7)

#### GT-063 — C029 (proposal P3-04)

- **Affected wording:** "what quality trade is acceptable".
- **Expected finding:** What quality is traded against, and so what Christine actually decided. Competing readings: how much quality loss is acceptable for lower cost (a cheaper model), for speed, or which kinds of quality failure may be tolerated relative to others. Each implies a different constraint on the test plan the sentence says is next.
- **Clarification target (example):** (Example) "…and told us how much [quality loss / which kinds of error — to be confirmed] is acceptable in exchange for [cost / speed — to be confirmed]…"
- **Found by:** fast-opus #180; slow-opus #188; strong-opus #224; plain-opus #172; fast-haiku #66 (5 of 7)

#### GT-064 — C031 (proposal P3-05)

- **Affected wording:** "nothing safety-class disagrees", "cost is in band".
- **Expected finding:** The test that permits the switch. "Safety-class" is an undefined category of output (or of disagreement), and "disagrees" leaves open what is compared with what and whether any difference or only a reversed decision counts. "In band" names no band and no place it is set, so the reader cannot tell whether a cost range exists or is still to be agreed.
- **Clarification target (example):** (Example) "If the candidate never [differs from the current model on a safety decision — definition to be confirmed], its cost stays within [the agreed range — not yet set] and no run errors, the workflow owner publishes the switch."
- **Found by:** fast-opus #191, #192; slow-opus #198, #199; strong-opus #234, #235; plain-opus #182, #183; fast-haiku #70, #71; slow-haiku #26; strong-haiku #69, #70 (7 of 7)

#### GT-065 — C031 (proposal P3-06)

- **Affected wording:** "Rollback is restoring the previous n8n version. That works because adapted prompts are new rows, never edits of the live one.".
- **Expected finding:** Why restoring a workflow version also restores its prompt. The reason given depends on a link the paragraph never states: that each workflow version points at a specific prompt row in a table, so the old version still finds its old, unedited row. Without it the reader cannot tell whether rollback restores the prompt or only the workflow, and "rows" has no table and "the live one" is unclear between the live row and the live prompt.
- **Clarification target (example):** (Example) "Rollback is restoring the previous n8n version. That restores the old prompt too, because each version reads its prompt from [the prompts table — to confirm] by row, and an adapted prompt is added as a new row rather than overwriting the one the live version uses."
- **Found by:** fast-opus #197; slow-opus #204; strong-opus #240; plain-opus #187 (4 of 7)

#### GT-066 — C033 (proposal P4-01)

- **Affected wording:** "what an evaluation needs is there or one step away".
- **Expected finding:** The reader cannot tell which of the five listed ingredients are usable now and which still need a step, nor what that step is. Competing readings: everything listed can be used immediately and "one step away" is loose phrasing; or one or more items (for example the saved runs or the trusted prompts) still need preparatory work before a first evaluation can start.
- **Clarification target (example):** *Example:* "Most of what an evaluation needs is already there: saved runs to replay, Christine's inputs on what counts as correct, her July tests and the largest measurable spend. One step remains: confirming that the stored prompts are the ones running." (Which item needs which step must come from the author; not invented here.)
- **Found by:** fast-opus, slow-opus, strong-opus, plain-opus (4 of 7)

#### GT-067 — C033 (proposal P4-02)

- **Affected wording:** "her July tests".
- **Expected finding:** The reader cannot establish what the July tests were or what they contribute to an evaluation. Competing readings: tests of candidate models on this family's work (direct prior evidence), tests of the workflow's prompts or outputs (usable as test cases), or Christine's own manual checks of moderation decisions (usable as reference answers). Each makes the item a different kind of asset.
- **Clarification target (example):** *Example:* "her July tests, in which she checked [what she tested] against [which records]" (content to come from the author).
- **Found by:** fast-opus, slow-opus, strong-opus, plain-opus, slow-haiku (5 of 7)

#### GT-068 — C034 (proposal P4-03)

- **Affected wording:** "the family's workflow owner" ... "per workflow" ... "that owner".
- **Expected finding:** The reader cannot tell who judges the results and writes the bar when a family contains several workflows. Competing readings: one owner for the whole family judges and sets the bar for every workflow in it; or each workflow's own owner judges and sets the bar for that workflow, so a family evaluation may involve several people. The singular "the family's workflow owner" and "that owner" pull towards the first; "decided per workflow" pulls towards the second.
- **Clarification target (example):** *Example:* "each workflow's owner judges the results for that workflow and writes its bar before the results exist" or "the family's owner judges the results for all its workflows", whichever the author means.
- **Found by:** fast-opus, slow-opus, strong-opus (3 of 7)

#### GT-069 — C037 (proposal P4-04)

- **Affected wording:** "their Owner".
- **Expected finding:** The recipient is asked to accept a role but cannot tell what he would own. "Their" can refer to the keys, the service accounts or the Airtable records (the nearest plural). Owning the keys or accounts means being responsible for the credentials themselves; owning the Airtable records means being responsible for keeping the descriptive entries current.
- **Clarification target (example):** *Example:* "Could you also confirm whether you're happy to be listed in Airtable as the Owner of the four keys?" (or of the records, whichever the author means).
- **Found by:** fast-opus, slow-opus, strong-opus, plain-opus (4 of 7)

#### GT-070 — C038 (proposal P4-05)

- **Affected wording:** "audit checks and reporting preparation".
- **Expected finding:** Christine cannot tell what these two steps are or whether either is hers. Competing readings: they are steps she is expected to do as part of her n8n setup work (which would affect the capacity she is asked to estimate); or they are steps for the author or someone else, which she only waits on. What is audited and what reporting is prepared is also unstated.
- **Clarification target (example):** *Example:* "... once the n8n setup is done, I have run the audit checks on [what], and [who] has prepared the reporting for [what]." (Contents and actors to come from the author.)
- **Found by:** fast-opus, slow-opus, strong-opus, plain-opus, strong-haiku (5 of 7)

