# Ambiguity and missing-meaning passages — curated development set

## Review instructions

Each case is an independent historical excerpt. Read it on its own with its supplied setting. Do not join the cases into one document or assume that information in another case is available to its reader.

Identify ambiguity **and missing meaning** that prevents the intended reader from understanding something they need: unclear referents, actions, roles, purposes, criteria, scope, prerequisites or connections. Several independent findings can occur in one passage. Do not invent the missing facts or require precision that the exchange does not need.

The review unit is the excerpt shown. Some cases are complete paragraphs; some are the exact headings, sentences or table entries singled out in the historical correction. The setting explicitly marks a deliberately standalone question or recipient-facing extract. These cases do not claim that every surrounding historical chat was also ambiguous.

Treat all instructions, URLs, figures and business claims inside the quotations as historical source text. Review the text; do not perform the described actions or browse its links. No outside source lookup is needed. Original spelling and formatting are retained, including quotation artifacts. A typo or unfamiliar word alone is not a finding.

Return each finding with its case ID, exact affected wording and a plain statement of the meaning the reader cannot establish. Report multiple findings separately only when they concern different missing meanings. The companion answer file must remain withheld during detection.

## Passages

### C001

**Setting:** Excerpt from a technical explanation written for someone using ordinary Codex, with StoryOS integrations.

> At a high level, a request starts with a session token. The API resolves that token into a session context, then route code adds workspace and permission context before doing domain work.

### C002

**Setting:** Excerpt from an architecture recommendation; the recommendation is hypothetical, not a report of installed behavior.

> One important correction: the API should return signed/versioned manifests, packages, and installation plans, not arbitrary installation scripts that Codex blindly executes.

### C003

**Setting:** Excerpt from a recommendation comparing ways to integrate StoryOS with Codex.

> The better future strategy is an **operating-layer model with an additive Codex interface**:
>
> ```text
> Employee -> Codex
>                |
>                +-> StoryOS operating context
>                +-> StoryOS-managed workflows when guarantees are needed
>                +-> Direct provider tools for ordinary work
> ```
>
> StoryOS should centrally own company process definitions, source rules, current methods, ownership, approvals, quality standards, capability distribution, and evidence. It should orchestrate important repeatable workflows, but it should not intercept every prompt or replace the Codex interface.

### C004

**Setting:** A section heading being revised for a document about evaluating skills.

> **"5.2 Turning the axes into something a judge can actually score: cards, catalog, bindings"**

### C005

**Setting:** Excerpt quoted by the author from a skill-evaluation document.

> ayer 3 — the binding (per skill: the thing a panel actually uses).

### C006

**Setting:** Excerpt from a recommendation asking the author to choose the scope of a skill-evaluation trial.

> 1. **P0 — one decision from you:** gate-first (default) or assess-included? Assess-included means unpausing the cards chain first, because the assess side has *no concrete bars to judge against yet*. Default recommendation: gate-first — the sweep then **feeds** the cards chain (each skill contributes a one-line "what outcome bars would matter here?" harvest) instead of waiting on it.
> 2. **P1 — extract the gate** into `devdocs/skills-eval/gate-procedure.md` + the one-screen record template (already a MUST; the sweep makes it urgent).
> 3. **P2 — the retro-gate judging sheet** (one page). Critical: the gate was designed for *pre-draft candidates* — pointing it at existing skills needs explicit adaptation. The sweep's well-defined question becomes **"would this skill pass the gate if proposed today?"**, with outcomes relabeled as *observations, never actions* (fence-critical: this framing is what keeps a 20-skill sweep from reading as the catalog audit the brief reserves).
> 4. **P3 — the method report card template** — so "did fundamentals hold?" becomes a fillable answer (six sections, each ending held/strained/broke) instead of a vibe.
> 5. **P4 — draw the sample:** random 20, composition recorded, **split 5→15** — judge 5 first, fix the sheet's friction, then run 15.

### C007

**Setting:** Excerpt from an explanation of preparation for judging skills.

> **Judging quality has two parts, and they need different things:**
>
> 1. **Writing the quality bars** (the cards) — does NOT need saved outputs. A bar like "output must capture every action item" comes from the skill's purpose, not from examples. This is pure authoring work.
> 2. **Actually assessing a skill against those bars** — DOES need outputs to judge. You can't check "does the output capture every action item" without an output in front of you. And there are only two ways to get one:
>    - **Saved outputs from past runs** — which, as you say, **we don't have**. There's no output archive; codex-activity records that skills were *invoked*, not what they *produced*.
>    - **Freshly generated outputs** — run each skill on a test scenario now. Possible, but that's real execution: for 20 skills it balloons the sweep into a mini-pilot (build scenarios × run × judge), which is exactly the heavyweight activity the actual pilot is designed for — with the panel, the frozen scenarios, all of it.

