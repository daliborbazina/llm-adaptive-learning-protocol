# Rules

This file is a short summary of the main rules in `../prompt/german-a1-b1.md`.

The prompt file contains the complete instructions and takes precedence over this summary.

## Test structure

Each test must contain:

```text
14 tasks
266 total points
maximum CEFR level: B1
```

Each task should show its relevant CEFR level or range.

## Previous test required

A new follow-up test should not be created until the previous test has been answered and checked.

The reset command is:

```text
NOVI INICIJALNI TEST
```

A normal request for "another test" is not a reset.

## Track the smallest useful mistake

A visible test item can contain more than one independently checkable part.

Example:

```text
die Zeitung / Zeitungen
```

should be treated as:

```text
article = die
plural = Zeitungen
```

If only one part is wrong, the prompt should not automatically mark both parts as wrong.

## Wrong or unanswered items

A wrong or unanswered target must be checked again in the next test.

The next check should:

- test the same problem;
- be direct enough to confirm the correction;
- avoid re-testing unrelated parts that were already correct.

## Correct items

A correct target from the immediately previous test should not return as mandatory repetition only because another target in the same question was wrong.

It may still appear later for normal review, integration, or maintenance.

## Correction is not the same as long-term retention

If the user answers the immediate follow-up correctly, the concrete error is considered corrected.

That does not mean the whole grammar area is considered stable.

Later checks are still required.

## Later review intervals

The prompt uses approximate review points after a successful immediate correction:

```text
+3 days
+7 days
+14 days
+30 days
```

The intervals are calculated from the date of the successful immediate correction.

## Use new examples

Later checks should normally use a new sentence or context.

A cosmetic rewrite of the same sentence is not enough.

## Levels of checking

The prompt can check the same area in several ways:

```text
1. direct form
2. new controlled context
3. integration with other known grammar
4. open production
```

Not every grammar item needs all four forms immediately.

## Recorded states

The prompt uses these status names:

```text
ACTIVE
STABILIZATION
STABLE
MAINTENANCE
REGRESSION
```

In plain terms:

- `ACTIVE` — a current unresolved problem exists;
- `STABILIZATION` — the immediate correction worked, but more checks are needed;
- `STABLE` — repeated evidence suggests the area is currently reliable;
- `MAINTENANCE` — only occasional checking is needed;
- `REGRESSION` — a previously stable area became a problem again.

These states are text maintained by the language model. They are not enforced by program code.

stateDiagram-v2
[*] --> ACTIVE

    ACTIVE --> STABILIZATION: immediate correction passed
    STABILIZATION --> STABLE: later checks passed
    STABLE --> MAINTENANCE: no current problem
    STABLE --> REGRESSION: new relevant error
    MAINTENANCE --> REGRESSION: new relevant error
    REGRESSION --> STABILIZATION: correction passed


## Priority when creating the next test

The prompt uses this order:

1. unresolved mistakes from the previous test;
2. review checks that are due;
3. checks in new contexts;
4. previously stable areas that showed a new problem;
5. new A1–B1 material;
6. occasional review of stable material.

## Do not reduce the whole test to weak areas

Old mistakes have priority, but the test should still contain other material.

Otherwise the system would stop finding new gaps.

## New B1 grammar

The prompt can gradually introduce B1 areas including:

- adjective declension;
- relative clauses;
- Konjunktiv II;
- verbs with prepositions;
- da-/wo-words;
- reflexive verbs;
- infinitive with `zu`;
- `um ... zu`;
- `damit`;
- indirect questions;
- additional subordinate clauses;
- passive;
- Futur I;
- Präteritum of common verbs and modal verbs;
- basic genitive.

New B1 grammar should be introduced gradually rather than all at once.

## Vocabulary difficulty

When a new grammar point is being tested, vocabulary should normally remain familiar and no harder than necessary.

A question should not become difficult only because it contains rare vocabulary.

## Content selection

The current prompt aims roughly for:

```text
75% course / textbook / TELC-relevant A1–B1 material
25% practical everyday situations in Germany
```

This is a guideline for the whole test, not an exact percentage for every task.

## Open answers

A valid alternative answer should be accepted if it:

- is grammatically correct;
- keeps the required meaning;
- follows the task;
- demonstrates the target knowledge.

The prompt should not reject a correct sentence only because it differs from one expected answer.

## Scoring and mistake tracking are separate

A mistake can affect:

1. the score;
2. what should be checked again later.

These are not the same thing.

One underlying mistake should not automatically be counted several times only because it causes several visible problems.

## Repetition limit

Outside mandatory repetition, the same grammar area should normally not be deliberately tested several times in one test without a reason.

## Picture task

The picture-description task should use a real or photorealistic scene when image support is available.

If no image can be provided, the task should remain present and clearly state that an image is required.

## Output after correction

After checking a completed test, the prompt asks for:

- total score;
- score by task;
- mistake analysis;
- short explanations where useful;
- list of areas checked;
- unresolved items;
- updated state;
- updated recent-item list;
- the next test unless the user explicitly asks not to create it.

## Output after test generation

The generated test should include:

- all 14 tasks;
- answer key;
- 266 maximum points;
- test number;
- date when known;
- a format that can be copied, saved, or printed.
