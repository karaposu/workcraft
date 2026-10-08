
# Explicitness bank

**What it detects.** An explicitness gap is a place where the wording demands a specific thing (which one, how many, who, what happens, when or under which condition, by which standard, how things connect) and the text does not supply it before it is needed.

**No reader.** Nothing in this bank asks what a reader knows, would find plausible, or would do. Statements in the setting about what the reader has or has not seen are not fillers. Only facts stated in the text are.

## The text

The **text** is the setting plus the passage.

- A filler counts as **supplied** if it is stated earlier in the setting or the passage, or in the same sentence.
- A filler that appears only **after** the demanding wording counts as LATER.
- Nothing outside the setting and passage counts: no general knowledge of the domain and no guesses.

## Answer values

Every question is answered with exactly one of these:

| Value | Meaning |
|---|---|
| `QUOTE` | The text supplies the filler before or at this point. Give the exact words. |
| `LATER` | The filler appears only after this point. Give the exact later words. |
| `MULTIPLE` | The text offers two or more candidate fillers, and nothing picks one. Quote each candidate. |
| `CONFLICT` | The text supplies fillers that are incompatible, or states that the actor or object is something other than what actually does it or is acted on. Quote both. |
| `CANNOT` | The text does not supply the filler. |
| `NOT-DEMANDED` | On a close look, this wording does not demand a specific filler: a generic or indefinite use ("some friends", "trains are faster"), or the question does not apply. Say why in a few words. |

A **gap** is any answer of LATER, MULTIPLE, CONFLICT or CANNOT.

## How to use

1. Go through the passage sentence by sentence. Include headings and list items.
2. For each sentence, mark every **trigger**: wording listed below that demands a filler.
3. Ask each listed question for that trigger. One wording can trigger several questions, from different slots.
4. Answer each question with one value and its quote.

Ask every question that applies. Each question is a separate check, so finding one gap in a sentence does not finish that sentence.

---

## Slot 1 — Identity: which one?

**P01 — A generic noun, number or set used for one particular thing**
- **Triggers:** a definite generic noun ("the plan", "the list", "the booking", "the deposit", "the group", "the station"); "the usual X"; a count or set used as known ("the five", "both", "the others", "everyone").
- **P01.a** — Which particular thing or set is meant? Quote the words that identify it.
- **P01.b** — *(counts and sets only)* Which members make up this count or set? Quote them.

**P02 — A pronoun or shorthand pointing back**
- **Triggers:** it, its, this, that, these, those, they, them, he, she, there, then, the same, the other, the former, the latter, one, both.
- **P02.a** — What does it point back to? Quote the antecedent. Use MULTIPLE when two or more candidates fit.

**P03 — An object that exists in more than one place, system or version**
- **Triggers:** a noun for an object of a kind that the text shows existing in more than one place, system, version or instance (two bookings, two stations, several drafts, two chats, two tables).
- **P03.a** — Which place, system, version or instance is meant? Quote the words that pick it.

**P04 — A name used as if known**
- **Triggers:** a proper name, label, feature, place, team or capitalised term used without introduction.
- **P04.a** — What kind of thing is this name, and where or what is it? Quote the words that introduce it.

**P06 — A record or the thing it describes**
- **Triggers:** an action on something that the text shows existing both as a record, entry or listing and as the real thing (a calendar entry and the booking it records; a database row and the workflow it describes).
- **P06.a** — Is the action on the thing itself, on the record about it, or on both? Quote the words that decide.

## Slot 2 — Quantity and extent: how many, all or some?

**P13 (extent) — How much of the target**
- **Triggers:** an action on a plural or mass object ("send the photos", "pay the bill", "copy the times"); extent words such as some, a few, the rest, extras, everything, anything, any, part of.
- **P13.b** — All of them or some? If some, which ones? Quote the words.
- **P13.c** — How much, or how far, does it reach? Quote an amount or limit.

## Slot 3 — Participants: who acts, on what, and who is addressed?

**P12 — The actor**
- **Triggers:**
  - a passive of an action someone must carry out ("will be booked", "has to be picked up", "needs to be paid", "is verified");
  - an action noun ("approval", "payment due", "check-in", "pick-up");
  - "someone", "we'll", "you all";
  - an instruction to a group.
- **P12.a** — Who or what performs this action? Quote the words.
- **P12.b** — *(group actor only)* Which member or members of the group act? Quote the words.
- **P12.c** — Does anything in the text say that a different person or system actually performs it? If yes, answer CONFLICT and quote both; otherwise NOT-DEMANDED.

**P13 (target) — What the action applies to**
- **Triggers:** an action verb whose object is unstated or general (book, pay, bring, cancel, split, cover, collect, send, check, confirm, pack, share, remove, update, clean up).
- **P13.a** — What exactly does the action apply to? Quote the words.
- **P13.d** — *(only when the sentence excludes something: but, except, leave, separate, apart from)* What exactly is excluded, and from which operations? Quote the words.

**P14 — Who an instruction addresses**
- **Triggers:** an instruction inside material that has more than one audience or surface (a script read aloud, a message to several people, a customer-facing line).
- **P14.a** — Who is told to do this? Quote the words that name the addressee.
- **P14.b** — If the addressee is not the audience hearing or seeing the material, does the text mark the change? Quote the marker.

## Slot 4 — Event: what happens?

