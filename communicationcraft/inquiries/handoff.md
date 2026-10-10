
# Communication Craft: where we are, what we understood, and where to go next

A handoff for a fresh session. Written 10 October 2026. It covers the work of 8–10 October, with the weight on 9–10 October. The findings themselves are in `findings-merged-2026-10-08-to-2026-10-10.md` beside this file; this document says what they add up to.

**Terms used here:**
- **Communication Craft:** the communication part of Workcraft, the owner's framework for automating work through AI. It has two parts: theory and methodology, and skills an AI can execute.
- **A finding:** the written result of one inquiry, produced by the Traverse method. Each has a question, an answer, the reasons, and next actions. Later findings refine earlier ones; corrections are appended as dated notes, never by rewriting.
- **The owner:** the person this project belongs to. They own AlignCraft, Workcraft and Communication Craft, and they adopt or decline every rule the AI proposes.
- **This project is standalone.** It must not use material, skills, catalogues, people or products from other local projects. Two findings from these days were built on another project's product and are left out of the merged file.

---

## 1. Where Communication Craft stands

**The design, in one picture (the owner's diagram, which is correct and is not to be redrawn):**

```
Raw Context  →  Comm Substrate  →  Materialisation
         ◇ Alignment Check ◇   ◇ Alignment Check ◇
```

- **Raw context:** the material a text draws on: facts, figures, evidence, earlier messages, the request.
- **The substrate, or the brief:** the written account of what one text must achieve and say, made before the text. The owner's word for it is "the communication brief"; it has its own format.
- **The text** (materialisation): what the recipient receives.
- **The two checks:** the brief against the raw context; the text against the brief. Each runs all six AlignCraft layers.
- **Outside the diagram, in the workspace:** the **base reference**, the written rules for what every text of a kind should be.

**Built and measured:**
- the explicitness detector and fixer (public, in the workcraft repository under `communicationcraft/skills/`). The detector's rules found 79–82% real gaps against 65% for the same AI with no rules; the fixer resolved 50 of 56 planted gaps with the author's answers;
- two benchmarks;
- a written method for building any further check, with rules for measuring it honestly (`core/evolution-of-the-explicitness-test.md`).

**Theory only (findings, no implementation):**
- the brief: its concept, its contents, its shape, how its entries are formed;
- the two alignment checks;
- the base reference: its structure, with drafted but untested rules.

**Not existing:**
- any written brief format;
- any end-to-end loop from raw context to a checked text;
- any measure of the quality of a created text.

**The public face is stale.** The repository's README still says "Communication — v1 complete" and lists older skills the owner has since ruled outside this project, with links that point outside the repository. The Communication Craft overview links to findings the repository does not hold. The owner has not yet decided how to correct this.

---

## 2. What we understood, in the order it came

### 8 October: what sits behind a text

- **Develop the substrate through one concrete use** (12-40). Not a complete general substrate first; not independent tools that are later merged. One useful communication operation, together with the understanding needed to perform and inspect it. Share parts only when two uses show they are common. "Build the substrate" names five different jobs: understand the concept; establish one exchange's understanding; choose a representation; develop a formation method; create shared support.
- **Two kinds of check** (13-08). *Is the meaning well expressed?* (fixed by rewriting) and *is the meaning right?* (fixed by changing the meaning, getting information, or doing the work). The deciding test: where can the right meaning be quoted from? From what the author has settled: rewrite. Only from the sources, or from nowhere: content.
- **Three fundamental gaps** (15-59): need, meaning, conveyance. Adequacy is the verdict, not a fourth gap. What counts as supplied: the text, its stated setting, earlier turns, conventions of the genre, declared shared ground. Never undeclared reader knowledge.
- **The need** (16-18) is the recipient's state: what they will do next and what that raises. The request is evidence of the need, not the need. Conventions count only if they can be quoted; "readers usually want…" is not a source, it becomes a visible assumption written in the text.
- **Several parties** (16-28): place each holder by where they stop reading; a text that will be forwarded must survive forwarding.
- **How an essence gets formed** (15-47): by answering the questions the recipient's next act raises, one at a time; the facets of the substrate are a final sweep, not a form to fill.

### 9 October: the unit of meaning, what may be left unsaid, and how parts belong together

- **The meaning unit** (16-16): a point, what is done with it (stated, asked, decided, offered), and its internal limits; units are linked by relations. Each unit has a *standing*: how firmly it is held and on what basis, with quotable entry conditions. Meaning must be *quotable, with its standing, when a check needs it*; it need not all be written in advance. **An AI never marks its own units as settled.**
- **Conveyance** (16-52): a text may leave something unsaid on three grounds only: it is supplied; any reasonable choice gives the same result; or the text declares it open. The explicitness bank's exception rules all fit these grounds. Where the rules had been written as surface stand-ins ("one end state"), they leaked. The strict form (each alternative with its own result) fixed the leak but found no more gaps: the three grounds are a precision principle, not a recall lever.
- **Where an answer comes from** (17-15): settled by the author; gathered from a source; produced by reasoning; asked; or left open. "Asked" is temporary; "left open" is final for this exchange.
- **The substrate's shape** (19-31): the substrate had the right contents in separate sections and never said how they hang together: which requirement matters most, which point answers it, and what each fact does for which point. Reading order follows rank. The main point is declared, with its standing; undeclared means undecided.
- **Harmony** (19-42, 20-02, 21-40): the parts of a communication belong together as one whole. Four kinds at first (the through-line, the skin, who-to-whom, due weight), judged by *belonging, not sameness*: a shift breaks harmony only when it does not serve the whole or changes what the reader takes. "Every quality is an agreement with something."

### 10 October: alignment as the family, the base reference, and the build

- **Content harmony** (07-57): a fifth kind, broken only by a change of meaning. The five kinds (content; the path of the telling; the skin; who-to-whom; due weight) are each broken by one kind of change. The substrate is a *level*, not another kind: check the substrate, then the text, then that the text matches it. "A declared tension is not a clash"; "restore the limit first".
- **Alignment is the family** (09-00). Every quality of a communication is a kind of alignment: agreement between what was meant and what is understood or produced. Six layers (workspace, task, action-space, action-set, coherence, outcome) across two relationships (author–drafter; sender–recipient). All six are required for every draft. **AlignCraft's four pillars are how context is uncovered so it can be aligned; they are never project tools.** The owner corrected an earlier mapping of pillars onto tools; the correction is permanent.
- **The diagram, read** (11-29). Checks of a text on its own (explicitness; parts belonging together) are the reader's side of alignment, judged against rules writer and reader share. **Textual integrity** has three parts: determinate (the wording singles out what it needs), consistent (the parts belong together), readable form (the medium can show it). An integrity check detects; the comparison against settled meaning decides (fixed, asked, or declined). Explicitness sits at the action-set layer.
- **"Something is off" is a comparison** (13-28). It compares the text with what every text of its kind should be. Those expectations belong, written, in the workspace's base reference; checking against them is alignment with the workspace. There are two scopes of "what was meant": for every text of this kind (the base reference) and for this text (the brief). Not a seventh layer. **The base reference holds:** three principles set by what each check compares the text with (textual integrity; faithful; fit); rules with their reason, exceptions and a test pair; parts for each kind of text; the workspace's own decisions as a style sheet; cited standards. Rules that protect readability and faithfulness are floors a workspace cannot lower; conventions can be overridden locally. Exceptions count only when shown, never by matching a surface condition. Only explicitness is measured as something the AI does not already do on its own.
- **Implicit contracts** (14-41). An unwritten expectation is a contract the AI fills with its trained defaults, and the same defaults then judge the result. Write every expectation someone will hold the work to, unless it is shared, makes no difference, or a cited standard already says it. High-stakes expectations are always written. Competence stays implicit. A chapter "Implicit Contracts" is proposed for AlignCraft; the owner has not decided.
- **The next step** (18-29, then corrected twice the same day; the diagnosis is 19-51). The answer "yes, the substrate is the focus" stands. The plan under it was wrong: it offered checks and rules in place of the brief, and then listed the material inside the brief. **The corrected direction:** build the brief's format first; fill it on real texts; write from it; only then the checks. And the brief *refers to* its material; it does not carry it.

---

## 3. The model as it stands now

**Five kinds of written thing, and what each may hold:**

| Kind | What it is | What it holds |
|---|---|---|
| **raw context** (an object) | the material | facts, figures, evidence, earlier texts, the request |
| **the brief** (an object) | one text's account, made before writing | decisions: who the reader is and what they need; the main point and the key points, each with what it does and its limits; how firmly each holds; what is left open; the ask; the order. **For each point, a reference into the raw context: where its basis is, and how firmly it holds. Never the material itself.** |
| **the text** (an object) | what the recipient receives | the brief's decisions, expressed |
| **a check** | a comparison between two objects | brief against raw context; text against brief; plus the text's own integrity |
| **a rule** (the base reference) | what every text of a kind should be | principles; rules with reasons and exceptions; kind parts; the workspace's style sheet |

**The owner's two corrections that fix the brief's boundaries:**
- "substrate is the communication brief and it has its own format like it is different from the checks";
- "Brief should say like if there's this point, it should mention the raw context, but it should refer to it. And it can talk about it, but … it doesn't include it itself."

**Settled:**
- the diagram and its two checks;
- alignment as the family; the six layers; the pillars as uncovering, never tools;
- textual integrity's three parts;
- the three grounds for leaving something unsaid, shown strictly;
- the brief holds decisions and references, not material;
- the base reference's structure;
- write the brief's format before any check or tool.

**Open in the theory:**
- what a reference inside the brief must contain so that writer and checker land on the same material;
- where a decision made while writing the brief lives, since no raw context holds it yet;
- how long a point's sentence may be before it stops being a decision and becomes material;
- the edge of the brief's depth for short texts against long ones;
- whether the path of the telling is a kind of harmony on its own (no real text yet shows it failing alone);
- when a wording "demands" one particular thing (the boundary of the implicit; the bank's open edge).

**Waiting on the owner:**
- how to correct the public README (a one-line pointer was recommended as the minimum);
- the AlignCraft chapter "Implicit Contracts" and its four edits;
- the names: "textual integrity" for the first principle; whether to stop using "standing" in Communication Craft, where it already means a unit's basis;
- the proposed wording notes appended to 07-57, 11-29 and 19-31 (the brief refers to material, does not carry it): keep, edit or remove;
- consent to use past session transcripts, filtered to this project, as test material;
- the proposals for the Traverse method: an articulation reading "what is X; show one"; a trigger on "build X"; a critique dimension "produces the object named".

---

## 4. The direction the knowledge moved, and where it should go next

**How it moved.** The work started on the text alone (explicitness: can the wording be read one way?). It then moved behind the text, to what a text is made from: the need, the meaning units, what may be left unsaid, the brief and its shape. Then it moved around the text, to the frame that holds all of it: alignment, the six layers, the two checks. Then to the rules every text is held to: the base reference and the implicit contract. The last step was the build plan, which went wrong by reaching for checks again, and was corrected.

**The drift to watch.** The project has a strong pull toward checks and measurement, because they are what it has built and measured. Three times in three days a familiar thing was offered in place of the thing asked for (tools for pillars; checks for the brief; material for a reference). The guard is to read from the diagram: name which kind each deliverable is before sending it.

**Where to go next, in order.**
1. **The brief's format, version 0.** Its sections (from section 3's table), a short guide to filling each, and one filled example. Build nothing else first. The three open questions above are answered by doing this.
2. **Fill it for real texts of this project.** The AI's own reports and findings to the owner are the available first use: a present recipient, real corrections, no other project's material. Early, add one message to someone else built from sources (the README's Communication section is a candidate), because only there do all of the brief's sections come into play.
3. **Write each text from its brief.**
4. **Only then the checks:** does the brief capture and answer the literal question, faithfully to the raw context? Does the text follow the brief? The existing explicitness detector runs on the text. The owner's marks are the outcome. A comparison with texts written without a brief shows whether the brief earns its place.
5. **Revise the format from what fails; then make it a tool.**
6. **A second, different use;** then the full base reference, the shared parts, consolidation, and publishing.

**What not to do next:** more theory-only inquiries; a universal substrate tool before two uses; tools before the written format; any rule for every text drawn from one recipient.

---

## 5. Working rules for the new session

- **Standalone.** Use only this project's material and public outside sources.
- **Build the thing asked.** When the owner names a thing to build, step one produces that thing in its own format. Put a kind column (object / check / rule / material / reference) on every plan and every list of what something holds. A finding that says "build X" shows a version-0 instance of X.
- **Open with a one-line direct answer** to the owner's literal question. Define terms before using them. Plain words.
- **One relation and one reference per concept.** Never relate concepts by a shared word or a shared feature; relate them by their role in the design. Generic scope; examples only as tests.
- **No reader profiles.** Checks judge the text and its stated setting, never what a reader happens to know. The owner's judgments count as outcomes and as workspace conventions, not as rules for every text.
- **Detect, then decide.** A check finds a deviation; what the author has settled decides whether it is a fault. An AI never settles its own meaning or its own rules; the owner adopts.
- **Resolve edge cases by a general principle,** then re-test; never case by case.
- **Record changes as dated notes** on earlier findings; never rewrite them.
- **Full depth.** Read sources in full; reason fully; quote.

---

## 6. What to read first

1. This file.
2. `findings-merged-2026-10-08-to-2026-10-10.md`: all 21 findings of these days, in order. If time is short, read 13-28 (the base reference), 18-29 with its three notes (the plan and its corrections), and 19-51 (what went wrong and the guard).
3. The public overview: `communicationcraft/docs/what_is_communication_carft.md` in the workcraft repository.
4. The diagram: `communicationcraft/benchmarks/explicitness/commcraft.drawio.png`.
5. `core/evolution-of-the-explicitness-test.md`: how the one built check was made and measured, and the method for making the next.
6. The 8 October review of the earlier 73 findings: `Communication Craft/essential-findings-review/essential-findings.md`.