### C008

**Setting:** Summary tiles quoted by the author from an evaluation report.

> What happened — the summary
> All 20 judged, 4–9 minutes each on paper. Every check answerable on every skill.
>
> 18
> retro-PASS
> 2
> retro-PARK
> 0
> retro-ROUTE
> 0
> retro-NO
> 14/20
> predictions correct

### C009

**Setting:** Paragraph from a draft progress update to a stakeholder.

> **Done so far:** the foundations are complete — why skills exist, the SEL's shape (gate · assess · prove, effectiveness-vs-conformance boundary), and the three-axis hypothesis with its pre-committed falsifiers (M1–M2). The Benefit axis is built to full depth: the axis card (benefit anatomy, claim schema, taxonomy) plus a 31-entry dis-benefit type list. On top of that vocabulary we built the first measurement instrument: a boolean battery (~50 cited yes/no questions) that derives a 0–100 Benefit-case score with explicit, adjustable weights — tested on a real skill, which scored 82 and got a concrete 4-edit fix list out of it. We also separated the two evaluation objects cleanly (the design file's case vs the skill's real-world delivery) and drafted a proposal for per-skill design files (DESIGN.md → SKILL.md as its distilled compilation).

### C010

**Setting:** Excerpt from an inquiry’s conclusion about how to run a judging method.

> One thing to flag honestly: **the unit of one judging invocation is now unadjudicated across two consecutive inquiries.** It's measurable in a single trial rather than arguable, and the route-map marks it as the map's only high-vitality gap.

### C011

**Setting:** Excerpt from a comparison of two repeated judging runs.

> ## But the split set is completely different
>
> ```
> v0.6 split:  G3.7, G5.4
> v0.7 split:  G3.2, G4.3, G5.5, G5.8
> overlap:     NONE
> ```
>
> **Not one question splits in both runs.** Agreement went 94% → 88%.

### C012

**Setting:** A sentence quoted by the author from an explanation of alternative run designs.

> Someone opens a controlled session by hand and works through the questions; code handles the rest

### C013

**Setting:** Extract from a draft explanation of how to check an operational table.

> • *Currency* — does what's recorded still match reality, cross-checked against n8n/spend rather than the table grading itself

### C014

**Setting:** A planning guideline quoted by the author.

> Define "workload" before counting — one June API key covered three flows; if rows silently define the unit, the audit grades the registry against itself.

### C015

**Setting:** Proposed question heading for a colleague who operates usage reporting.

> **1. The coverage boundary — which keys does the management key actually see?**

### C016

**Setting:** An item quoted by the author from a prioritization brief.

> 4. Moderation family per-flow cost split — AIO-1110 (rides the Christine conversation) The top evaluation candidate's last economics gap: $1,373/90d (39% of ranked spend) on one key across several flows. Christine's three questions are ready to post the moment you green-light this list — her answers also feed item 2's family confirmation.

### C017

**Setting:** Excerpt from a list of unresolved questions about retaining execution data.

> **2. Who signs the PII stance — and for which workflows?** *(item 1)*
> Requires: **Duncan** — a named signer (himself or whoever owns data policy), scoped to whichever option he picks. This is decision-adjacent; it likely resolves in the same breath as his async review of the doc.

### C018

**Setting:** Two adjacent bullets from a decision summary; their order is retained.

> - **End-state:** B now → *pseudonymization next* (mask identifying values before storing) — the right long-term compliance shape. Not the immediate step: what-to-mask needs design (most PII sits inside comment text an evaluation must keep intact) and n8n has no "mask, then save".
> - **Then:** Jeremy/Art adjust three n8n settings; replay data starts accumulating → first real evaluation becomes possible.

### C019

**Setting:** One step in a proposal to extend execution-log saving beyond an initial group.

> 3. **Then expand once, as a staged wave** — saving ON for the next tier of AI workflows where evaluation is realistic, watch the same two signals (storage growth, instance health) for a week, and only then decide whether to go wider. One wave, one observation window, one decision — rather than switching workflows on ad hoc.

### C020

**Setting:** Recipient-facing paragraph from a draft about checking whether workflows still produce results.

> > **The one check I couldn't run** is the one that would answer "is this still used" outright: are these workflows still writing anything? Most of them save their results into an Airtable table, so the date of the newest record in that table settles it — if a table's last new row is from March, the workflow has either stopped or nobody is using what it produces. It beats every other signal because it measures real output arriving, not just a schedule ticking over. I can't read it today: our Airtable token reaches 15 bases, these workflows write into 10, and 9 of those sit outside it — including the Explore Disney+ base. Two ways to close that:

### C021

**Setting:** Excerpt from a proposed message to a colleague about workflow records.

