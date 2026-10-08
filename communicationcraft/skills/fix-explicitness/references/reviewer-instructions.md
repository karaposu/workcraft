
# Reviewer instructions

You work alone, in this one session. No subagents, no delegation, and do not invoke any skill. Open only the files named in your task message:
- **ORIGINAL:** the text before fixing;
- **COPY:** the text after fixing;
- **DIFF:** the changes;
- **TABLE:** the missing-meanings table, one JSON row per particular;
- **TRACE:** words a script could not trace to a basis;
- **OUT:** where to write your review.

You did not make these edits. Your job is to check them once, independently. You are not re-detecting the text: check only the changed passages, the hunks in DIFF.

**Background.** Each edit supplies a particular the text was missing (which one, who, of what, by what criterion, and so on). An edit is allowed only when the particular is established by the text itself, by a basis file quoted in TABLE, or by an author answer recorded in TABLE. Each table row gives:
- the canonical `wording` for first use;
- the `short` form for later mentions;
- the `basis` quote.

## For each changed passage, check

1. **Invented particular** (`must-fix`). The new words add a fact, name, number, actor, criterion or scope that the cited rows' `wording` / `basis` and ORIGINAL do not contain.
   - Use TRACE as leads, but judge yourself: an inflection or a function word is not an invention.
2. **Dropped or changed meaning** (`must-fix`). The edit removed or altered something ORIGINAL said: a fact, a hedge, a commitment, a condition, a number.
3. **Broken reference** (`must-fix`). The edit breaks a pronoun, a "this/that/the above", a list numbering or a cross-reference that worked before.
4. **Inconsistent naming** (`must-fix`). The same particular appears under different wording in different edits, or deviates from its row's `wording` / `short`.
   - Also: an introduction appears twice, or a later mention uses the short form before any introduction.
5. **Broken format** (`must-fix`). Markdown, table pipes, quotes or code damaged.
6. **Leaked note** (`must-fix`). Editorial text, a question to the author, or row ids in the text.
7. **Readability** (`advisory`). The edit is clumsy: a doubled word, a garbled clause, a very long insertion. Advisory only. Do not ask for style changes beyond what makes the sentence read correctly.

Do not report gaps that the edits did not touch, and do not judge whether a declined or asked row should have been fixed. That is not your role.

## Write OUT

Write a markdown table with columns:

| # | line in COPY | check (1–7) | must-fix / advisory | what is wrong | minimal repair (revert, or exact replacement words) |
|---|---|---|---|---|---|

Under it, give:
- the number of changed passages reviewed;
- the number of findings by check.

Reply with only those counts and OUT's path.



