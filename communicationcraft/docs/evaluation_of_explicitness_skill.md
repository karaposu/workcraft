
# The evolution of the explicitness test

How a reliable LLM detector for missing meaning in text was built between 29 September and 7 October 2026: every approach tried, how it was tested, what came out, why it failed or worked, and what it led to. It ends with a method for building a detector of the same kind for any other check, and a list of things not to repeat.

**Why this document exists.** The intermediate experiment folders, runs, scoring files and inquiry notes will be deleted. What remains is:
- the latest skill (`non-explicitness-detection`, with bank version 6.7.2 as the target);
- the fix skill (`non-explicitness-fix`);
- possibly the benchmarks.

This document carries the knowledge of how we got there, so that the next detector (for fidelity, aspect, consistency or anything else) does not repeat our mistakes or re-test options we already know the answer to.

**How to read it.**
- Section 1 defines the terms.
- Section 2 states where we ended up.
- Section 3 gives the whole path on one page.
- Sections 4–6 tell the story in three eras, approach by approach.
- Section 7 explains how to measure a detector honestly.
- Section 8 is the reusable method.
- Section 9 lists what not to repeat.
- Section 10 lists what is still open.

Numbers are as measured at the time. Every number belongs to a specific benchmark, reference and judge, which are named with it. Numbers from different judges or reference lists are not comparable.

---

## 1. Terms

| Term | Meaning |
|---|---|
| **Explicitness gap** | A place where the wording demands something particular (which one, of what, who, what is done, by what criterion, which system, when or where, how things connect) and the text does not single it out among the alternatives it puts in play. A property of the text, not of a reader. |
| **Demand test** | Is something particular needed here? |
| **Sufficiency test** | Does the text single it out, at or before the point (or in the very next sentence)? |
| **Bank** (explicitness bank, codebook) | The written question list plus its rules, answer values and output format. A model answers it sentence by sentence. The technical name for the method is *LLM annotation with a written codebook*. |
| **Slot** | The kind of particular the wording needs: which one, of what, which meaning, what it contains, who, what is done, by what criterion, by what relation, per what unit, which system, when or where. |
| **Trigger** | Wording that nominates a place to check: "the X", a pronoun, a passive, a judgment word, an action noun. |
| **Answer values** | **QUOTE**: supplied; give the words. **LATER**: supplied only after the next sentence. **MULTIPLE**: two or more candidates fit. **CONFLICT**: two places disagree. **CANNOT**: not supplied. **UNSPECIFIC**: an earlier mention is fuller than this re-mention. **NOT-DEMANDED**: nothing particular is needed, with the rule named. The first answer and the last are not gaps; LATER, MULTIPLE, CONFLICT, CANNOT and UNSPECIFIC are gaps. |
| **SENT / PHRASE / question rows** | The output format. One SENT row per sentence; one PHRASE row per questioned phrase listing its slots; one question row per slot, with the answer and quote. |
| **Family** | A group of question types: ID (which one, who, where), TERM (TERM.a: meaning of a non-ordinary term; TERM.b: "of what?"), SET (members of a set), CONN (connections), SENSE (word meaning; SENSE.b: "what exactly?" for a vague ordinary word), SRC (by whom, from what source), MARKED, UNSPECIFIC. |
| **Run** | One complete detection pass over a benchmark, made of one fresh subagent per section. |
| **Blind editor** | A fresh model judge that sees the passage and a shuffled pool of gaps from several detectors with the source hidden, and answers ASK (a careful editor would ask the author to specify this, so "real") or NO. |
| **Plain detector** | The prompt-only baseline: a fresh Opus reader asked to list unclear places, with the pattern catalogue as guidance (`comm-detect-ambiguity`, fast mode). |
| **Benchmark 1 (B1)** | One long document (a 5,047-word inquiry finding) with a line-by-line reference: 59 agreed rows, re-judged to 46 after the short-name rule. |
| **Benchmark 2 (B2)** | 42 independent real excerpts of technical writing (C001–C042). Their authors listed 70 issues: 53 from the author's own corrections, plus 17 accepted from reviewer proposals. This list is author-relative, not exhaustive. |
| **Benchmark 3 (B3)** | 30 hand-made group-trip messages with 56 planted gaps (47 "non-weak"), 4 clean paragraphs and 4 decoys that look unclear but whose context resolves them. |
| **Recall** | Reference issues found ÷ all reference issues. |
| **Precision ("real share")** | Real findings ÷ all findings, as judged by the named judge. |

---

## 2. Where we ended up

**The detector** (`~/.claude/skills/non-explicitness-detection/`):
1. The session settles the inputs: the source, a one-sentence **setting** (the only context besides the text), runs and model (Opus).
2. It writes a numbered copy and cuts **sections of about 800 words (max 1,800)** at headings or paragraphs.
3. It launches **one fresh subagent per section, not a fork**, all at once. The session never detects, and never reads the bank.
4. Each subagent reads the bank and the whole document, then writes for every sentence:
   - a **SENT row**;
   - **PHRASE rows** listing the slots each questioned phrase needs;
   - **one question row per slot**, answered with one of the seven values. A QUOTE must fill the asked slot itself, from a supplier that is itself supplied, with competitors listed. A NOT-DEMANDED names its rule and slot.
5. Each subagent self-checks by reading its own rows back: every sentence has a SENT row, every slot has a row, every row has a PHRASE row, every exemption names its slot.
6. The session collects the gap answers into `gaps.md`. With two runs, it merges by meaning and marks "both runs" or "one run".

**Measured quality (bank v6.7.1 packaged as the skill, 5 October; v6.7.2 on 7 October):**

| Benchmark | Measure | Result |
|---|---|---|
| B2 | precision (blind editors) | 79–82%, against 65% for the plain detector |
| B2 | real gaps per run | 169–181 |
| B2 | authors' 70 issues fully found | 45–48 per run; 51 (v6.7.1) and 55 (v6.7.2) across two runs |
| B2 | gaps found by both runs that are real | 85–86% |
| B1 | recall | 78–87% depending on version |
| B3 | planted gaps found | 48–50 of 56, at 78–83% real |

