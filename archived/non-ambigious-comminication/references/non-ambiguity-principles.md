
# Principles for non-ambiguous communication

## The reader and the required result

Write for the user, who usually knows the direction of the work but may not remember its detailed context. They should be able to identify the things being discussed, understand what they mean and follow their connections without reconstructing earlier conversations.

These principles address the meaning carried by an explanation. Apply them in proportion to the question and the reader's need. The examples below illustrate wording and intended meaning; they do not assert current project facts.

## 1. Make the thing being referred to identifiable

**Principle.** Give important things recognisable names and enough scope to distinguish them from other plausible meanings. A generic noun is sufficient only when its intended referent is clear in the text.

Words such as “the project,” “the evaluation,” “the method,” “the document,” “the questions” and “the row” can refer to several things. The writer's certainty about which one it means does not make the reference available to the reader.

Use the actual name when one exists. Include the system, table, document or project that locates the thing when that distinction is necessary. Searchable names help the reader find it again.

**Examples.**

- “Session token” can mean a token for a StoryOS session or something associated with a Codex session. Name the system whose session is meant.
- “The test plan” may need to become “the test plan for the model evaluation.”
- “Its questions” may need to become “the sample preparation framework's questions.”

Pronouns and short names are useful once their meaning is established nearby. Repeating a full name in every sentence is unnecessary. Reintroduce the name when a topic change or another possible referent makes the shorthand unclear.

**Check.** For each important name, noun or pronoun: which thing does this mean, and where can the reader establish that? Could another thing reasonably fit?

## 2. Explain what an object represents and how it relates to other objects

**Principle.** When understanding depends on an object's role or a relationship, explain it. Naming each object may still leave the relationship missing.

A reader might understand the words “Airtable record” and “n8n workflow” but not know whether they are two names for one thing, separate things, or a representation and the thing represented.

**Example.**

> Airtable's Workflows table stores a record describing each tracked n8n workflow. The workflow runs in n8n; its Airtable record stores information about it. The check determines whether that corresponding record already exists.

This establishes the representation before relying on it. The same need arises when explaining a document and its source, a model and the workflow using it, or a method and an instance of applying it.

Explain the relationship relevant to the present point. Include an identifier, location or direction of a link when the reader needs it to distinguish the objects or understand how they connect.

**Check.** Does the reader know what each important thing represents, and how the things connect in this explanation?

## 3. State the action and its actor concretely

**Principle.** Make clear who or what does something, what the action involves, and what it acts on when those details are needed to understand the sentence.

An actor can be a person, team, application or automated workflow. Use the actual actor. A descriptive sentence can also explain a relationship without forcing a person into it.

Broad verbs such as “start,” “guide,” “support,” “handle” or “prepare” can hide the action. Abstract nouns can do the same. Expand them where the reader would otherwise have to guess.

**Example.**

> The five workflows I'd start with.

This identifies a set while leaving the intended action unclear. If the intended action is enabling execution-log saving, say:

> The five n8n workflows for which I'd enable execution-log saving first.

In another explanation, “the framework guides us” may mean that its questions help someone identify test situations and find records for them. State those activities when “guides” alone does not communicate them.

**Check.** Who or what acts? What happens? What does the action affect? Which of those answers are needed and missing?

## 4. Give purposes, scope and judgment words their intended meaning

**Principle.** Connect words such as “right,” “useful,” “enough,” “ready” and “usable” to the purpose or criterion intended in this explanation.

A sentence can be grammatically complete while leaving its purpose unstated. “The right examples” could mean relevant examples, representative examples or examples whose recorded answers are correct. Those meanings are different.

**Example.**

> Can its questions guide us to the right examples?

If the intended question concerns a framework for preparing a model evaluation, a clearer version is:

> Do the sample preparation framework's questions help us identify the cases we need to test and find the data for those cases?

This names the framework and preserves both activities: identifying cases and finding their data. Where the surrounding explanation has not established the intended data, add a concrete illustration, such as the actual comment, the post it responds to and the relevant guidance.

Likewise:

> Can we obtain enough context to make each example usable?

needs to establish context of what, examples for what, and usable for which task. One possible expansion is:

> For each Freeform comment selected for the model evaluation, can we obtain the post it responds to and the applicable Freeform rules so reviewers can judge the AI's recommended action or reply?

**Check.** Enough for what? Useful to whom and for which purpose? Right according to which intended requirement? Does the explanation supply the answer?