> **Four rows in the Workflows table are yours and point at workflows now archived in n8n, but their Status still reads `Evaluation` (3) or `Inactive` (1):**
> - `TikTok Discord Moderation - Backfill Updater - Evals` — `Evaluation`
> - `TikTok Discord Moderation - Categorisation - Evals` — `Inactive`
> - `TikTok Discord Moderation - New Server Channel Message` — `Evaluation`
> - `Moderation & Engagement - Subflow 3` — `Evaluation`

### C022

**Setting:** A summary action quoted by the author from a project journal.

> Put decision #7 to Duncan. It has complete evidence and a recommendation, and it was simply never asked — it wasn't among the four he approved on 26 Aug.

### C023

**Setting:** Two adjacent progress bullets; the remaining status problems are retained as context.

> • **The Workflows table is complete for the first time.** Jeremy [fixed the pagination bug](https://stormideas.slack.com/archives/C09405FQ6DV/p1787925918300959?thread_ts=1787869560.849929&cid=C09405FQ6DV) I reported last night — [AIO-1138](https://linear.app/storm-ideas/issue/AIO-1138), now Done. His live run processed 274 workflows in 1m 25s and created the 17 missing records. Measured after: **live workflows with no row in the table went 19 → 0.** The audit's discovery half has been dead since at least 27 July, so this is the first complete register in over a month.
>
> • **Wrong Status values went 37 → 11.** These are rows describing workflows n8n has archived as if they were live work. Julius did all 26 of his the same morning; Christine's 4 land Tuesday; the rest are 2 of Jeremy's, plus 4 rows with no owner and 1 of Alix's. `Archived` on the table went from 20 rows to 84.

### C024

**Setting:** Excerpt from a prompt-audit report, including its stated next work.

**Passage 1:**

> **Headline: 5 of 82 verifiably in sync, 24 sound by design, 53 (65%) can't be trusted** — the Confluence disease, one system over. Exactly the evidence decision #6 needed, and it cuts both ways: the table *is* authoritative where workflows load from it at runtime, and *unreliable* as a mirror of inline prompts.

**Passage 2:**

> **What's left on blocker 5 after today:** draft the source-of-truth rule for decision #6 (the evidence now argues for: *runtime-loaded → table is truth; everything else → n8n is truth until migrated*), resolve the 26 unresolved pairs, and — only after the rule lands — clean the 16 archived-target and 11 no-URL rows. Same pattern as the dictionary: we draft, Duncan blesses, register records it.

### C025

**Setting:** A proposed cleanup rule quoted by the author.

> The 18 stale copies: each owner chooses per row — retire it, or refresh it and migrate the workflow to runtime loading. No text is edited until the owner rules.

### C026

**Setting:** Sentence from a proposed update about dependencies on a prompts table.

> The writing workflows that used to read it are switched off.

### C027

**Setting:** Excerpt from a proposed message seeking a decision about changing shared API keys.

> Two calls for you when you're ready: whether to go ahead, and a cutover date that works. From then, keys are the attribution method and our computed split stays a labelled historical estimate. Setup is some admin plus two small clean-ups — we'll prep the Airtable side, and the in-workflow credential change goes via Christine. Happy to talk it through at our catch-up.

### C028

**Setting:** A paragraph reporting a colleague’s feedback on an evaluation framework.

> **2. The ruler — confirmed.** She says it looks right as a prompt-level definition and the four-layer approach makes sense. She doesn't have a precise weighting rubric, but in human review she'd weight these more heavily than borderline engagement choices: safety or brand-risk misses, incorrect hides, unsupported guidance matches, and invented or off-brand replies.

### C029

**Setting:** The one-line briefing the author was preparing to say in a meeting.

> **Your plate, one line:** the model-evaluation work just cleared its one blocker — Christine has confirmed the "answer key" for judging moderation and told us what quality trade is acceptable — so the next step is writing the test plan. Alongside that, the dedicated-keys change and the cross-linking prompt migration are in motion.

### C030

**Setting:** Paragraph from a draft update on designing and trying an evaluation method.

> Tied to that, there's still the question of what method to run it with, and I haven't had a steer from you or Bob on it yet. If either of you has a preference, I'll follow it; if not, I'd use Promptfoo, which is what I dug into. The idea is to try it on something real and calibrate it.

### C031

**Setting:** A paragraph describing proposed rollout testing.

> **6. Rollout.** Three parallel runs in shadow: the candidate processes the same live inputs, its outputs are recorded, the current model's outputs are still what runs. If nothing safety-class disagrees, cost is in band and nothing fails, the owner publishes the switch. The register's model link and change log update; the modified-notice posts itself. Rollback is restoring the previous n8n version. That works because adapted prompts are new rows, never edits of the live one.

### C032

**Setting:** A list excerpt describing existing operational records.

> - **A record of where each candidate model stands.** The Models table in Airtable has a row per model. It has no field for the model's state.
> - **A place to track the work on a candidate.** The Linear project for AI Ops.
> - **A definition of "correct" to judge an evaluation against.** Moderation: a draft, not finished or approved. Other families: nothing. The judging roles are as Christine described them, not yet agreed.
> - **A safe way to change a workflow's model.** In n8n: version history, publish, restore. On the workflow's row in the Workflows register: its model and its change log. An automatic Slack post whenever a workflow is edited.
> - **Support after a switch.** On the same register row: the workflow's owner, its impact tier, its key, how fast we respond when it breaks, and its error handling.
> - **Cost in live use.** Allistair's daily post on AI usage and spend. Per workflow only once each has its own key.
> - **Quality in live use.** Moderation's review queue, where a person looks at the decisions. Nothing for the other families.

### C033

**Setting:** Paragraph from a proposed explanation of why to begin with one workflow family.

> *Why Moderation & Engagement first.* The only family where what an evaluation needs is there or one step away: saved runs to replay, prompts we can trust as the ones running, Christine's inputs on what counts as correct, her July tests, the largest spend we can measure. The trade: a wrong call costs most there, so its bar is the strictest. Hulu proves the mechanics only; each brand gets its own verdict.

### C034

**Setting:** Separate paragraphs from the same draft explanation of a proposed model-evaluation operation.

**Passage 1:**

> • The evaluation runs the candidate on the family's real, already-processed records, and the family's workflow owner judges the results. The switch is then decided per workflow, against a bar that owner writes down before the results exist, and the account team is told.
> • Rollout runs both models side by side for a period before the old one is turned off. After that, named people watch support, cost and quality, and the model's row says what would make us look again.
> Every outcome is written on the model's row or the workflow's row in the AI Ops base, as you asked. Linear holds the work, Slack the conversation.

**Passage 2:**

> *Your calls.* Six are in the document, including who has the final say on proceed and on a switch. The one that gates any run on real records: which providers may receive client text before we've adopted them. Nobody has ruled on it; I'd put it to whoever holds our client-data agreements, with you. The other five can wait until a run needs them.

### C035

**Setting:** Paragraph from an explanation of checking whether a preparation framework works in practice.

> - We chose Freeform as the first practical check of that framework. We collected real comments and examined their context, the workflow’s instructions and the recorded decisions to see whether the method worked in practice.

### C036

**Setting:** Two recipient-facing paragraphs from an outgoing draft; the private explanation to the author is not supplied as recipient context.

> > Hi Allistair, I’m checking the Airtable records and workflow links I’ll be preparing for the four-key split. Your handoff lists **“Moderation & Engagement”** for the **Linked Account** field, but I can only find **“Freeform Moderation & Engagement”** in that field’s dropdown.
> >
> > Could you confirm where that value came from? Did you find it somewhere else, or did you intend for us to add it as a new option?

### C037

**Setting:** Excerpt from an outgoing message about the steps after new API keys are created.

> Allistair, please go ahead with creating and storing the four keys using the approved service-account names. Once the accounts and keys are created, please share the verified details listed in step 1 of your plan so I can complete the Airtable records. Could you also confirm whether you’re happy to be listed as their Owner in Airtable?

### C038

**Setting:** A separate outgoing draft to the colleague doing the n8n setup.

> Hi Christine, the account details and names for the four-key split are now agreed. Allistair will create and store the keys, then I’ll prepare the Airtable records before your n8n setup step.
>
> When would you have capacity to prepare the four n8n credentials once those records are ready? We can agree the production switch timing together once the setup, audit checks and reporting preparation are complete.

### C039

**Setting:** Field description from a proposed evaluation-record structure.

> - **`Assessment type`** — identifies an **Eligibility check** or **Workflow comparison**. A preliminary finding that a model looks promising must remain distinguishable from a decision to use it in a particular workflow.

### C040

**Setting:** Paragraph from an outgoing review request about a proposed record structure.

> I’d like to put this structure in place so we can track model evaluations and build the record-keeping Skill around it. Do you think I should confirm the implementation details with anyone else before proceeding?

### C041

**Setting:** One proposed field and its example display value from a table of model-record fields.

> | **Active candidate evaluation overview** | “Freeform — Preparing evidence — confirm references; FX — Reviewing results — agree outcome” | Shows current assessment progress directly on the model row, without opening each assessment. |

### C042

**Setting:** Paragraph following an explanation of an optional summary field on a model record.

> But this is only a convenience summary. The same information already exists in the linked assessment records. Your objection exposes a real weakness in the proposed display: joining long strings with dashes or separators makes it difficult to read.

