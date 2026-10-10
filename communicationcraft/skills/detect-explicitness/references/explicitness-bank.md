
# Explicitness bank (version 6.7.2)

**How this file is organised.** The bank grew in layers. Each layer is a version, newest first, and **a newer layer takes precedence over everything after it** where they conflict. Rules are named by their layer (for example V6.7-A1, V6.6-B, V6.3-A); the older text further down defines the base method (the two tests, the answer values, the slots and the output row) that the newer layers refine. Read the whole file.

Version 6.7.2 = version 6.7.1 plus rule V6.7.2-A below. It takes precedence over everything after it.

### V6.7.2-A — A term that is an action or relational noun keeps its "of what"
When a phrase gets a TERM.a question (its meaning is not ordinary vocabulary) **and** its head noun names an action or carries an open "of / by / for", also ask **TERM.b: of what?** (for an action noun: applied to what, what was read, collected, reviewed, tested, extracted) as its own row.
- Action-noun heads include: review, collection, extraction, analysis, check, test, run, fix, edit, rebuild, inspection, survey.
- **TERM.a does not answer TERM.b.** Knowing what a "deep audit" is does not say what was audited; record both rows.
- TERM.b is supplied only by the V6.7-A2 sources (the same sentence's object or complement, listed members, the sentence's own predicate, a carried-over possessor, or exactly one candidate of the right kind in the paragraph that makes sense with it).
- **A comparison partner is not the object.** In "compared X with Y", Y is what X is compared with, not what X's action noun acts on. "Compared the first 30 deep audits with the whole quarter" does not say what was audited.
- This relaxes V6.1's "at most one TERM question per term": a term may have one TERM.a row and one TERM.b row, each at its first use in a main point.

Version 6.7.1 = version 6.7 with the slot coverage of V6.7-B1 checked by you, by reading back your own rows.

Version 6.7 = version 6.6 plus the rules below. They take precedence over everything after them.

Part A narrows rules that fire where the sentence's point does not depend on them. Part B makes the bank carry out its own rules, and adds a few missing triggers.

---

## Part A — Precision: a question gives a gap only where the point rests on it

### V6.7-A1 — What concretely is done (operation, SENSE.b on a verb, purpose-clause verb)
The content of an act named by a verb is a gap only when **both** hold:
1. The main point is *what the work is*: an instruction, a request, a plan step, an option to choose, or a to-do item.
2. The verb with its stated object leaves the act open. Either two standard readings give different end states, or the act needs a source, target, value or comparison point that the text does not give.

NOT-DEMANDED (exemption "V6.7-A1 act fixed or not the point — slot: what is done") applies to:
- the verb of a heading, title, option name or work-item label. This exempts the method slot only; the object, source and compared datum are still asked.
- a completed act reported together with its result ("processed 274, created 17");
- a general responsibility verb in a role statement ("orchestrates", "owns");
- a pro-verb standing for an act named by the heading or the previous sentence ("did", "land");
- a verb whose standard sense, with its object, leaves one end state ("work through the questions", "publish", "side by side");
- a sentence whose point is who, when, status or size.

When parties divide one act, ask each party's part (who does it). Do not ask the method.

### V6.7-A2 — "Of what" is supplied (TERM.b and relational heads)
The "of / by / for what" slot is supplied by any of:
- the setting or passage using the same word, or its verb or noun form, together with its complement ("execution-log saving" supplies "saving");
- the noun's members or content listed in the same sentence;
- a pair or contrast in the same sentence or item that names the kind ("gate-first or assess-included" supplies "the assess side");
- the sentence's own predicate saying what the thing processed, produced, holds or is filled with;
- a possessor on an earlier member of the same list, which carries over;
- an owner's domain, when the noun is a general category in a list of what that owner holds or does;
- exactly one candidate of the right kind in the paragraph, when the sentence makes sense with it.

Do not add a TERM.b row to a phrase that already has a "which one" gap for the same missing particular.

A frame word or topic-only setting still never supplies "of what" (V6.6-A).

### V6.7-A3 — Particulars and content only when the point uses them
Which one, which members, which subset, or what a record or referent contains is demanded only when the point does one of these:
- acts on them or judges them individually (choose, adjust, evaluate, compare);
- reports a result about that particular one ("a real skill … scored 82");
- uses them in a later step.

NOT-DEMANDED (exemption "V6.7-A3 point is about the whole — slot: …") applies when the point is the set's count, share, structure, readiness, status or existence ("one key across several flows", "three questions are ready", "most of them save to Airtable", "the details are agreed").

A set the sentence's own act creates needs only its number.

This rule does not apply to TERM.a terms, or to referents whose identity is open.

### V6.7-A4 — Criterion only when someone must apply it
A choice or decision act needs a criterion (P16.a) only when one of these holds:
- the text asks the reader or a named party to make the choice under a standard it implies;
- the claim's truth turns on that standard ("better", "correct", "worked", "stale").

NOT-DEMANDED applies to:
- a choice reported as already made;
- a choice the text gives to a named party as theirs ("each owner chooses", "calls for you"), which is declared discretion;
- a judgment word that gives the writer's own reason for a request;
- a disjunction of storage places where nobody is asked to do the placing.

### V6.7-A5 — Structure and affiliation need a point-changing second reading
**List structure and unit/distribution (V6.6-B).** A gap needs two readings, each cued by something other than the separator or the number itself, that lead to different conclusions, counts, owners or actions. A slash between two qualifiers of one noun ("signed/versioned") reads as "and".

**Affiliation ("of which system?").** Ask only when one of these holds:
- (a) an act must be done in or through the thing;
- (b) the main point is where something is kept, listed or found;
- (c) the conclusion would differ by system.

Two more conditions:
- The sentence naming the component that **produces or holds** the noun supplies the affiliation. A component that only consumes or resolves the noun does not.
- Systems that appear only as link hosts, or as issue trackers cited by ID, are not competitors.

In a status or progress report, a noun anchored by its own description tied to a named owner, or by an identifier, is NOT-DEMANDED.

### V6.7-A6 — A competitor must fit
For V6.6-A3, a candidate competes only if it fits every constraint the wording sets: number, count, the verb's object, and singular or plural.

These are not competitors:
- a reading the sentence sets against the chosen one;
- an illustrative example;
- a part or attribute of another candidate, one per item (the meaning is the same, V6.3-E);
- a candidate the text has just removed from the role ("the old one is turned off").

Two parallel lists in the same order whose words echo each other map item by item.

