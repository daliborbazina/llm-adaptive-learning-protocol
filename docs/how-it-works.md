# How it works

This repository contains a prompt for repeated German grammar and writing practice from A1 to B1.

The basic idea is simple:

```text
test
-> user answers
-> correction
-> specific mistakes are recorded
-> unresolved mistakes return
-> corrected areas are checked again later
-> next test
```

## First test

The user copies the complete prompt from:

```text
prompt/german-a1-b1.md
```

into a new chat with a language model and sends:

```text
NOVI INICIJALNI TEST
```

This starts a new test without using previous test history.

## After the user answers

The language model is instructed to:

1. correct the test;
2. calculate the score;
3. identify which parts were correct, wrong, or unanswered;
4. record specific mistakes;
5. include unresolved mistakes in the next test;
6. plan later checks for corrected areas;
7. create the next test.

The user normally stays in the same chat so the previous test and recorded state remain available.

## Specific mistakes instead of whole topics

The prompt tries to avoid treating a whole grammar topic as unknown because of one small mistake.

Example:

```text
die Zeitung / Zeitungen
```

contains two separate things that can be checked:

```text
article: die
plural: Zeitungen
```

If the article is correct and the plural is wrong, only the plural should be treated as the unresolved mistake.

Another example:

```text
Ich helfe er.
```

The relevant problem is:

```text
er -> ihm
```

The prompt should not conclude that the user does not know the whole dative case.

## Immediate repetition

A wrong or unanswered item should be checked again in the next test.

The new item can use a different sentence as long as it checks the same problem.

A correct part of the previous item should not be repeated only because another part was wrong.

## Later checks

A correct answer in the next test only shows that the immediate correction worked.

The prompt therefore asks for the same area to be checked again later, roughly after:

```text
+3 days
+7 days
+14 days
+30 days
```

These checks should use new examples where possible.

## Different contexts

Later checks can become less direct.

For example:

```text
direct form
-> new controlled sentence
-> sentence that combines several known rules
-> open writing where the same grammar appears naturally
```

The purpose is to avoid treating memorisation of one sentence as proof that the grammar is known.

## When an old mistake returns

If an area that had previously been considered stable becomes wrong again, the prompt records that it needs attention again.

## New material still appears

The tests are not supposed to contain only old mistakes.

The prompt gives priority to unresolved mistakes and scheduled checks, but it also keeps adding A1–B1 material so that new gaps can still be found.

## Test format

The current format contains:

```text
14 tasks
266 total points
maximum level: B1
```

The tasks cover areas such as:

- articles and plurals;
- adjectives;
- present tense;
- perfect tense;
- possessive articles;
- personal pronouns;
- prepositions and cases;
- sentence order;
- connectors and subordinate clauses;
- tense, mood and passive;
- error correction;
- case recognition;
- picture description;
- vocabulary and paraphrasing.

## Important limitation

All of these rules are written inside the prompt.

There is no separate program enforcing them.

The language model can apply a rule incorrectly, forget earlier context, misread an answer, or produce an inconsistent test.

See `limitations.md` for the full list of limitations.