**P10 — Objects or a case with no action**
- **Triggers:** a sentence or fragment that names objects without a verb saying what happens to them; a raised case ("if there are several", "in case of rain", "for late arrivals").
- **P10.a** — *(objects)* What is to be done with these objects? Quote the action.
- **P10.b** — *(case)* If this case happens, what is to be done? Quote the action.

**P11 — A broad verb or action noun**
- **Triggers:** sort out, handle, deal with, take care of, process, check, verify, look at, review, fix up, organise, follow up, the rest (as an action), "verification", "follow-through".
- **P11.a** — Concretely, what operation is this? Quote the words that make it concrete.
- **P11.b** — What exists or has changed afterwards? Quote the result.

## Slot 5 — Circumstance: when, under which condition?

**P20 — A condition or threshold**
- **Triggers:** if still…, if it goes up a lot, when critical, if anything changes, if needed, if it differs, in case of problems.
- **P20.a** — What state or sign means the condition is met? Quote the test.
- **P20.b** — *(repeated attempts or waiting)* After how many tries, or by when? Quote the words.

**S5.time — Time (an addition beyond the catalogue)**
- **Triggers:** relative or deictic times (tomorrow, next Friday, later, soon, before eight, the weekend, by then, the same day) when more than one date or time could be meant.
- **S5.time.a** — Which date or time exactly? Quote the words that fix it. Use MULTIPLE when the text allows two or more.

## Slot 6 — Standard: by what measure, compared with what, within which boundary, for what?

**P16 — A judgment word or a step without its purpose**
- **Triggers:** good, right, best, decent, proper, fine, reasonable, nice, early, cheap, comfortable, suitable, smart, worth it, a lot, normal, light, small; or a step given with no purpose.
- **P16.a** — By what standard, or for what purpose, is this judged? Quote the words.
- **P16.b** — *(step without purpose)* What is this step for? Quote the words.

**P17 — Sufficiency or readiness**
- **Triggers:** enough, sufficient, complete, ready, done, set, sorted, covered.
- **P17.a** — Enough, or ready, for what use? Quote the words.

**P18 — The boundary of a rule, default, recommendation or exemption**
- **Triggers:** unless, except, only, most, usually, covers, included, free, exempt, allowed, not needed, optional, as long as, everything (in a rule), normal use, trusted.
- **P18.a** — Which cases fall inside the rule and which fall outside? Quote the boundary.
- **P18.b** — Exempt from what, or covering what, exactly? Quote the words.
- **P18.c** — Over what time does the rule apply: once, every day, or the whole trip? Quote the words.

**P19 — A comparison**
- **Triggers:** comparatives (shorter, cheaper, faster, higher, better, more, less, closer), "now" plus a change, different, changed, instead.
- **P19.a** — Compared with what? Quote the baseline.

## Slot 7 — Relation: how things and statements connect

**P07 — A method or tool, and the material it is used on**
- **Triggers:** a method, tool, framework or app named together with material ("put the suggestions through an app", "check X against Y").
- **P07.a** — What does the method or tool contribute, and what is done with the material? Quote the words.

**P08 — Two named things**
- **Triggers:** two named things placed together where one may describe, use, contain, overlap with, or be the same as the other ("the kitty card and the trip account"); "outside it"; evidence stated without a subject.
- **P08.a** — How are these two related: same thing, parts of one thing, one using or describing the other, or overlapping? Quote the words.
- **P08.b** — *(evidence)* What is this evidence evidence of? Quote the words.

**P27 — Parallel points (a structural trigger)**
- **Triggers:** several points or list items placed under a question, heading or claim.
- **P27.a** — Which question does each point answer, and does each support the claim? Quote the link for each point.

**P28 — A contrast**
- **Triggers:** not X, instead of, rather than, one … not many, either … or.
- **P28.a** — Are these genuine alternatives, or connected or sequential steps? Quote the words that settle it.

**P29 — A change of topic, level or surface (a structural trigger)**
- **Triggers:** consecutive sentences or surfaces on different subjects, with no connecting words.
- **P29.a** — What links the new topic to the previous one? Quote the transition.

**P30 — The same thing stated twice (a structural trigger)**
- **Triggers:** two places that define, describe, count or require the same thing.
- **P30.a** — Do they agree? If not, answer CONFLICT and quote both.

**P31 — Steps or parts that depend on each other (a structural trigger)**
- **Triggers:** two actions or parts where one can only work after or with the other.
- **P31.a** — Is the order or dependency stated? Quote the words.

## Order and source: where the filler lives

**P22 — An example's situation**
- **Triggers:** details of an example or scenario being used, compared or checked.
- **P22.a** — Is the situation the details belong to introduced before them? Quote the introduction.

**P24 — A private surface**
- **Triggers:** audience-facing material (speech, a slide, a customer line) that relies on something said to exist only in private notes, a facilitator's instructions or an uninspected link.
- **P24.a** — Is the needed explanation on a surface the audience receives? Quote it.

**P25 — An agreement, decision, reason or earlier event that is referred to**
- **Triggers:** as agreed, as discussed, given X's decision, for the usual reason, again, as before, as planned.
- **P25.a** — What was agreed, decided or given as the reason? Quote its content.

*P23 (explanation after the point) is not a separate question. It is the LATER answer to any question above.*

---

**Count.** 26 named patterns, plus one added time slot, give 42 questions. A question is asked only where its trigger appears.