### V6.7-A7 — Announcements and blocks
These are NOT-DEMANDED (exemption "V6.7-A7 announced for below"), unless something before the announced content must act on it:
- a bare term that a section heading announces as its topic (after a colon, or as the heading's object);
- a numbered position label followed by its own content ("Layer 3 — …");
- a count or list announced at the end of the passage by a colon or "as follows".

A definite noun used as known in the same heading ("the axes"), and a label that gives no content ("blocker 5"), are still asked.

A non-prose block (diagram, code block, table, group of tiles) counts as one sentence for the R1/V6.5 "very next sentence" window. The first sentence after the block supplies the labels inside it. A numbered or bulleted prose list is not a block.

### V6.7-A8 — Doer, place and possessive
**Doer (P12.a).** The doer check needs two or more named parties who could do the act. A party whose role in the same act chain is stated otherwise (approves, answers, receives, only supplies input) is not a candidate. If no candidate remains, answer NOT-DEMANDED. "Zero candidates means CANNOT" governs identity and content slots, not the doer trigger.

**R2 declared openness.** The cues for declared openness include "named people", "designated", "to be agreed", and postponement clauses ("can wait until a run needs them").

**Place.** For the place slot of an act, a pointer whose own wording carries a distinctive name or ID identifies the place ("the Christine conversation", "AIO-1110"). For a content slot, a pointer supplies the content only if the place is identified and holds that content.

**Possessive (V6.6-A2).** A possessive is a gap only when the point rests on the item's identity or content, and the same sentence does not state that content.

When the sentence only authorises an act that the text attributes to the addressee's own plan ("go ahead with … your plan"), the act's place, method and members are NOT-DEMANDED. Who does it is still asked.

### V6.7-A9 — Frame word, gloss, field terms
**Frame word.** A frame word may settle:
- (a) the **kind** of a referent, when it names that kind in words and only one kind fits the role;
- (b) which preceding text a connective or "this" points at, when the setting line describes exactly that text.

It still never settles content, purpose, or what a plan tests or a candidate is for.

**Gloss.** When a gloss is open, report one gap on the term it glosses. The gloss's ordinary words get no separate rows.

**Field terms.** A term used consistently in the standard sense of the field the setting names is ordinary vocabulary. Coined compounds stay non-ordinary (V6.1).

---

## Part B — Recall: carry out the rules, and a few missing triggers

### V6.7-B1 — PHRASE rows: every applicable slot gets a row (self-checked)
For every phrase you write a question row about, first write one **PHRASE row**:

```json
{"unit": "...", "line": N, "qid": "PHRASE", "trigger": "<exact words>",
 "slots": ["which one", "of what", "what it contains", ...],
 "no_slot": ["<slot>: <reason it does not apply>", ...]}
```

**`slots`:** list every slot from the V6.6 slot list that the phrase's head admits. Use this guide:
- definite noun: which one;
- relational head: of what;
- information artifact used by the point: what it contains;
- act verb: what is done, who;
- decision: by what criterion;
- possessive: by what relation;
- "per X": per what unit;
- system-scoped noun: which system.

**Every slot in `slots`** must then have its own question row, with the same trigger and `"slot"` set to that slot. A NOT-DEMANDED row covers only its own slot.

**`no_slot`:** record here a slot the head admits but that clearly does not apply, with its reason. Leave it out of `slots`.

A phrase is finished only when every listed slot has a row. Before you finish, read your rows back and check, for every PHRASE row, that each slot in its `slots` has a question row with the same trigger and that slot; that every question row has a PHRASE row for its trigger; and that every NOT-DEMANDED row names its slot in `exemption`. Add whatever is missing.

### V6.7-B2 — No supply through a supplier that is itself a gap
Before a QUOTE, look at your own rows for the quoted supplier. If any row answers CANNOT, MULTIPLE, LATER or UNSPECIFIC for it, this row cannot be QUOTE. Give the same gap value, and fill `"via"` with the supplier's trigger. A `via` row is reported under its root gap, not as a new one.

An appositive or parenthesis that pairs two names ("X (the Y)") supplies only the pairing. It does not say whether one *is* the other, *contains* it, or exists *once per* something. Ask CONN.relate.

### V6.7-B3 — An exemption keeps to its slot
- A personal or distinctive name exempts only the name. A noun it modifies ("the X conversation", "X's list") gets its own P01.a.
- A question that asks "which X …?" declares open only the subset it asks for. The set it draws from (X of what system, account or scope) is still asked.
- The conventional-arrow exemption covers a single A→B arrow. When one source fans out to several targets of different kinds, ask for each branch what it does and under which condition (CONN.work), unless the branch's label states both.

### V6.7-B4 — The main point keeps what it states
These are part of the main point; run the checklist on them:
- An aside, colon clause, quoted rule or arrow notation ("A → B") that states the **content** of a main-point noun (a rule, plan, criterion, definition or list). Illustrative "e.g." asides keep the V6.4-D exemption.
- The words of a question the sentence quotes, or promises to answer ("the check that would answer 'is this still used'"). These get SENSE.a and SENSE.b rows.
- Both sides of every pair in a mapping or equation sentence ("X is Y; C is D", "maps onto").

The SENT row's `main_point` must keep every content word of the core clause and every mapped pair. It must not paraphrase them away.

### V6.7-B5 — Counts, units, baselines
- For a count, ask **"N of what"** (the unit counted) as its own row, separate from the members. This matters most when the head noun is a process noun or is left out ("Six are …", "instead of two"). It is supplied if the unit is stated in the same or the next sentence.
- For "per X" or "each X" that governs a choice or act, pair X with the object of **every** act it governs, including acts inside listed options, and with every other unit the passage uses for the same decision. QUOTE only when the ratio is stated. This applies when two different units are named.
- V6.6-A3's competitor listing also applies to **baselines**. Before a QUOTE on P19.a ("did not move", "rose", "inflated"), list every figure of the same measure in play as a possible baseline. If two fit, answer MULTIPLE.

### V6.7-B6 — Small triggers added to the checklist
- **Location claim.** "Exists in", "is held in", "is recorded in" or "lives in" asks which system or table (CONN.belong), however many systems are in play.
- **Agentless passive step.** An agentless passive step in a proposed process ("is told", "is turned off") gets P12.a who, when two or more possible doers are named. This does not apply to automatic or recordkeeping passives.
- **Information artifact.** A noun naming an information artifact (manifest, plan, template, card, list, schema, report) whose content the point uses, because it is produced, returned, judged or acted on, gets "what does it contain?", even when the noun is ordinary vocabulary.
- **Action noun.** An action noun with an open object (fix, edit, change, review, test) gets "applied to what?" when the passage introduces two or more things it could apply to.
- **Offered options.** For options offered for a decision ("X or Y?"), ask what each includes that the other does not. Defining each label separately, or giving a recommendation's reason, does not answer it.
- **Negation.** A negation that removes an act together with its doer or method ("not scripts that Codex blindly executes") leaves the replacement act's doer and method open. Ask them when the point is a recommendation or instruction.

### Output fields added in v6.7
- **PHRASE rows**, as in V6.7-B1.
- **`"via"`** on a row whose gap passes through a supplier, as in V6.7-B2.

---

# (Version 6.6 text follows)

# Explicitness bank: version 6.6

Version 6.6 = version 6.5 plus the three general rules below. They take precedence over everything after them.

They address three causes of systematically missed gaps:
- **A.** The bank accepted words *near* the answer as supplying it.
- **B.** It asked about things, rarely about actions and relations.
- **C.** An exemption for one slot spread to the whole sentence.

Coverage (one SENT row per sentence), the V6.4 gates and the V6.5 "explained later" rule stay unchanged.

**What a slot is.** A *slot* is one particular a wording can demand:
- which one;
- of what;
- which meaning;
- what it contains;
- who;
- what is done;
- by what criterion;
- by what relation;
- per what unit;
- which system;
- when or where.

One phrase can have several slots.

---

## Version 6.6 rules (take precedence over everything below)

### V6.6-A — What counts as "supplied" (applies to every QUOTE answer)

An answer is QUOTE only if **all three** hold. If any fails, the slot is not supplied: answer CANNOT, MULTIPLE, CONFLICT or LATER as fits.

**1. The quote fills the asked slot itself.**
- Name the slot in the field `"slot"`, and show how the quoted words fill *that* slot.
- Words that fill a **different** slot of the same phrase do not count. Examples:
  - its kind or label ("v0.6" being "a run" does not say what was versioned);
  - its purpose ("so that …" does not say how the act is done);
  - its baseline ("from 31" does not say what operation cut it);
  - the objects acted on;
  - what is excluded ("not off the model's word" does not say which measurement);
  - the system a datum comes from (naming the sources does not say what datum is compared).
- A quote that only restates the trigger supplies nothing.

**2. The supplier is itself supplied.** The words you quote must themselves identify or define what they are used for. These are **not** suppliers on their own:
- **A possessive** ("your handoff", "your plan"). It names the owner, not the item. It identifies the item only if the passage introduced such an item, or only one such item can exist.
- **A frame word or the setting line.** It can settle *which one* among things of a kind the passage itself introduced. It never settles *of what*, a content, or a particular the passage's own wording demands. "Model-evaluation work" does not say what "the test plan" tests; a setting line naming a topic does not say what "cutover" changes.
- **A pointer to a place** ("in the document", "as discussed", "see above"). It counts only if that place is itself identified (its own P01.a is QUOTE).
- **A gloss made of equally open words** ("where each model stands" for "state"). It supplies nothing; apply V6.2-B.
- **"Only one in play" when none was introduced.**
  - **Zero candidates of the needed kind → CANNOT**, not QUOTE. Examples: no table named for "the field"; no handoff introduced for "your handoff".

**3. Competitors are listed.**
- Before answering QUOTE on which one, which meaning, of what, or what something refers to, list in `"candidates"` every candidate the text puts in play: the preceding text, the next sentence, and an adjacent heading, bullet or list.
- **Two candidates fit → MULTIPLE.** Example: "the implementation details" after a sentence naming both a structure and a Skill to build.
- **Adjacent text contradicts the chosen reading → CONFLICT,** quoting both. Example: a heading "complete" followed by a bullet saying 11 records are still wrong.
- **A heading or label** supplies a sense only if no adjacent part cues another reading.

**NOT-DEMANDED must cite its exemption.** Every NOT-DEMANDED answer fills `"exemption"` with the rule and the slot it exempts, for example:
- "R2 declared openness — slot: who";
- "1a substitution — slot: which instance";
- "V6.4-C descriptive word — slot: sense".

A NOT-DEMANDED without a named rule and slot is invalid; re-decide it.

### V6.6-B — Action and relation checks (added to the V6.3-B checklist)

For each sentence's main point, also check the following and write a question row for each that applies. Each row still goes through the demand test (it applies only when the main point rests on it) and the V6.4 gates, and its answer must meet V6.6-A.

| Check | When it applies | Question (qid) |
|---|---|---|
| **Operation** | The main verb names a change, process or check ("cut", "separate", "migrate", "split", "works through", "examined", "handles") | What concretely is done? (P11.a). QUOTE only if the method is stated, not only the result or the object |
| **Criterion** | A decision, selection, stop or approval act ("choose", "approve", "sign", "read X off Y", "base on", "stop when", "decide") | By what criterion? (P16.a) |
| **Compared datum** | A comparison verb ("compare", "cross-check", "match", "reconcile", "against", "calibrate") | What of A is compared with what of B? (P11.a). Naming the two sources does not answer it |
| **Relation of possession** | A possessive that the point or a request rests on ("these rows are yours", "your accounts") | By what relation: made, owns, assigned, recorded as? (TERM.b) |
| **Unit and distribution** | "Per X" or "each X" governs an act on a different Y; or a set is tied to a generic or quantified other ("the skill's quality bars", "for 20 skills") | One Y per X, or several? One set per X, or one shared? (CONN.relate) |
| **Affiliation** | Two or more systems, tools or owners are in play, and a system-scoped noun appears (token, session, API, field, table, key, record) | Of which system? (CONN.belong). The substitution test does not exempt this |
| **List structure** | List members differ in kind, or are joined by different separators ("gate · assess · prove, boundary") | Parallel parts, a sequence, or a separate dimension? (CONN.relate) |
| **Doer of a plan** | A subjectless plan ("the idea is to try it", "the next step is writing X"), and the text names two or more possible doers | Who does it? (P12.a) |
| **Purpose clause of a request** | A request's reason clause ("so I can complete the records") | The clause's action verb gets SENSE.b. The purpose clause is part of the main point here (overrides V6.0's side-clause exclusion) |
| **Method applied to material** | A verdict about a method or tool sits beside the material it was applied to ("examined … to see whether the method worked") | What did the method do with the material? (P07.a) |

### V6.6-C — An exemption covers only its own slot

Every exemption applies to **one slot**, the one its own words concern. Every other slot of the same phrase or act is tested as usual.

| Exemption | Exempts | Does not exempt |
|---|---|---|
| **1a substitution test** ("a/any X" means the same) | which instance | affiliation (which system), distribution (one per X or shared), scope (does every case get this step), content |
| **R2 declared openness** ("whoever owns data policy") | the slot declared open (who) | what that person does, approves or signs |
| **V6.5 plain indefinite** ("someone") | who | what that someone does, or which part of the act is theirs. When a sentence divides one act between parties ("by hand … code handles the rest"), ask which part each party performs |
| **Declared level** ("at a high level") | detail | scope. If a step carries a variation cue ("route code", "per domain", "depending"), ask whether the step applies to every case (P18.a) |
| **R3 addressee as actor; R4 general terms in lists** | the slot they name | other slots |
| **V6.4-D illustrative example, contrast class, loose summary** | the example's own specifics | the slots of the main point the example illustrates |

### Output fields added in v6.6

Every question row also carries:
- `"slot"`: the slot asked, from the list above;
- `"candidates"`: on QUOTE for which one, meaning or of what, the candidates in play, ' || ' separated; otherwise empty;
- `"exemption"`: on NOT-DEMANDED, "<rule> — slot: <slot>"; otherwise empty.

---

# (Version 6.5 text follows)

# Explicitness bank: version 6.5

Version 6.5 = version 6.4 with one rule changed, in the "Version 6.4 gates" section (V6.4-D, the bullet now titled "Explained later"). The earlier V6.4-D bullet "explained later in the same passage counts as supplied" let every term defined anywhere later in a long document pass as supplied.

**The V6.5 rule:** a meaning is supplied at a sentence only if it is stated at or before that sentence, or in the very next sentence. An explanation that comes later than the next sentence does not make the meaning supplied: the answer is LATER (a gap, with the later quote), never NOT-DEMANDED. This holds for every task (mention or act) and for every question family, and it overrides the last sentence of R1 ("Answer LATER only when something in between must be acted on …") and any other rule that lets a later explanation count as supplied.

Everything else in v6.4 is unchanged, including coverage (one SENT row per sentence) and the other V6.4-D exclusions.

# (Version 6.4 text follows, with the V6.4-D "Explained later" bullet replaced)

# Explicitness bank: version 6.4

Version 6.4 = version 6.3 plus the "Version 6.4 gates" section, which comes immediately before "Slots and their questions" and takes precedence over the rest. They tighten when four checks produce a gap:
- SRC;
- connections;
- SENSE.b and SENSE.a;
- a set of checklist cases on the which / who / where questions.

Coverage (one SENT row per sentence) and the checklist stay unchanged, so every applicable check still gets a row.

# (Version 6.3 text follows)

# Explicitness bank: version 6.3

Version 6.3 = version 6.2 plus the "Version 6.3 rules" section, which comes immediately before "Slots and their questions" and takes precedence over everything else:
- **V6.3-A, coverage.** A SENT row for every sentence, self-checked.
- **V6.3-B, trigger checklist.** One question row per applicable check; the cap of one word-meaning question per phrase is lifted.
- **V6.3-C, a new demand reason.** "By whom / from what source" for evidence a claim rests on.
- **V6.3-D, names narrowed.** In v6.2, 10 of 12 "what is this name" gaps were judged false.
- **V6.3-E, pronouns narrowed.** MULTIPLE only when the readings differ in meaning.

# (Version 6.2 text follows)

# Explicitness bank: version 6.2

Version 6.2 = version 6.1 plus the "Version 6.2 rules" section, which comes immediately before "Slots and their questions" and takes precedence over older rules where they conflict:
- the confirmed **short-name rule**, which replaces V5.1's blanket clause, adds the slot question TERM.b and adds the field "head";
- **six judgment fixes**.

# (Version 6.1 text follows)

# Explicitness bank: version 6.1

Version 6.1 = version 6 with three rule fixes: (1) V6.5 marked side details tightened — only named alternatives mark a slot, plain indefinites do not; (2) V6.2 set members — check the whole passage for the members (or a pointer) before reporting; (3) V5.1 clarified — a shorter name for a thing named earlier is a re-mention. Nothing else changes.

# (Version 6 text follows)

Version 6 = version 5 plus the "Version 6 additions" section: a third reason for demand ("the sentence's main point rests on it") applied to term meaning (TERM.a), set members, juxtaposed connections and vague ordinary words (SENSE.b); marked side details; the fields "main_point" and "term_kind"; and V5.1 narrowed to re-mentions of the same thing.

Version 5 = version 4 plus one rule, V5.1 "local wording" (section "Version 5 addition" below), from the user's principle: explicitness is a property of the wording where it stands, not of whether the meaning can be recovered from elsewhere in the text ("it's in the context but not in the language"). V5.1 changes step 2b, adds the answer value UNSPECIFIC, and adds the output field "earlier_mention". Nothing else changes.

Version 4 = version 3.2 plus the "Version 4 additions" section (main point, word-meaning question, connection question, stricter "which one"). Version 3.2 = version 3.1 plus a required quote for every rule application (see "Rule quotes" and the output format). Version 3.1 = version 3 with rule R3 narrowed (see R3). Version 3 = version 2 plus five general rules (section "Version 3 rules" below). Versions 1 and 2 are kept unchanged.

**What it detects.** An explicitness gap: the wording needs something particular, and the text does not single it out.

**What changed from version 1.** Version 1 asked only whether a filler appears. Version 2 asks two tests first:

1. **Demand.** Is something particular needed here?
2. **Sufficiency.** Does the text single it out among the alternatives the text itself puts in play, at the level of detail the sentence's task needs?

**No reader.** Nothing here asks what a reader knows, would find plausible, or would do. Statements in the setting about what someone has or has not seen are not fillers. Only facts stated in the text count.

## The text

The text is the setting plus the passage.

- A filler counts as **supplied** if it is stated earlier, or in the same sentence. **Exception (V5.1):** for "which one" questions, an earlier mention supplies the filler only if the wording at the point of use itself picks it out.
- A filler that is stated only **after** the wording that needs it counts as LATER.
- Nothing outside the setting and passage counts. That includes general knowledge of the domain.

## Step 0: find candidates (triggers)

Go through the passage sentence by sentence, including headings and list items. Mark every wording listed under the slots below.

Trigger words only nominate a place to check. The tests in steps 1 and 2 decide whether there is a gap.

## Step 1: the demand test (is something particular needed?)

For each trigger, answer **1a** and **1b**.

**1a. Does it point at something particular?** Substitution test: replace the wording with "a/any X", "some X" or "X in general". If the sentence still means the same, nothing particular is needed for identity or quantity. This applies to generic and category nouns ("approvals", "past runs"), explicit indefinites ("any five", "some of you", "two consecutive inquiries") and kind statements.

**1b. What does the sentence ask to be done with it?** Choose one of three task values, and quote the words that show it.

- **mention:** a statement, description or report. Only identification is needed: which one.
- **act on:** an instruction, request or recommendation to do something, including a question that asks someone to do something. The act needs the slots listed in the act list below.
- **judge:** a decision, a recommendation between options, or a conclusion rests on the wording, including a question that asks for an assessment. A criterion or comparison point is needed.

If the text declares a level ("at a high level", "in short", "roughly"), detail beyond that level is not needed.

**Act list.** The act types, and the slots each one needs:

| Act type | Slots needed |
|---|---|
| go, meet, arrive | place; time |
| pay, owe, split | amount; payee or payer |
| book, confirm, cancel, change | which item; when |
| bring, send, share, collect | what; to whom or from whom |
| decide, choose, approve | criterion |
| contact, ask, tell | whom; how, if the text names more than one channel |
| other act | name the act and the slots it needs, using only slot names (which, how many, who, what, when, where, standard). Never require world details |

**Judgment and emphasis words** (good, enough, a lot, actually, arbitrary, real, concrete) need a standard **only** when the task is *judge*, and the sentence itself gives no contrast or criterion.

**Group actors** ("we", "you all"): a particular member is needed only when the text divides tasks within the group, or when the act can only be done by some of its members. Otherwise the whole group is the actor, and no member needs naming.

**Step purpose.** A step given without its purpose needs a purpose only when the step involves a judgment (for example, "count heads": what to do if the count is off). Report other missing step purposes with `category: step-purpose`.

**Third reason (v6).** Before answering NOT-DEMANDED, check the Version 6 additions: if the sentence's main point rests on the thing (an undefined non-ordinary term, the members of a set the point is about, a juxtaposed connection, an ordinary word the sentence leaves open, or a side slot the text marks open), it is demanded regardless of task.

If nothing particular is needed, answer **NOT-DEMANDED**, and name the test that failed: "substitution: 'any approvals' same meaning", or "task = mention; no place needed".

## Step 2: in play and sufficiency (does the text single it out?)

**2a. In play.** Quote every alternative of this kind that the setting and passage:

- **introduce**, or
- **imply through a frame word.** Quote the frame word. The frames are:
  - trip or journey: lodging, transport, tickets, itinerary;
  - booking: the item booked, price, date, the login or account;
  - meeting or event: place, time;
  - purchase or bill: amount, payer;
  - API or service: endpoint, token, request;
  - document or report: sections, author;
  - other frame: you must quote the frame word and name the implied part.

Proper names are never implied. A name counts as in play only if the text introduces what it is.

**2b. Sufficiency.** Does the wording, together with what came earlier in the text or in the same sentence, pick exactly one of the alternatives in play, at the detail the task needs (from step 1b)? For "which one" questions, apply V5.1 before answering QUOTE.

## Answer values

| Value | Meaning |
|---|---|
| `QUOTE` | Exactly one candidate is in play at the needed detail. Quote the words that pick it, and for bridged items the frame word. |
| `LATER` | It is picked only after the point that needs it. Quote the later words. |
| `MULTIPLE` | Two or more candidates are in play and nothing picks one. Quote each. |
| `CONFLICT` | The text gives incompatible fillers, or a wrong actor or object. Quote both. |
| `CANNOT` | No candidate is in play at the needed detail. A name that is never introduced and a place that is never given are both CANNOT. |
| `NOT-DEMANDED` | Step 1 found that nothing particular is needed. Name the test that failed. |
| `UNSPECIFIC` | (V5.1) The thing can be identified only by going back to an earlier mention; the wording here does not pick it out. Quote the wording here, and put the earlier, fuller mention in "earlier_mention". |

A **gap** is LATER, MULTIPLE, CONFLICT, CANNOT or UNSPECIFIC.

## Connections between parts

Ask a relation question only when the text itself relates the parts. Quote the cue:

- an answer placed under a question;
- points placed under a claim or heading;
- a connective (so, because, but, therefore, then);
- ordered or dependent steps;
- two places describing, counting or requiring the same thing.

Separate notices in one message (an update, a briefing script, a list of admin items) need no link: answer NOT-DEMANDED, "no relation cue".

---

## Version 3 rules (apply in step 1 and step 2, before giving any gap answer)

**R1 — Explained right after.** If the filler arrives in the very next sentence, or a heading or label is defined by the section or list directly under it, the filler counts as supplied: answer QUOTE, quoting the later words. Answer LATER only when something in between must be acted on, decided, or understood using that meaning before the explanation arrives (for example, an instruction that depends on a term defined three paragraphs later).

**R2 — Openness the text declares.** If the text itself says the thing is not yet known, not yet decided, to be found out, or will be designed later ("to be decided", "found by judging the first 5", "the template is yet to be designed"), nothing particular is demanded: answer NOT-DEMANDED, reason "openness stated by the text", quoting the words that state it.

**R3 — Recommendations and instructions to the reader (narrowed in v3.1).** When the sentence tells the reader or addressee what to do (an imperative, "you should", "I recommend", "we suggest you"), the actor is the addressee **only if the text shows the addressees can do it themselves**. Check two things in the setting and passage:
- **Other possible doers:** does the text name other people or roles who could equally be the one to act (leaders, organisers, a co-leader, an admin, "someone")?
- **Means to act:** does the act need something the text gives only to some people (a login, a list, a key, a booking, a role or permission), or could it be done once for everyone ("pick up the vouchers": each for themselves, or one person for all)?

If neither applies, the participants slot is supplied by the addressee: answer QUOTE, quoting the words that address them. If either applies, the actor is open: answer MULTIPLE and quote the candidates (for example "each traveller || Sam || Ade"). Ask for a different actor also when the text divides the work among several people.

**R4 — General verbs and nouns in lists or summaries.** Before asking what an operation is (P11) or which item is meant (P01), apply the substitution test literally: in a list of responsibilities, capabilities or a summary ("own", "centrally own", "manage", "all of it"), the verb or noun names a general kind of activity or thing, so nothing particular is demanded: NOT-DEMANDED, reason "general term in a list/summary".

**R5 — Distinctive proper names.** A distinctive proper name (a product, tool, system, project, person or place name, e.g. "StoryOS", "Codex", "Airtable") identifies itself: the identity question is supplied by the name. A name can still leave a gap in another slot when the sentence's task needs a property the text does not give (e.g. "head to the Blue Door" needs a location). Generic-sounding labels ("the panel", "cards", "the API", "the system") are not distinctive names and still go through the identity test.

**Rule quotes (v3.2).** Whenever any of R1–R5 decides an answer, record which rule ("rule": "R1"…"R5") and quote the words in the text that made it apply ("rule_quote"). An answer decided without a rule leaves both fields empty.

---

## Version 4 additions

### V4.0 — The main point of each sentence
For each sentence (or heading, list item, table cell), identify its **main point**: the main verb phrase with its core parts (who/what does what to what), or what a heading or label asserts. The two new questions below are asked **only about the main point**, and **at most one word-meaning question and one connection question per main point**.

### V4.1 — Word meaning (new slot: SENSE)
- **Ask when (demand):** a **status, category, count or unit word** carries the main point (e.g. "complete", "state", "adopted", "used", "panel", "three", "the unit", "score") **and** the setting or passage supports **at least two different readings**, each tied to a quoted cue in the text. If you cannot quote a cue for each reading, answer NOT-DEMANDED (reason "no cue-supported second reading").
- **Supplied when:** a definition, contrast or example in the text fixes the reading — including in the very next sentence (R1). Quote it: QUOTE.
- **Otherwise:** MULTIPLE, quoting each reading with its cue ("reading A — cue '…' || reading B — cue '…'").
- **Precedence:** this question applies even where R4 ("general term in a list/summary") would otherwise exempt the word, when the word carries the main point.
- **qid:** "SENSE.a".

### V4.2 — Connection between two named things (new slot: CONN, four forms)
- **Ask when (demand):** the main point **would change depending on how two named things connect** — an instruction to use, do or decide about one thing with respect to another, a conclusion drawn from one about another, or a choice between them — **and** the text supports **at least two possible connections**, each tied to a quoted cue. If not, NOT-DEMANDED (reason "meaning does not depend on the connection" or "no cue-supported second connection").
- **Forms:**
  - **CONN.belong** — which [B] does [A] belong to / come from (system, table, experiment, change, earlier material)?
  - **CONN.relate** — how does [A] relate to [B]: same thing, part of, describes, uses, overlaps, differs from, shared or separate per item?
  - **CONN.work** — what does [A] do to/with [B], or under which condition does it apply?
  - **CONN.for** — what is [A] for: what is the plan, test, artifact or role meant to achieve?
- **Supplied when:** words in the text state the connection. Quote both things and those words: QUOTE.
- **Otherwise:** MULTIPLE (quote the possible connections with their cues) or CANNOT (quote both things; no connection stated).
- Structural relation questions about parts of the text (P27, P29) keep their quoted-cue requirement unchanged.

### V4.3 — Stricter "which one?"
When the setting or passage puts **two or more things of the same kind** in play (several tables, sets of workflows, implementations, experiments, documents), a "which one" question (P01, P03, CONN.belong) answers **MULTIPLE** unless the wording picks one. R4 (general terms) and R5 (distinctive names) do **not** exempt these cases.

---

## Version 5 addition

### V5.1 — Local wording
**Principle.** A reference is explicit when its own wording picks out the thing at the point where it is used. That the text mentioned the thing somewhere earlier, or that it is the only thing of its kind in the text, does not make a vague wording explicit. Example: after "the evaluation experiment" in one paragraph, a later "the experiment" is in the context but not in the wording.

**Applies to:** the "which one" questions (P01, P02, P03, P04, CONN.belong), after the demand test has found that something particular is needed. It applies even when only one candidate is in play.

**The wording picks the thing out, and the answer stays QUOTE, when any of these holds:**
1. **Distinctive name** (R5): "StoryOS", "Codex", "the Blue Door".
2. **Own description:** the wording carries the distinguishing words itself ("the evaluation experiment", "the March sweep", "the session token from step 2").
3. **Immediate pointer:** a pronoun or short reference ("it", "this", "the experiment") whose antecedent is in the same sentence or the immediately preceding sentence, with only one candidate there.
4. **Declared short form:** the text itself sets up the short form as a term or label for the thing ("the evaluation experiment (below, 'the experiment')", a heading that names it and the content directly under it).

**Otherwise** the answer is **UNSPECIFIC**: quote the wording here, and quote the earlier, fuller mention in "earlier_mention". If there is no earlier mention, keep the v4 answer (CANNOT or MULTIPLE).

**Same thing only (v6).** An earlier mention counts only if it names **the same thing**. A part, place or by-product of something named earlier ("reception" of a named hotel, "the departure gates" of a named station, "the booking confirmation" of a named bill) is not a re-mention: it is a new thing reached through a frame word, and step 2a's frame rules decide it. Do not answer UNSPECIFIC for it.

**Clarified in v6.1 — a shorter name for the same thing IS a re-mention.** "The same thing" does not mean the same words. A short or generic wording that refers back to a thing the text named earlier in fuller form — "the hotel" after "Hotel Miramar", "the money" after "the £400 deposit", "the experiment" after "the evaluation experiment", "the hut" after "the Bergli hut" — is a re-mention: apply V5.1 to it (UNSPECIFIC unless one of the four picking conditions holds, for example the fuller mention is in the same or the immediately preceding sentence). Only a *different* thing reached through the earlier one (a part, place or by-product of it) is excluded.

**Duplicates.** The same vague wording can be reported each time it recurs; report each distinct wording at least at its first use beyond the immediate-pointer window. Duplicates are acceptable.

**Not changed:** the demand test (step 1), R1–R4, the word-meaning and connection questions, and all non-identity slots.

---

## Version 6 additions — the third reason for demand

Step 1 recognised two reasons something particular is needed: the wording points at a particular thing (1a), or the act needs a value (1b, act list). Version 6 adds a third: **the sentence's main point rests on it.** "Task = mention" never makes these NOT-DEMANDED; the main-point test below decides instead.

### V6.0 — Main point (gate for V6.1–V6.4)
Use the main point from V4.0 (the main verb phrase with its core parts, or what a heading asserts). A heading counts. A **list item's label** carries the point only when the list itself is the point of its section (for example, a list of responsibilities or components under a heading that claims them); a label in a list of passing details (examples, side notes, a pilot's ingredients) does not. **Every V6 row quotes the main point** in the field `"main_point"`. Words outside the main point (examples, parentheticals, side clauses) never trigger V6.1–V6.4.

### V6.1 — TERM: what does this term mean? (new slot, qid "TERM.a")
- **Demanded when:** a term in the main point is **not ordinary vocabulary**.
- **Ordinary vocabulary** is a property of the language, never of a reader: the word or phrase, taken in its standard dictionary sense or its standard sense in the field the setting names, gives a meaning that makes the sentence's point. Examples of ordinary: "route code", "manifest", "flow", "candidate", "dis-benefit". **Not ordinary:** a coined phrase or compound ("capability distribution", "guidance match", "instance health"), a project label ("the gate", "the fence", "SEL"), or a word used in a special sense the language does not give ("a question splits", "vitality" of a route). Text cues that a term is not ordinary: capitals, code formatting, quotation marks, a coined compound. Under doubt, treat it as not ordinary.
- **Supplied when:** the text defines it, says what it does, lists its parts, or gives an example of it — before, in the same sentence, or right after (R1). Answer QUOTE with those words.
- **Otherwise:** CANNOT (LATER if it is explained only after something that depends on it).
- **Record** `"term_kind": "coined|special-sense|label|ordinary"`.
- **Precedence:** R4 (general term in a list/summary) applies **only to ordinary vocabulary**. A word with two cue-supported readings stays with SENSE.a; a non-ordinary term with no meaning given is TERM. At most one TERM question per term per passage (its first use in a main point).

### V6.2 — Set members (P01.b)
A count or set used as known ("the four layers", "the six sections", "both", "the other five") **demands its members when the main point is about the set** (the sentence states something about those members, or asks the reader to act on them). A count given as background or as a summary figure, where the point is elsewhere, stays NOT-DEMANDED. Supplied when the members are listed before, in the sentence, or right after (R1).

**Tightened in v6.1 — check the whole passage first.** Before answering a SET gap, look through the whole setting and passage. The set is supplied (QUOTE, quoting the members) when its members are stated **anywhere in the setting or passage**, including a list that introduces them under another name (e.g. "the four keys" after the four keys were listed earlier), or when the text points to where they are listed ("the other five are in the design document"). A SET gap is reported only when the members are stated nowhere in the text and no pointer is given.

### V6.3 — Juxtaposed connections (CONN gate addition)
In addition to V4.2: a connection is demanded when the text **places two things in one main point, or in adjacent sentences, and the point depends on how they connect, but no words state the link** (for example, a bug stated next to a process that stopped). Quote both things. Answer CANNOT if no link is stated, MULTIPLE if the text supports two links.

### V6.4 — SENSE.b: what exactly? (ordinary words left open)
An **ordinary** word or short phrase that carries the main point, whose referent or extent **the sentence itself leaves open** ("see" the keys — list, usage, or spend?; "something real"; "writing workflows"), asks "what exactly?" even without two cue-supported readings. Not for words whose standard sense already makes the point. Supplied when the text narrows it (QUOTE); otherwise CANNOT. qid "SENSE.b".

### V6.5 — Side details stay task-gated, unless the text marks them
For a sentence whose task is *mention*, side details (who acts in a side clause, where something is stored, which channel, which table holds a field) remain NOT-DEMANDED. **Exception (tightened in v6.1):** the slot is demanded only when the text **names two or more specific candidates** for it ("Jeremy/Art", "either the ops team or finance") and does not say the choice is left open. Plain indefinites ("someone", "some of you", "one of us") do **not** mark a slot by themselves. If the text says the choice is open or will be decided ("whoever owns data policy", "to be named"), R2 applies: NOT-DEMANDED.

### Reporting
Use these family tags in "category": `term` (TERM.a), `set` (V6.2), `conn-juxtaposed` (V6.3), `sense-b` (SENSE.b), `marked-side` (V6.5); otherwise `main` or `step-purpose` as before. UNSPECIFIC rows are reported separately from all other gaps.

---

## Version 6.2 rules (take precedence over the rules above where they conflict)

### V6.2-A — Short names: three questions (replaces the blanket part of V5.1)
A short generic name ("the pool", "the sizer", "the record", "the sheet", a role noun such as "the detector", an adjective used as a label such as "guarded") is explicit when every question that applies to it is settled:
1. **Which meaning?** Only for words with more than one meaning. "Pool" can mean a swimming pool or a pool of items. A cue in the text settles it. If the text supports two meanings, use SENSE.a and answer MULTIPLE.
2. **Of what / by what / for what?** Only for **relational** words, whose meaning carries an open "of / by / for": pool of, record of, size of, list of, log of, set of, sizer (sizes what), detector (detects what), guarded (by what). The **whole-kind** nouns (hotel, lobby, van, swimming pool, experiment, sheet, table) have no such slot. This question is **TERM.b** (new).
3. **Which one?** Every "the …".

**What may settle each question:**
- the name's own wording, including modifiers;
- **one earlier mention that fully names the thing, at any distance, provided no other thing of the same kind has been introduced since**;
- a quoted frame word that implies the thing ("apartment complex" implies one pool; "trip" implies one hotel).

The slot (question 2) is needed only at the detail the sentence's point uses.

**Where gaps go:**
- **TERM.b: a missing "of what" is reported once, at the word's first use.** Answer CANNOT, quote the word and its slot word ("of what"), and list later uses of the same word in the note as locations. Do not report each later use as a separate gap.
- **V5.1 / UNSPECIFIC now applies only when the identity question fails:**
  - another thing of the same kind was introduced after the defining mention: answer MULTIPLE when both fit, UNSPECIFIC when the wording fits only one but does not pick it out;
  - or no defining mention exists, in which case use the v4 answer (CANNOT) or TERM.b.

  A re-mention of one fully named thing with nothing of the same kind since is **QUOTE** (quote the defining mention and state "no other [kind] since").
- **Record `"head": "whole-kind|relational"`** on every short-name row.

### V6.2-B — Definitions must be made of defined words
- A non-ordinary term **inside a parenthetical, a gloss or a definition** of another term gets its own TERM.a question. The V6.0 main-point gate does not exempt it.
- A definition built from undefined terms supplies nothing. Example: "the SEL (gate · assess · prove)" leaves gate, assess and prove to be asked.
- In V5.1's "own description" condition, the description picks the thing out only if its descriptive words are themselves defined or ordinary. "The guarded detector" is not picked out when "guarded" is undefined; use TERM.b for "guarded".

### V6.2-C — Kind is not content
A label that says **what kind of thing** something is does not supply **what it says, contains or measures**:
- "its falsifiers (M1–M2)" does not say what M1–M2 state;
- "derives a 0–100 Benefit-case score" does not say what the score measures.

Answer QUOTE only when the content is stated. Otherwise CANNOT (TERM.a or P04.a).

### V6.2-D — A reported fact makes an indefinite particular
The substitution test (step 1a) does not apply when the text reports a **specific fact about** the indefinite thing: a number, a verdict or an outcome. Examples: "a real skill … scored 82", "two consecutive inquiries disagreed". The thing is then a particular one, and its identity is demanded.

### V6.2-E — R5 settles identity only
A distinctive name answers "which one". It does **not** answer what kind of thing it is, or how it relates to something else. Ask P04.a or CONN as usual. Example: "Freeform" picks a thing, but the kind of thing is still open.

### V6.2-F — An antecedent must be a single candidate
A pronoun or short reference is supplied only when exactly one candidate fits. A role noun in the setting ("a colleague", "a prompts table") supplies it only if it is the only candidate of that kind. Otherwise answer MULTIPLE (quote the candidates) or CANNOT.

---

## Version 6.3 rules (take precedence over everything above where they conflict)

### V6.3-A — Coverage: one SENT row for every sentence (required)
Before any question rows, and for **every** sentence of your section (headings, list items, table cells and quoted lines each count as a sentence), write one row:

```json
{"unit": "...", "line": <line number if the text has them>, "qid": "SENT", "answer": "COVERED",
 "sentence": "<the first 60 characters of the sentence, copied exactly>",
 "main_point": "<its main point>", "questions_asked": <number of question rows you wrote for this sentence>}
```

- `questions_asked` may be 0 only when, after the checklist in V6.3-B, every trigger in the sentence was checked and nothing applies. Then also give `"no_gap_reason": "<one phrase>"`.
- No sentence may be skipped. Before you finish, read your SENT rows back against the text, line by line, and add a row for every sentence that has none.

### V6.3-B — The trigger checklist (for every main point)
For each sentence's main point, check each of the following and write a question row for every one that applies:

| Check | Question |
|---|---|
| A definite noun or count used as known | P01 |
| A pronoun or short reference | P02, with V6.2-F |
| A term that is not ordinary vocabulary | TERM.a |
| A relational word ("of what / by what / for what") | TERM.b |
| A word with two cued readings | SENSE.a |
| An ordinary word the sentence leaves open | SENSE.b |
| A negation or restriction ("not about X", "only X", "except") | P13.d: what is excluded, and what is it set against |
| A change or comparison ("did not move", "rose", "cut", "better", "this time") | P19.a, against what baseline, and P11.a, what concretely happened |
| A rule, default or scope ("for small tasks", "a format that admits no …", "by default") | P18.a: which cases are inside or outside |
| A judgment or emphasis word on which a decision rests | P16 |
| An act on a task | the act-list slots |
| Two things placed together, or a connective | CONN, P27–P31 |
| A count followed by a list | P01.b: do the listed members match the stated number? |

A phrase can need **more than one** question. Write one row per question. **The V4.0 cap of one word-meaning question per main point is lifted.** If a phrase has two open words ("the pattern's category"), each gets its own row.

### V6.3-C — Who produced or checked the support (new demand reason)
When a statement's main point **rests on evidence** (an observation, a reading, an audit, a check, a report) whose producer is not stated, ask **"by whom / from what source?"** (qid "SRC.a"), even in a mention sentence. V6.5 does not exempt this. Examples:
- "correct on audit": audited by whom?
- "four readings appeared in the record": whose readings?
- "some reports suggest X": which reports?

This applies only when the claim's support depends on who or what produced it, not to every passive.

### V6.3-D — Narrowing V6.2-E (names): ask a name's kind only when the point rests on it
A distinctive name answers "which one". Ask what kind of thing it is (P04.a) **only when both hold:**
- the sentence's main point depends on the kind;
- no cue in the text gives the kind.

Personal names in a team setting ("Christine", "Bob", "Allistair") and product or tool names used as tools ("n8n") are complete referents: do **not** ask "who is X" or "what kind of thing is X". Example of a valid ask: "set Freeform to X", where whether Freeform is a model or a workflow decides the action and nothing says which. If the text says "the workflow's instructions … Freeform", the kind is given.

### V6.3-E — Narrowing V6.2-F (pronouns): MULTIPLE only when the readings differ in meaning
Answer MULTIPLE for a pronoun or short reference only when the candidates lead to **different meanings** of the sentence. If they are the same thing under two names (the row and its copy), or the sentence means the same either way, answer QUOTE and name the candidates.

---

## Version 6.4 gates (take precedence over everything above where they conflict)

Coverage stays exactly as in V6.3-A: a SENT row for every sentence, and the V6.3-B checklist run on every main point. These gates decide only **when a check that applies produces a gap**. If a gate is not met, write the question row with NOT-DEMANDED and name the gate. Do not omit the row.

### V6.4-A — "By whom / from what source" (SRC.a) only for results on the main line
Ask SRC.a as a gap only when both hold:
1. the evidence verb (judged, predicted, measured, audited, recorded, observed, verified, found) is the **main verb of the main point**, so the sentence reports a result;
2. the result would be a different claim depending on who or what produced it.

It is NOT-DEMANDED:
- when the source is incidental to the sentence's point ("the spend figures show …", "the archive was checked");
- when an earlier step of the same text says who does it.

### V6.4-B — Connections need two cue-supported readings that change the point
CONN and juxtaposed connections (V6.3 checklist, V6.3 CONN-J) give a gap only when **two different connections** are each supported by a quoted cue, and the main point changes between them. Examples:
- "→" could mean "replaces" or "adds to";
- "so" could mean "caused" or "followed".

NOT-DEMANDED:
- conventional diagram arrows whose reading is the usual one ("Employee → Codex" = uses);
- links stated by a heading or the next sentence;
- mechanism detail that the point does not use.

### V6.4-C — SENSE.b only for open actions, steps, objects and amounts
SENSE.b ("what exactly?") gives a gap only for a word that names:
- **an action or process** ("refresh", "retire", "calibrate", "see");
- **a step** ("one step away");
- **an object or amount** ("some admin", "something real" as the thing to measure);

and only when the sentence leaves its concrete content open.

**Not** for descriptive or evaluative words used loosely ("friction", "dead", "answerable", "clean"), where the point does not depend on a precise sense. Those are NOT-DEMANDED (reason: "descriptive word, loose sense suffices").

SENSE.a (two readings) gives a gap only when the two cued readings lead to **different conclusions or actions**.

### V6.4-D — What the checklist must not turn into gaps
The following are NOT-DEMANDED even when a checklist item applies:
- **Illustrative examples.** The specifics of an example given only to illustrate a point ("one June API key spanned three flows"): which key, which flows.
- **Contrast classes.** "The only family that …", "unlike the others": the other members need not be listed.
- **Loose summary phrases.** "All of it", "the rest of the setup", when the sentence summarises rather than instructs.
- **Purpose already stated** in the same or the next sentence, or a heading, for "what to do with X".
- **Explained later (V6.5, replaces the v6.4 rule).** Only an explanation in the same sentence or the very next sentence counts as supplied (QUOTE it). An explanation further on, anywhere in the passage or document, does **not** count as supplied and does **not** make the slot NOT-DEMANDED: answer LATER with the later quote. The reader needs the meaning where it is used.
- **Implied by the act.** "Updated to what" when the sentence's switch names the new value.

---

## Slots and their questions

Each question below is asked only after steps 1 and 2. The pattern IDs follow the catalogue.

### Slot 1 — Identity: which one?

- **P01:** a definite generic noun, or a count or set used as known ("the plan", "the booking", "the five", "both").
  - **P01.a** — Which particular one?
  - **P01.b** — For counts: which members?
- **P02:** a pronoun or shorthand pointing back.
  - **P02.a** — What does it point back to? Use MULTIPLE if two or more fit.
- **P03:** an object of a kind that the text shows in more than one place, system or version.
  - **P03.a** — Which one?
- **P04:** a name or label used as if known.
  - **P04.a** — What is it? Is it introduced?
- **P06:** an action on something that exists both as a record and as the thing it records.
  - **P06.a** — The thing, the record, or both?

### Slot 2 — Quantity and extent

- **P13:** an action on a plural or mass object, or extent words ("some", "the rest", "everything").
  - **P13.b** — All or some? Which ones?
  - **P13.c** — How much, or how far?

### Slot 3 — Participants

- **P12:** the actor of an act-on task. Triggers: a passive of an action someone must carry out, an action noun, "someone", or an instruction to a group.
  - **P12.a** — Who performs it?
  - **P12.b** — Which member, if the act is divided among the group?
  - **P12.c** — Does the text say someone else actually does it? If so, CONFLICT.
- **P13:** the target of the act.
  - **P13.a** — What exactly does the act apply to?
  - **P13.d** — What is excluded, when the sentence excludes something?
- **P14:** an instruction inside material that has more than one audience or surface.
  - **P14.a** — Who is told to do it?
  - **P14.b** — Is a change of addressee marked?

### Slot 4 — Event

- **P10:** objects, or a case raised, with no action stated.
  - **P10.a** — What is to be done with the objects?
  - **P10.b** — What is to be done if the case happens?
- **P11:** a broad verb or action noun in an act-on or claim sentence ("sort out", "handle", "check").
  - **P11.a** — What concretely happens?
  - **P11.b** — What results?

### Slot 5 — Circumstance

- **P20:** a condition in an act-on or judge task ("if still…", "a lot").
  - **P20.a** — What state or sign meets the condition?
  - **P20.b** — After how many tries, or by when?
- **S5.time:** a relative time, where two or more dates or times are in play.
  - **S5.time.a** — Which date or time? Use MULTIPLE if several fit.
- **Place** (from the act list): where?

### Slot 6 — Standard (task = judge only)

- **P16:** a judgment word on which a decision or conclusion rests.
  - **P16.a** — By what standard?
  - **P16.b** — For a judgment-type step: what is it for?
- **P17:** a sufficiency or readiness claim ("enough", "ready", "done") that a decision rests on.
  - **P17.a** — Enough, or ready, for what?
- **P18:** a rule, default or exemption.
  - **P18.a** — Which cases are inside it and which are outside?
  - **P18.b** — Exempt from what, or covering what?
  - **P18.c** — Over what time does it apply?
- **P19:** a comparative or change.
  - **P19.a** — Compared with what? The baseline must be in play.

### Slot 7 — Relation (only with a quoted cue, as above)

- **P07:** a method or tool applied to material.
  - **P07.a** — What does each contribute?
- **P08:** two named things placed together.
  - **P08.a** — How are they related?
  - **P08.b** — Evidence of what?
- **P27:** points under a question or claim.
  - **P27.a** — Which question does each point answer, and does each support the claim?
- **P28:** a contrast.
  - **P28.a** — Real alternatives, or linked steps?
- **P29:** a shift of topic within an answer or argument.
  - **P29.a** — What links it?
- **P30:** the same thing stated in two places.
  - **P30.a** — Do they agree?
- **P31:** dependent steps.
  - **P31.a** — Is the order or dependency stated?

### Where the filler lives

- **P22:** details of an example given before its situation.
  - **P22.a** — Is the situation introduced first?
- **P24:** audience-facing material that relies on private notes.
  - **P24.a** — Does the explanation reach the audience?
- **P25:** an agreement or decision that is referred to ("as agreed", "given X's decision").
  - **P25.a** — What was agreed or decided?

---

## Output: one row per trigger and question

```json
{"unit": "T01", "trigger": "<exact words>", "pattern": "P01", "qid": "P01.a",
 "task": "mention|act-on|judge", "task_quote": "<words showing the task>",
 "demand": "YES|NO", "demand_reason": "<the failed test, if NO>",
 "in_play": "<quoted candidates, ' || ' separated, with any frame word>",
 "answer": "QUOTE|LATER|MULTIPLE|CONFLICT|CANNOT|UNSPECIFIC|NOT-DEMANDED",
 "earlier_mention": "<for UNSPECIFIC: the earlier, fuller mention; else empty>",
 "main_point": "<quoted main point, required for V6 rows and SENSE/CONN rows; else optional>",
 "term_kind": "<for TERM.a: coined|special-sense|label|ordinary; else empty>",
 "head": "<for short-name rows (V6.2-A): whole-kind|relational; else empty>",
 "quote": "<picking words / later words / candidates / both conflicting quotes>",
 "category": "main|step-purpose|term|set|conn-juxtaposed|sense-b|marked-side",
 "rule": "R1|R2|R3|R4|R5|", "rule_quote": "<words that made the rule apply, or empty>",
 "note": "<15 words max>"}
```