**Bank v6.7.2** = v6.7.1 + one rule: a non-ordinary term whose head is an action or relational noun also gets an "of what?" question (16 runs, no regression; the rule's own 10 gaps were all judged real).

The skill file still carries v6.7.1 until it is copied in.

**The fix skill** (`~/.claude/skills/non-explicitness-fix/`) works in four layers:
1. **Decide:** one fresh agent builds a missing-meanings table. Each meaning is fixed with a quoted basis, asked of the author, or declined with a quote.
2. **Word:** one agent for texts up to about 1,800 words; section agents beyond that.
3. **Apply:** literal replacement.
4. **Check:** a trace script, then one independent reviewer, once.

With the author's answers, 50 of 56 planted gaps were resolved with 0 invented particulars.

**The single principle under all of it:** *when a slot is left open, whoever fills it fills it fluently and wrongly.* That holds for a reader of a text, for a model reading our prompt, and for us reading our own rules and metrics. Every reliable step came from making the slot explicit and checking the answer against something quotable.

---

## 3. The whole path on one page

| Date | Approach | Key result | Verdict |
|---|---|---|---|
| 29 Sep | Inline prompt vs Fixcomm's two-pass protocol | 40 vs 29 labels | Two runs isolate nothing; merge by meaning |
| 30 Sep | Procedure changes, 32-pattern catalogue | 12–40 findings; no run found everything | One run is a sample; catalogue adds labels, not recall |
| 30 Sep | "Expect about 50 findings" | 52 findings, about 42 of 46 known | **Killed:** a guess off its home text; would force fabrication |
| 30 Sep–1 Oct | Guarded runs (evidence rule, candidates bin, computed rating) | 0 fabricated quotes; union of 3 runs 46 vs best single 26 | Guards need an outlet; compute ratings, don't ask for them |
| 1 Oct | Grounded-asks meta-pattern | — | Never ask the model to vouch for completeness, counts or importance |
| 1–3 Oct | Detection ladder, 29 readings | author session 14 vs fresh 30; breadth is the only recall lever | Fresh reader; the evidence rule filters but isn't truth |
| 4 Oct | Three benchmarks with checkable references | — | Score against references, not counts |
| 4 Oct | First question bank (8 patterns as small questions) | B2 33/70 at 20% real | "Text doesn't say which" ≠ reader can't tell; no invented answers |
| 4 Oct | **Reframe: explicitness, not reader knowledge** | — | The target becomes a property of the text |
| 4 Oct | Bank v1 (42 questions, 7 slots) | agreement 74–75%; B2 28–29% real (editor) | Measurable, but triggers over-fire |
| 4 Oct | **Reframe: two tests (demand, sufficiency)** | — | Name the parameter, never rule the case |
| 4 Oct | Bank v2 | B2 56–66% real; B3 met all targets | Demand + sufficiency doubles precision |
| 4 Oct | Bank v3 (rules R1–R5) | B2 79–81% real; real gaps fell about 33 → 26 | Rules buy precision, cost recall |
| 4 Oct | **Reframe: agreement drop was mostly the metric** | disputed gaps 81% real vs shared 80% | Union + reconcile, never consensus |
| 4–5 Oct | v3.2 head-to-head with the plain detector | bank 98 real/33 false vs plain 137/101; authors' 19 vs 44 | More precise, far less recall |
| 5 Oct | v4 (connections, word meaning), verifier test | verifier 90% real but halves recall; 36 of 75 dropped were real | The demand step is the recall sink |
| 5 Oct | v5 (local wording, UNSPECIFIC) | editor rejected 9/10 — the judge used the old definition | A judge can encode the old target |
| 5 Oct | v6 (third reason for demand: "the point rests on it") | different gaps, not more | One pass reports a roughly fixed amount |
| 5 Oct | v6.1 output-limit test | 7-excerpt sections: 151 real vs 116–131 | **Section size is the lever**; splitting the bank is not |
| 5 Oct | v6.2 short-name rule | TERM 87% real | General principle from the kind of noun |
| 5 Oct | **v6.3 one row per sentence** | B1 58% → **85–89%** | Structure beats instructions |
| 5 Oct | v6.4 gates + unbounded "passage" | B2 86% real, but B1 → 54% | Bound every word of extent; keep a held-out benchmark |
| 5 Oct | v6.5 bounded "later" | balanced; recommended default | — |
| 5 Oct | Stability test (72 passes) | noise floor about 8–10 real gaps | Compare only in one editor pool, with replicates |
| 5 Oct | **v6.6 checkable "supplied" + action/relation checks** | +60 real per run; authors' 51 vs plain 44 | First version to beat the plain detector on recall |
| 5 Oct | v6.7 precision gates + PHRASE rows | 81–83% real; but gates exempted about 48 real | Judgment words in gates over-fire |
| 5 Oct | v6.7.1 (no checking script) | no measurable loss | The format does the work, not the script |
| 5 Oct | Packaged as skill; trial | no regression | — |
| 5 Oct | Fix skill, two test rounds | 50/56 resolved, 0 invented | Fresh decider; independent reviewer essential |
| 7 Oct | v6.7.2 ("of what" for action terms) | rule's 10 gaps all real; no regression | Current version |

---

## 4. Era 1: before the bank (29 September – 4 October)

Until 1 October every experiment read one text: a 563-line workshop facilitator script of about 4,500 words. The tool was a **pattern catalogue**: `non-ambiguity-patterns.md`, 32 ambiguity patterns P01–P32. Each pattern had:
- a question;
- a "Problem when" clause and a "Not a problem when" clause;
- examples.

A detector procedure applied the catalogue (`non-ambiguity-detector.md`).

### 4.1 Inline prompt vs an elaborate protocol (29 Sep)

**Tried.** The same principles and chunking, in two forms:
- a one-pass inline prompt;
- Fixcomm's two-pass protocol (anchored passes, snapshots, withdrawal rules, hashes).

**Result.** The inline prompt gave 40 labels; the protocol gave 29.

**What happened next.** I ranked the causes with confidence (wording, bookkeeping load, the second pass). A reviewer rejected the ranking, because two runs isolate none of them. All the causes stayed hypotheses.

**Learned:**
- **More labels is not better detection.** Extra labels may only relabel the same gaps.
- **Merge runs by the specific missing meaning, not by line plus pattern ID.** The same gap gets different IDs across runs, and two labels on one line can be different gaps.

### 4.2 Procedure changes and the 32-pattern catalogue (30 Sep, experiments 3–6)

**Tried:**
- half-document runs;
- one fresh subagent per third of the text, merged by script;
- the catalogue flattened to 32 patterns.

**Result:**
- Counts were 31, 12, 40 and 25. Each run recovered 16–22 of a pool of about 46.
- 24 of the 46 were found by one run only; no item was found by all six runs.

**Measured lessons:**
- **The spread between runs with identical instructions was as large as any deliberate change.** One run is a sample.
- The model "checked every sentence against every pattern" by writing a script that **stamped a log line on every line**. This is form-compliance: satisfying an instruction's wording without its substance.
- The six-principle file gave 40 findings; the 32-pattern catalogue gave 31. **More patterns did not buy recall.** Nine patterns never fired.

### 4.3 The expected count (30 Sep, experiment 7)

**Tried.** Telling the model that earlier readings had found about 46 issues and that a complete reading lands around 50.

**Hypothesis.** The model stops when a learned sense of "a satisfying list" (two to three dozen items) fires.

**Result.** 52 findings, about 42 of the 46 known.

**Verdict: killed as a general technique**, by a full inquiry:
- It was honest only because six earlier runs existed, and even then "46" was an unadjudicated pool.
- On a clean text it would be an instruction to fabricate, because a checkable number outranks an uncheckable standard. This was predicted from the mechanism, never observed.
- A later test told a reader the range 86–121: 23 of 115 findings survived evidencing, against 20 of 106 without the range. **No measurable effect.**

**Kept:**
- **The provenance rule:** no quantity enters a prompt without a line stating where and on what it was measured.

### 4.4 Guarded runs (30 Sep – 1 Oct, experiments 8–16)

**Tried, layered one at a time:**
- **An evidence rule.** Quote the words that meet "Problem when" and say why "Not a problem when" fails. A script verified every quote.
- An expected yield computed by a separate sizer step from a measured density.
- **A candidates bin** for suspicions that fail the evidence rule.
- A self-rated importance, then **a computed rating**: the model records only whether the sentence is an instruction, and a script assigns vital, high or medium.
- A same-session second pass.

**Results:**
- No quote was fabricated in six guarded runs.
- The evidence rule alone gave 20 findings. With the computed yield and the bin, 29–38.
- With a doubled yield of 90–122, the model wrote that the text supported fewer and **did not pad**.
- Self-rating gave 10 "vital", mostly on descriptive sentences. The computed rating gave 10 "vital", all on instructions, all correct on audit.
- The union of three guarded runs had 46 distinct items, against 26 for the best single run.
- The same-session second pass added 6, all on lines already flagged.

**Learned:**
- **A guard with no push lowers recall. Pressure needs an outlet** (the candidates bin).
- **Self-rating inflates; compute ratings from recorded features.**
- **A same-session pass deepens but does not widen.**
- The union of independent runs is a real recall lever.

### 4.5 The grounded-asks meta-pattern (1 Oct)

**The insight.** Every prompt had joined a grounded task (detect, against clauses in the input) to an ungrounded vouching ask ("is the list complete?", "did you check every sentence?", "how important is this?").

**Definition.** A **grounded ask** is one whose referent and standard are in the input, so the answer can quote what settles it. Ungrounded asks get form-compliance. Word counts, which have a referent, came out exact every time.

**Remedy.** Move every ungrounded judgment out of the model:
- measure it outside (replicates, planted cases);
- build it into the output's shape (a quote per item, one verdict per unit);
- or compute it from recorded features.

**Why it matters.** This is the root of "answer with a quote" and of "never ask the model to vouch".

### 4.6 Composition design and the first skill (1 Oct)

**Decided** (by reasoning; not tested as specified):
- Detections read and fixes write, so detections on one text can run in any order, provided each check's standard is fixed. Group detections by what they read against: the text, the evidence or the request.
- Fix in one revision; every edit names its finding.
- The final read is a fresh detection, not the reviser's self-certification.
- Whether a fix is automatic or asked depends on authority: *how* something is said is delegated; *what* the author says is asked.

**Built.** `comm-fix-ambiguity`: detector + evidence rule + computed rating + a fix step with a basis rule.

### 4.7 The detection ladder: 29 readings of one document (1–3 Oct)

**Trigger.** The skill's first real use, in the session that had written the text, found 14 findings. A fresh session asked only "which lines are ambiguous to you" listed 64, and 60 of them fitted an existing pattern. The catalogue was not the limit.

**Tried.** Adding or removing one part of the skill at a time, with Fable, Codex, Sonnet and Haiku readers. A second-stage reader applied the evidence rule to other readers' lists.

**Measured results:**

| Change | Result |
|---|---|
| Author session vs fresh reader | **14 vs 30** |
| Removing the stamped examination log | no loss |
| Plain question, three runs | 64, 123 and 169 items |
| Full catalogue / half catalogue / catalogue in the prompt | 106 / 110 / 87 items: catalogue size and location are free |
| Sentence-by-pattern loop | 147 items in 28 minutes vs 106 in 15: costs time, not findings |
| Section-parallel readers (four readers, a quarter each) | **190 items in 11 minutes**: breadth is the recall lever |

- **Agreement between independent readers predicts real items.** Of items found by all three readers, 1 in 3 survived evidencing (including all 4 vital ones); of items found by one reader, 1 in 10 did.
- **The evidence rule is a filter, not truth.**
  - Against a later two-judge reference, evidence survivors matched no better than raw lists.
  - All 87 rejected candidates had passed an evidence check in at least one run.
  - Single readers reached 6–11 of 19 confirmed issues whatever the mode.
- **Other models:**
  - Haiku: 1 of 100 items survived.
  - Sonnet at maximum effort: four of six readers died at the output cap.
  - Waiting time is set by the effort setting, and subagents inherit it.

**Process lessons:**
- Never let the author session detect its own text.
- Don't rename a skill folder while a subagent reads it.
- Tell subagents not to delegate. One nested its own readers.

**Led to (2 Oct).** Detection in fresh subagents (fast, slow and strong modes) with no evidence stage for everyday use: "the diff is the artifact".

### 4.8 Three benchmarks with checkable references (4 Oct)

Count comparisons and the evidence check had both misled, so references were built:
- **B1:** the long finding, scored against a line-by-line reference. Four readers walked a quarter each and a second reader checked every row. The earlier pooled reference was rejected as "not checkable".
- **B2:** 42 excerpts with the authors' issues.
- **B3:** 30 trip paragraphs with planted gaps, clean paragraphs and decoys.

**Scores of the prompt-only modes:**

| Benchmark | Mode | Recall / precision |
|---|---|---|
| B1 | strong (4 parallel readers) | 93% / 35% |
| B1 | fast | 64% / 39% |
| B2 | fast | 74% / 29% |
| B3 | fast | 91% / 91% |

**Measured lessons:**
- Model strength sets the ceiling.
- Breadth raises recall and noise together.
- The catalogue helps only where issues were planted to match it.
- Wording tricks, size hints and counting rules had no reliable effect.
- Two careful judges agree only about 88% of the time on real texts.

### 4.9 The first question bank (4 Oct, 17:27)

**Tried.** Eight patterns turned into small questions answered QUOTE, CANNOT, YES/NO or ACTION, plus a materiality question ("name one thing the reader would do differently"). A script applied the firing rules.

**Result:**
- B3: 51/56 found at 66% real.
- **B2: 33/70 found at 20% real**, against the plain detector's 74% at 29%.

**Diagnosis:**
- 173 of 288 reports came from "CANNOT: the text does not say which one". That checks whether the text *names* something, which on its own is not a problem.
- The reader-knowledge question fired on 3 of 240 targets.
- Invented answers ("describe a case where…") were 2 of 12 real.
- Stricter rules over the same answers peaked at 25–27% real.

**Surviving principles:**
- **A reliable answer is found, not made.**
- An invented answer may explain a report but never trigger one.

---

## 5. Era 2: the explicitness bank, v1 to v5 (4–5 October)

### 5.1 Reframe 1: explicitness, not reader knowledge

**My proposal.** Add reader profiles, since the bank lacked "what the reader knows".

**The user's correction.** "It is not about what the reader already knows. It is about if the sentence is being explicit or not." The example: "I was running the experiments" vs "the benchmarking experiments".

**Adopted:**
- **Explicitness** is a property of the text: does it supply what its own wording demands? Every reader gets the same answer.
- **Relevance** depends on reader and purpose. It may rank findings, never decide detection.
- **"Ambiguity" is the wrong general name.** Strictly it means two readings, and the word steers the model toward guessing about readers.
- **A gap** = the wording demands a specific filler and the text does not supply it before it is needed. It can be missing, later or conflicting.
- **Only demanding wording counts:** "the experiments" demands a filler; "some experiments" does not.
- **The catalogue's "Not a problem when" clauses:** those pointing into the text become exemptions; those about the recipient leave detection.

**Plan.** Two annotators label from the text alone; the idea is measurable if they agree about 70% or more.

### 5.2 Bank v1: 42 questions under seven slots

**Design:**
- 26 catalogue patterns plus a time slot, grouped under seven slots: identity, quantity, participants, event, circumstance, standard, relation.
- No reader questions. What counts as text is the setting plus the passage; no domain knowledge.
- The answer values QUOTE / LATER / MULTIPLE / CONFLICT / CANNOT / NOT-DEMANDED were born here. The pattern "explanation after the point" simply became the answer LATER.
- Tested with two runs on 20 passages (T01–T10 and C001–C010), with scorers and later a blind editor.

**Result:**
- Agreement 74–75%: **measurable.**
- B3: 19–20/20 planted found.
- **B2: 17–19 gaps per excerpt**, 51–52% real by the scorer but only **28–29% by the blind editor**.

**Diagnosis.** Triggers over-fire:
- judgment words with no decision resting on them;
- generic nouns;
- fillers already in the same sentence;
- "no transition" between separate announcements.

Both runs made the same errors, so the cause is the rules, not randomness.

### 5.3 Reframe 2: two tests, and "name the parameter, never rule the case"

**What happened.** I asked the user to rule on one case ("the hotel"). The user asked for a general principle instead.

**The principle.** *"Wording is explicit enough when, for what the sentence asks to be done with a thing, the text singles that thing out among the alternatives the text itself puts in play."*

**The demand test:**
- **Substitution:** if "a / any / some X" gives the same meaning, nothing particular is needed.
- **The sentence's task:**
  - *mention* needs identification only;
  - *act on* needs the act's slots (go needs a place and time; pay needs an amount and payee; book needs the item and when; decide needs a criterion);
  - *judge* needs a criterion.

**The sufficiency test:** among the alternatives the text puts in play (or implies through a quoted frame word from a fixed list), the answer is:
- one candidate → QUOTE;
- several → MULTIPLE;
- none → CANNOT;
- picked only afterwards → LATER;
- incompatible → CONFLICT.

This is how a compiler resolves a name.

**The method.** Six parameters explained the nine error kinds:
- demand;
- alternatives in play;
- the sentence's task;
- the declared level of detail;
- the source of the filler;
- whether the text relates the parts.

A new edge case either falls under an existing parameter or reveals a new one that covers a class of cases.

**Killed:** "write the minimal addition that would make it explicit" as a test, because the answer is invented.

### 5.4 Bank v2: the two tests, plus an inventory arm

**Design:**
- Triggers only nominate places to check; demand and sufficiency decide.
- NOT-DEMANDED must name the failed test.
- Relation questions need a quoted cue.
- A second arm first wrote a flat inventory of things, people and times per passage.

**Result.** **B2 editor precision rose from 28–29% to 56–66%**, with volume down about 70%.

| | B3 | B2 |
|---|---|---|
| v2, no inventory | 80–82% real | 56–61% real; agreement 68% |
| v2, inventory arm | 84–90% real | 63–66% real; agreement 57% |

B3 met every target. The inventory arm was within noise and had the lowest agreement.

**The editor's five rejected classes on B2:**
1. a filler arriving in the next sentence;
2. openness the text declares;
3. a recommendation addressed to the reader;
4. general verbs in lists;
5. product names.

**The user's decision on product names.** Distinctive names identify themselves but can leave other slots open. Generic labels ("the panel", "the API") are not distinctive.

**Measured on the inventory.** The two runs' inventories disagreed on structure, not content. Neither recorded which system "the API" belonged to.

**Saved for later:** an entity table (rows = entities; columns = kind, identifier, where defined, platform, amount, time). Never run.

### 5.5 Bank v3: five rules (R1–R5)

**The rules:**
- **R1:** explained in the very next sentence or under the heading counts as supplied.
- **R2:** declared openness is NOT-DEMANDED.
- **R3:** the addressee of an instruction is its actor.
- **R4:** general words in lists are NOT-DEMANDED.
- **R5:** distinctive proper names identify themselves.

**Result:**
- B2 editor precision **79–81%** (the target).
- But real gaps fell from about 33 to 26 per run, and authors' issues from 9–11 to 6–8.
- **R3 suppressed a real planted gap:** who collects the vouchers.

**Lesson. Rules buy precision and cost recall.**

### 5.6 Reframe 3: the "agreement drop" was mostly the metric

**What happened.** Headline agreement fell from 75% (v1) to 68% (v2) to 61% (v3), and the user asked to treat it as the main problem.

**Measured.** Four effects moved the one number:

| Effect | Kind |
|---|---|
| shared false alarms removed | good |
| a gaps-only measure falls as precision rises | statistical |
| the scorer's grouping (81% shared row by row, 61% after grouping) | noise |
| uneven use of the new rules | real: real-gap sharing fell from 87% to 75% |

- Per-decision agreement *rose* to 90%.
- **Disputed gaps were as real as shared ones (81% vs 80%).** Keeping only consensus would discard 39% of real gaps.

**Rules adopted:**
- Report per-decision agreement, real-gap sharing and list agreement, each with recall.
- **Take the union of runs and reconcile, never consensus.**
- **Every rule use quotes the words that triggered it** (v3.2).

### 5.7 Bank v3.1, v3.2 and the first head-to-head

**v3.1.** Narrowed R3: the addressee is the actor only when no other doer is named and the act needs nothing only some people have.

**v3.2.** Required a quote for every rule use.

**First full-benchmark comparison with the plain detector:**

| | Plain detector | Bank v3.2 |
|---|---|---|
| B3 planted found | 53/56 | 46/56 |
| B2 real gaps | 137 | 98 |
| B2 false gaps | 101 | 33 |
| B2 precision (editor) | 57% | 74% |
| B2 authors' issues fully found | 44 | 19 |

**Diagnosis.**
- The bank was more precise but far behind on recall.
- The misses were relations, mechanisms and word meaning, which the bank barely asked about.
- One judge sorted the 41 misses: word meaning 12, how two things relate 8, belongs to 7, how something works 7, what it is for 4.

### 5.8 Bank v4: connection and word-meaning questions, plus a verifier test

**Design:**
- Questions are asked about each sentence's **main point**.
- A **SENSE** slot ("which meaning?", only with two cue-supported readings).
- A **CONN** slot in four forms (belongs to, relates to, works how, is for what), strictly gated.
- A stricter "which one" when two same-kind things are in play.

**Result:**
- B2 editor: 101 real / 29 false (77%), against the plain detector's 138 / 100.
- Authors' issues: still 19 vs 44.
- New families were precise on tiny samples (CONN 14/15, SENSE 5/5).

**Measured.** Run-to-run variation (4–5 found items) was as large as the version effects.

**The verifier test.** The bank's checks were used to filter the plain detector's candidates.

| | Precision | Authors' issues fully found |
|---|---|---|
| Plain detector | 57% | 44 |
| Plain + bank checks | **90%** | 18 |

Recall halved. **Of 75 candidates the bank dropped as NOT-DEMANDED, the blind editor judged 36 real. The demand step was the recall sink.** That triggered v6.

### 5.9 Bank v5: local wording and UNSPECIFIC

**The user's principle.** Explicitness belongs to the wording where it stands: "it's in the context but not in the language". After "the evaluation experiment", a bare "the experiment" later is a gap.

**The rule (V5.1).** A "which one" answer stays QUOTE only for:
- a distinctive name;
- the wording's own description;
- an antecedent in the same or the previous sentence;
- a short form the text itself declares.

Otherwise the answer is **UNSPECIFIC**.

**Result:**
- B3: 50 planted found. None of the 12 UNSPECIFIC gaps matched a planted gap, so the rise is run variance.
- 3 errors were parts or by-products wrongly treated as re-mentions.
- **The editor rejected 9 of 10 V5.1 gaps**, because its standard ("only one reading is possible") is the very standard V5.1 replaces.

**Lesson. A judge can encode the old definition.** Check that the judge measures the current target.

---

## 6. Era 3: v6 to v6.7.2, the skills, and the fix (5–7 October)

### 6.1 v6: a third reason for demand

**Diagnosis.** The 75 wrongly dropped candidates, sorted by what they asked about:

| Asked about | Real |
|---|---|
| term meaning | 59% |
| set members | 57% |
| connections | 71% |
| side details | 18% |

Sorted by the rule that dropped them, nothing stood out.

**Hypothesis.** The demand step was *incomplete*. It knew two reasons for demand (the wording points at a particular; the act needs a value) and lacked a third: **"the sentence's main point rests on it."**

**Changes:**
- New families: TERM (with an "ordinary vocabulary" exemption defined by the language, not by a reader), SET, CONN-J (juxtaposed things), SENSE.b and MARKED.
- New fields: `main_point` and `term_kind`.

**Result.**
- The new families were precise (TERM 81%, SENSE-B 11/12).
- **The total stayed about 130 gaps and about 105 real per pass.** ID gaps fell from 110 to 46 while the new families added 79.
- **v6 found different gaps, not more.**

### 6.2 v6.1: the output-limit test, and splitting the bank

**Output-limit test** (B2, one editor pool):

| Arm | Real / gaps | Authors' full |
|---|---|---|
| A: 3 sections of 14 excerpts | 116/143 | 21 |
| A2: identical repeat | 131/153 | 21 |
| **B: 6 sections of 7 excerpts, same cost** | **151/187** | **26** |
| A + A2 union (double cost) | 147/181 | 25 |

**Measured conclusion: one pass reports a roughly fixed amount.**
- Halving the section size raised real gaps by 20–35 at no extra cost.
- A second full pass gave a similar gain at twice the cost.

**Splitting the bank** between two subagents per section (the user's idea): +11 real and +12 false at twice the cost, at the edge of noise. **A weak lever; section size is the effective one.**

**B1, sections of about 30 lines:** recall *fell* to 51%, from v6's 64%. Causes:
- a re-mention clarification pushed undefined terms into UNSPECIFIC;
- a description using an undefined word was accepted;
- pass-to-pass variation.

Section size does not help when sections already read the whole document.

### 6.3 v6.2: the short-name rule

**The user's correction.** "The pool" is obvious in an apartment text but not in a data text ("the pool of what?"). They asked for a principle, not rulings.

**The principle.** The criterion is not "obvious from context" but the **kind of noun**:
- **Whole-kind nouns** (hotel, van, experiment) have only "which one?".
- **Relational nouns** (pool of, record of, sizer, detector) also have "of what?".

A short name is explicit when its meaning, its "of what" and its identity are each settled by its own words, by one earlier full mention with no same-kind thing introduced since, or by a frame word. A missing "of what" is reported once, at first use.

The rule reproduced all 14 known cases, and the user confirmed it. The B1 reference was re-judged to 46 rows by an independent subagent.

**Result:**
- TERM 87% real. B2: 162 real, 74%; authors' 32 fully found.
- B1 did not improve (54–58%).
- A miss analysis showed the detector **skipping sentences**.

### 6.4 v6.3: one row per sentence

**Change.** A required SENT row for every sentence, checked by script. Plus a trigger checklist, an SRC question, and narrower name and pronoun questions.

**Result: the decisive change.**

| | Before | After |
|---|---|---|
| B1 recall (one pass, 4 sections) | 58% | **85% (old reference) / 89% (new reference)** |
| Strong mode, for comparison | 93% | — |
| B2 real gaps | — | **200** (the most of any detector) |
| B2 precision | — | 71% |

SRC, CONN and SENSE-B were noisy.

**Lesson. A structural rule (the shape of the output), not a content rule, produced the step change.**

### 6.5 v6.4: strict gates and the unbounded "passage"

**Changes:**
- Narrow gates for SRC, CONN and SENSE.
- A not-demanded list including **"anything explained later in the same passage"**.
- Tuned on B2, with B1 held out.

**Result:**
- B2 86% real, but only 126 real gaps.
- **B1 recall collapsed to 49–54%.** LATER answers fell from 46 to 1; NOT-DEMANDED rose from 17 to 102.

**Diagnosis (measured from the rows).** "The same passage" was never bounded, so on a long document the model took the whole document as the passage and waved through every term defined sections later. The narrow gates themselves worked.

**Lessons:**
- **Bound every word of extent.**
- **Keep a held-out benchmark.** Tuning on B2 broke B1.

### 6.6 v6.5: bounding "later"

**Change.** A meaning is supplied only at or before the sentence, or in the very next sentence. Anything later is LATER, a gap.

**Result:**
- B1 63–67% recall.
- B2: 160 real, 79% precision, 42 false.

**Remaining B1 misses:** 9 of 15 were never asked at all (trigger-step variation). 89 of 93 NOT-DEMANDED rows did not name their gate, although the bank required it.

**Status.** Declared the balanced default.

### 6.7 The stability test and the persistent misses

**Stability test.** v6.2–v6.5 were each run three more times on B2: 72 passes, all judged in one editor pool.
- The real count moved by at most 8 within a version.
- Version rankings were identical in every run.
- About 70% of real gaps were found by all three runs, while 26–43% of false gaps appeared in only one run.
- **Noise floor: differences under about 8–10 real gaps on B2 are not real.**

**Persistent misses.** 37 issues were missed by every version v6.2–v6.5, with the same wrong answer in up to 16 of 16 runs. **They are systematic, so more runs cannot fix them; rules can.**

Three independent analysts found the same causes:
1. **Lax QUOTE:**
   - a quote filling another slot;
   - a supplier that is itself unsupplied (a possessive, a frame word, the setting line);
   - one candidate taken without listing competitors.
2. **Nouns asked about, not operations and relations.**
3. **Exemptions spreading** beyond their own slot.
4. **Consistency between distant places** never checked.

**Recap insight.** Quotes became the new "stamp": a quote got form-compliance the way "check every sentence" once did. **Grounding means a quote plus a checkable fit**: it fills the asked slot, its supplier is defined, and competitors are listed.

### 6.8 v6.6: checkable "supplied", and action/relation checks

**Changes:**
- **A QUOTE must fill the asked slot itself,** from a supplier that is itself supplied, with competitors listed.
- Ten action and relation checks: operation, criterion, compared datum, possession, unit, affiliation, list structure, doer of a plan, purpose clause, method applied to material.
- **An exemption covers only its own slot.**
- Slots defined explicitly.

**Result.**

| | v6.6 | Plain detector |
|---|---|---|
| B2 real gaps per run | 205–209 (+60 over v6.5) | — |
| B2 precision | 56–57% | — |
| Authors' issues fully found | **48 per run, 51 across both** | 44 |
| B1 recall (new reference) | 85–87% | — |

- **The first bank version to match or beat the plain detector on the authors' list.**
- 16 of the 30 issues every earlier version missed were now fully found.
- **The cost:** about +100 false gaps per run, mostly ID and TERM on short excerpts.
- The recap had predicted "rule-only gains are exhausted". **That prediction was refuted.**

### 6.9 v6.7: precision gates and PHRASE rows

**Part A, precision gates (A1–A9).** Examples:
- **A1:** the content of an act is a gap only when the point is what the work is and the act has no single end state.
- **A3:** particulars only when the point uses them, not when "the point is about the whole".
- **A8:** doer and possessive "rest on it" or "only give a steer".
- **A9:** glosses.

**Part B, recall:**
- **B1:** one PHRASE row per questioned phrase listing all its slots, each with its own row, checked by `slot_check.py`.
- **B2:** no supply through a supplier that is itself a gap (a `via` field).
- Counts, units and baselines.

**Result.**

| | v6.7 | v6.6 |
|---|---|---|
| B2 precision | **81–83%** | 61–62% |
| B2 real gaps per run | 171–173 | 220–226 |
| Authors' issues fully found (both runs) | 45 | 51 |
| B1 precision | 37–38% | 27–30% |

**Diagnosis (measured from the rows on lost issues).** **The gates over-fire.** They exempted about 48 real gaps, against 6–8 predicted:
- "Your handoff" was exempted as a possessive (A8);
- "who runs the experiment" as a doer (A8);
- "complete the Airtable records" by A1 + A3.

Each gate has a judgment word the model reads broadly: "about the whole", "rests on it", "only gives a steer", "one end state". This is the v6.4 lesson again.

v6.6 and v6.7 mark the two ends of a precision–recall line. **A proposed v6.8 tightening of A1, A3, A8 and A9 was never built.**

### 6.10 v6.7.1: no checking script

**Why.** A skill cannot ship a `.py` file.

**Change.** The agent reads its own rows back and adds anything missing.

**Result:**
- Running `slot_check.py` afterwards on all 20 outputs: **0 problems.**
- Precision and recall unchanged within noise (B2 79–80%; authors' 47 across both runs).
- In v6.7, every agent had already passed the script on its first try.

**Lesson. The format (PHRASE rows) plus a written read-back does the work, not the script.**

### 6.11 Packaging as a skill, and the trial

**What changed against the controlled tests:**
- one whole file instead of pre-cut passages;
- sections of 850–990 words instead of 400–770;
- excerpt independence stated only in the setting sentence;
- a self-checked SENT coverage.

**Result:**

| | Skill | Unpackaged v6.7.1 |
|---|---|---|
| B2 real per run | 177–181 | 170–171 |
| B2 precision | 79–81% | — |
| Authors' issues across both runs | 51 | 47 |
| Gaps found by both runs that are real | 86% | — |

- B3: 49–50 planted found at 78–79% real, with 4 certain false alarms per run, mostly "two readings fit" calls.
- **No packaging regression.**

### 6.12 v6.7.2: "of what" for action terms (7 October)

**Trigger.** On a real report, the bank flagged "the first 42 full readings" only for what a full reading *is*, never readings *of what*.

**Rule V6.7.2-A.** A non-ordinary term whose head is an action or relational noun also gets an "of what?" row. A comparison partner ("compared X with the whole week") is not the object.

**Test design.**
- The rule's examples were written neutrally ("deep audits", "the whole quarter"), and "reading" was left out of the noun list, so the test text did not hand the agent the answer.
- 16 sections, two runs per benchmark.
- One fresh editor pool judged v6.7.1 and v6.7.2 together. This pool was stricter: it scored the same v6.7.1 gaps at 68–72% against 79–81% before.

**Result.**

| | v6.7.2 | v6.7.1 |
|---|---|---|
| B2 real per run | 169 / 163 | 156 / 156 |
| B2 precision (this pool) | 70% / 70% | 72% / 68% |
| Authors' issues across both runs | 55 | 51 |
| The 30 hard issues | 17 | 15 |
| B3 planted found per run | 48 / 48 | 49 / 50 |
| B3 precision | 82–83% | 78–79% |

- **The rule's own 10 distinct gaps were all judged real.**
- **No regression.** The other gains are of run-variance size.

### 6.13 The fix skill

**Design: decide every gap, change only with a basis.** Each gap gets exactly one outcome:
- **fixed**, with a quoted basis;
- **asked** of the author;
- **declined**, only with a quote that singles the meaning out.

The answer type routes where to look:
- LATER and UNSPECIFIC: the text itself;
- MULTIPLE and CONFLICT: the material or the author, never the likeliest reading;
- CANNOT: the material or the author.

**Execution.** "Parallel vs holistic" was a false choice. Four layers:
1. **Decide:** one missing-meanings table, which is where holism lives, like a translation termbase.
2. **Word:** one agent for texts up to about 1,800 words; otherwise section agents that read everything but propose only for their own sentences.
3. **Apply:** literal replacement.
4. **Check:** a trace script, then one fresh reviewer, once.

**The session never decides or words.**

**Round 1 tests:**
- Folding gaps into meanings was stable: two deciders were within 5 meanings.
- 74/74 proposals applied.
- **The trace script gave 0 flags while reviewers found narrowings and an invented particular**, because narrowing reuses the text's own words. **The independent reviewer is essential.**
- One agent vs parallel wording made no quality difference. **The lever is the decide-layer wording rules**, which were then added:
  - LATER is a merge (move the words up, don't duplicate);
  - an instance supports only "such as", never a narrowing;
  - introduce once, never mention before introduction.

**Round 2 tests:**
- **New rules:** reviewer must-fix fell from 4 to 2, with 0 invented and 0 narrowed.
- **Answer round** (a stand-in author answered from the key): **50 of 56 planted gaps resolved**, decoy and clean paragraphs untouched, 0 must-fix, text +14%.
- **Placement test** on a text this session had written:
  - a fresh decider made 0 own-judgment declines;
  - **the author-session decider made 7, and an independent judge found 4 of them wrong.**
  - **The fresh decider is confirmed.**

---

## 7. How to measure a detector honestly

These were learned by being misled first.

1. **Never compare by count.** More findings can be relabelling or padding. Score against a checkable reference, matching on the *missing meaning*, not on line plus label.
2. **Use three kinds of yardstick together.** Each one misleads alone.
   - **A planted benchmark** (B3), which includes clean paragraphs and decoys. These give certain false alarms and a true denominator.
   - **A real-text reference list** (the authors' issues on B2). It is author-relative, so it understates a detector that finds more than the author noticed.
   - **A long connected document** (B1). It catches coverage failures such as skipped sentences and unbounded "later".
3. **Precision comes from blind editors.**
   - They see pooled gaps from all detectors, shuffled, with the source hidden.
   - **Compare only within one pool.** Editor strictness varies by pool (68–72% vs 79–81% for the same gaps) and by excerpt group (26–88%).
   - Editors are not the definition. They rejected 9 of 10 true re-mentions under an older standard, and 20 of 109 gaps they called "false" matched author issues.
4. **Replicate.**
   - At least two runs per arm.
   - The measured noise floor is about 8–10 real gaps on B2; single-run differences under about a third were noise in the early ladder.
   - Never claim an effect from one run.
5. **Keep a held-out benchmark.** Tuning on B2 broke B1 (v6.4).
6. **Report recall and precision together.** The versions moved along a precision–recall line (v6.6 vs v6.7); a gain in one is often a loss in the other.
7. **Agreement between runs:**
   - Report per-decision agreement and real-gap sharing, not just "gaps both runs found".
   - **Disputed gaps can be as real as shared ones.** Use the union of runs, and agreement only to rank.
8. **Separate variable misses from systematic misses.**
   - Variable misses yield to more runs.
   - Systematic misses (the same wrong answer in 16/16 runs) yield only to rule changes.
   - Read the rows to find which rule decided each miss.
9. **Check that the judge measures the current target,** especially after changing the definition (v5).
10. **Test conditions:**
    - change one thing at a time;
    - fix the success criteria before running;
    - keep test examples out of the rule text (v6.7.2 used neutral examples so the test text didn't leak the answer).

**The pipeline we used:**
1. Two runs, in sections.
2. Gap rows converted to numbered lists.
3. Matcher agents merge the runs into distinct gaps by meaning, recording which run found each.
4. A blind editor pool judges ASK or NO.
5. A summary script computes real/false per run, recurrence and families.
6. A reference matcher scores the authors' list as full or partial.
7. B1 and B3 are scored against their keys.

---

## 8. The method: building a codebook detector for any check

This is the reusable part. It applies to any task that asks a model to find, judge, check or extract something in a text, for example fidelity (is a claim supported by its source?), aspect (does the message answer what the recipient needs?) or consistency.

### 8.1 Define the target as a property of the input

- Say what the detector finds in terms of the text and the material supplied with it, never in terms of what a reader knows or feels.
- If the natural name of the problem is fuzzy ("ambiguity"), find the checkable property under it (explicitness: the wording demands a particular the text doesn't single out).
- Relevance, importance and audience can rank findings afterwards. They must not decide detection.

### 8.2 Split every decision into a demand test and a sufficiency test

- **Demand:** is something needed here? Use substitution and the sentence's task.
- **Sufficiency:** does the supplied material settle it? Use a closed answer set that includes "not there" (CANNOT), "too late" (LATER), "several fit" (MULTIPLE), "contradicted" (CONFLICT) and "not needed, by rule X" (NOT-DEMANDED).

Most of the early precision gain came from adding these two tests.

### 8.3 Ask small questions the input can settle; decide everything else outside the model

- One thing per question.
- **Every answer quotes what settles it.** "Not there" is always allowed.
- **A quote counts only with a checkable fit:**
  - it fills the asked slot itself;
  - its supplier is itself clear;
  - competitors are listed.

  A bare quote becomes the new rubber stamp.
- **Never ask the model to vouch** for completeness, counts or importance; it will answer fluently and wrongly. Compute those yourself.
- **Never use invented answers** ("describe a case where…", "write the minimal fix") as triggers. A reliable answer is found, not made.

### 8.4 Let the output's shape enforce coverage

- Require one row per unit that must be examined: a SENT row per sentence, and a PHRASE row listing each phrase's slots with a row per slot.
- Check the rows with a script during development, or with a written read-back in a packaged skill; both worked equally.
- **Structure beat instructions every time.** The SENT row raised long-document recall from 58% to 85–89%; instructions to "check every sentence" got stamped.

### 8.5 Keep each pass small, and use breadth for recall

- **One pass reports a roughly fixed amount.** Sections of about 800 words gave 20–35 more real gaps than sections twice as large, at the same cost.
- New rules can displace old findings rather than add to them.
- Parallel sections, and a union of independent runs, are the recall levers.
- Splitting the codebook between agents, wording tricks, size hints, counting rules and the pattern catalogue's size were not.

### 8.6 Run detection in fresh subagents fed only files

- The session that wrote or discussed the text knows meanings the text doesn't state. It detected 14 where fresh readers found 30, and it made 4 of 7 wrong decisions in the fix test.
- Give subagents only:
  - the codebook;
  - the document;
  - a one-sentence setting;
  - their section range.
- Tell them not to delegate.
- Give each its own scratch folder; two collisions happened when agents shared one.

### 8.7 Write the codebook as a text that will be read literally

- **Bound every word of extent:** "later", "the passage", "supplied", "about the whole". An unbounded word in an exemption collapsed recall twice (v6.4, v6.7).
- **Say exactly which slot each exemption exempts, and nothing more.**
- Gates with judgment words ("rests on it", "only a steer") will be read broadly.
- Settle edge cases with a **general parameter** (the kind of noun, the sentence's task, distance), then re-test. Never rule single cases.
- Layer versions with explicit precedence, newest first, and keep the base definitions underneath.

### 8.8 Iterate by reading the rows

1. Run, score and pool.
2. For each miss and each false finding, find the row that decided it and the rule it cites.
3. Class the problems: never asked, wrong question, wrongly exempted, wrongly answered "supplied", or not the target at all.
4. Fix the class with a general rule.
5. Re-test on held-out material with two runs.

Expect a precision–recall trade, and choose deliberately.

### 8.9 The fix side, if the check needs one

- Decide every finding, but change text only with a quoted basis. Otherwise ask the author.
- Keep decisions in one table (the holism layer); word per sentence; apply literally.
- Check with an independent reviewer once. A script that traces words cannot see narrowings built from the text's own words.
- No detect-fix loops.

---

## 9. Do not repeat

**On the target:**
- Detecting by reader knowledge, reader profiles or "for this recipient" exemptions.
- Calling the whole target "ambiguity".
- Asking the user to rule on single cases instead of finding the parameter.

**On prompts and codebooks:**
- Stating an expected number of findings.
- Asking the model to certify coverage (the logs get stamped), or to rate importance (it inflates).
- Invented-answer questions as triggers.
- "CANNOT: the text doesn't name it" as the firing signal without a demand test.
- Trigger words alone deciding demand (v1 flooded: about 18 gaps per excerpt, about 70% false).
- Relation questions without a quoted cue.
- Exemptions or gates with unbounded words of extent or judgment words (v6.4 "same passage", v6.7 A1/A3/A8).
- Any exemption that isn't limited to its own slot.
- A broad "the addressee is the actor" rule; it suppressed a real gap.
- Flat inventory lists before detection (lowest agreement). If an inventory returns, use the entity table and test it alone.

**On procedure:**
- Two passes, halves, per-third subagents, a same-session second pass, or a sentence-by-pattern loop as recall tools. They stay within noise, deepen without widening, or cost time without findings.
- Expecting a bigger pattern catalogue to raise recall.
- Splitting the codebook across agents on the same text (+8% real at twice the cost).
- Letting the author session detect or decide.
- Renaming a skill folder while a subagent reads it; shared scratch or output folders between parallel agents.
- Shipping a checking script with a skill; a written read-back does the same.
- Haiku as a fast option (1 of 100 items survived evidencing); Sonnet at maximum effort (died at the output cap).

**On evidence and measurement:**
- Treating evidence-rule survival as truth, or building a reference from detector output.
- Comparing by counts, single runs, or across editor pools.
- Consensus-only lists, or optimising the headline agreement number.
- Judging a definition change with a judge that applies the old definition.
- Tuning and testing on the same benchmark only.
- Trusting a fix trace script without an independent reviewer.

---

## 10. Still open

| Item | Status |
|---|---|
| **v6.8** (tightening the over-firing gates A1, A3, A8, A9) | Proposed, never built. Expected to recover 30–40 of about 48 real gaps lost in v6.7 |
| **Consistency between distant places** (a figure against another place far away) | Not detected; needs a separate whole-document pass |
| **The entity-table inventory** | Designed, never run |
| **The plain detector's own run-to-run noise** | Never measured |
| **A cross-model or human agreement check on the codebook** | Never done |
| **Fix skill** | Folding the same meaning in a summary and in the body is missed; edits add about 14% length with answers |
| **v6.7.2 in the skill** | The installed skill's bank is still v6.7.1 until v6.7.2 is copied in |

---

## 11. Where the evidence was

The paths below are the record at the time of writing. If they have been deleted, this document is the record.

- **Banks, all versions:** `AIOpsMan/compare/benchmark_data/explicitness-bank/explicitness-bank*.md`.
- **Results, per version:** `…/explicitness-bank/results*.md`, `results-stability.md`, `v67-analysis-summary.md`, `fix-tests/results-fix-tests.md`.
- **Inquiries:** `AIOpsMan/compare/devdocs/inquiries/`, including:
  - `2026-09-30` expected count;
  - `2026-10-01` meta-pattern;
  - `2026-10-04` question-bank structure, explicitness reframe, when wording is explicit enough, agreement drop;
  - `2026-10-05` relations for v4, demand test for v6, short-name rule, recap, prompt-design rules, fix skill design.
- **Era 1 reports:** `AIOpsMan/compare/report-detection-experiments.md`, `AIOpsMan/report-detection-ladder-2026-10-02/`.
- **Benchmarks:** `AIOpsMan/compare/benchmark_data/1`, `/2`, `/3`, each with `scoreboard.md` and its keys.
- **Scoring pipeline scripts:** `…/explicitness-bank/stability/`.