## 5. Restore the prerequisite context for the present point

**Principle.** Include the background the reader needs to understand this answer. Explain the relevant prior event, reason or distinction before relying on it.

The user may remember the broad goal while forgetting why a particular object, example or earlier discussion entered the work. Defining a word alone will not answer a question about that history.

An explanation may need to establish:

- what the current discussion concerns;
- the relevant previous event or question;
- why the particular thing now being mentioned is relevant;
- how that context leads to the present point.

These are possible needs, not compulsory sections. Include only those needed for this answer.

For example, when a particular workflow appears in an explanation of a method, the reader may need to know that it was the example on which the method was tried. The explanation should establish that role before discussing what the example shows.

Prefer a connected account in which each point supplies meaning needed by the next. Explain necessary technical details in familiar terms; removing those details can make the answer harder to understand when they identify the subject or explain the relationship.

**Check.** Which part of the answer would make sense only to someone who remembers the previous conversation? What is the smallest piece of background that makes it understandable here?

## 6. Make the relationships between the parts of an explanation explicit

**Principle.** The reader should be able to follow what question a section answers and how each point contributes to that answer. Make a change of question or level of explanation explicit.

Clear sentences can still form a confusing explanation if their relationship is unstated. A goal, an activity, an observation and a conclusion can belong together, but they play different roles. Name or explain those roles when the reader would otherwise have to infer them.

**Example.**

When explaining an assessment of a sample preparation framework, these questions have different subjects:

- Do the selected records contain the information required for the evaluation?
- Did the framework's questions help us identify that information and find its source?

The first concerns the records. The second concerns the framework's contribution. If both belong in the explanation, show how the observation about the records bears on the question about the framework.

An incomplete set of records may reflect information that was unavailable, even if the framework correctly identified what was needed. A complete set might have been assembled using knowledge outside the framework. The relationship needs explanation before the reader can understand what the example establishes about the framework.

Use bullets for genuinely parallel points. Use connecting sentences to explain causes, qualifications and relationships. A heading should identify the subject and purpose of the section sufficiently for the reader to follow it when skimming.

**Check.** What question is this section answering? What role does each point play? Are the connections stated, or must the reader reconstruct them?

## 7. Preserve necessary meaning when shortening or revising

**Principle.** Retain the words and relationships that make the remaining text understandable. Brevity should reduce reading effort without transferring the missing explanation back to the reader.

Cutting “model evaluation” while retaining “the test plan” may remove the very context needed to identify the plan. Replacing a named set of questions with “six are in the document” preserves a count while losing the subject.

When shortening, remove optional points before stripping necessary explanations from the points that remain. Split a sentence when several relationships need explaining. Concise wording and pronouns are appropriate where the text already makes their meaning clear.

When revising, preserve clarifications already established for the text. Check the revised answer itself; a clarification in a separate chat reply does not repair a document that still contains the ambiguous wording.

**Check.** Have the referents, actions, purposes and necessary relationships survived the edit? Can the intended reader still understand the remaining points without the earlier version?

## 8. Make missing knowledge explicit when it prevents clarification

**Principle.** Restore meaning from information that is available. If a necessary referent, relationship or reason is unknown, identify the missing information instead of supplying a plausible invention.

For example, if the available text says only “the table” and does not establish which table is meant, acknowledge that specific uncertainty. Adding a guessed table name would make the sentence appear more precise while changing its meaning.

A necessary question should identify the information that cannot be established from the available context. Use what is already known to clarify the rest of the explanation.

**Check.** Did the revision make an established meaning explicit, or did it invent the missing meaning?

## Review before returning the text

Read the answer from the position of someone who knows the direction but may not remember the detailed conversation.

1. **Identify the subject.** Can the reader tell which things the important words refer to?
2. **Follow the meaning.** Are the necessary roles, actions, purposes and relationships explained?
3. **Recover the context from this answer.** Is the background needed for the present point included where the reader needs it?
4. **Follow the connections.** Does each section answer an identifiable question, with its points connected clearly?
5. **Check the revision.** Has the intended meaning survived, including any uncertainty that remains?

Challenge unclear wording with “which?”, “of what?”, “for what?”, “who or what does it?” and “how does this relate?”. Add the answers necessary to understand the present point. Stop when that meaning is accessible; further questions being imaginable does not make every detail necessary.

