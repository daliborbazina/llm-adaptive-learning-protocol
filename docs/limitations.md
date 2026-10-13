# Limitations

This project is a prompt, not a language-learning application.

The rules are interpreted and applied by a language model. There is no separate program that guarantees that every rule is followed.

## No scientific validation

This project has not been tested in a controlled study.

It does not prove that:

- users learn German faster;
- users reach B1 faster;
- the review intervals used here are optimal;
- the test structure is better than other study methods;
- the recorded status of a grammar area matches actual language ability.

The rules are practical choices, not validated measurements.

## Not a CEFR assessment

The prompt uses A1, A2 and B1 labels to control the difficulty of exercises.

Those labels do not make the generated tests official CEFR assessments.

A score on one of these tests is not equivalent to a TELC, Goethe, ÖSD or other recognised exam result.

## Not complete B1 preparation

The current prompt focuses mainly on:

- grammar;
- writing;
- repeated practice based on mistakes.

It does not fully cover all skills required for general B1 language ability.

For example, it is not designed as a complete system for:

- listening;
- speaking;
- pronunciation;
- real-time conversation;
- full exam preparation.

## The language model can make mistakes

The model can:

- mark a correct answer as wrong;
- accept a wrong answer;
- misunderstand handwriting or a photo;
- assign the wrong grammar category to an error;
- create an exercise that does not test the intended point;
- forget part of the previous state;
- repeat material unnecessarily;
- ignore a rule from the prompt;
- produce an incorrect explanation;
- produce an incorrect answer key.

The prompt reduces some of these risks by giving explicit rules, but it cannot remove them.

## Long conversations can reduce reliability

The method depends on previous tests, answers, and recorded state being available.

In a long conversation, the model may no longer use all earlier information reliably.

If the user changes to another chat or another model, the relevant state has to be copied manually.

Missing history must not be reconstructed by guessing.

## Different models may behave differently

The same prompt may produce different results with different language models.

Differences can include:

- interpretation of the rules;
- grammar explanations;
- scoring;
- exercise difficulty;
- handling of state;
- output format.

The prompt does not make model behaviour deterministic.

## State is only text

Items such as:

```text
ACTIVE
STABILIZATION
STABLE
MAINTENANCE
REGRESSION
```

are labels maintained in text by the language model.

They are not database records and they are not enforced by program code.

The model can update them incorrectly.

## Review dates are approximate

The prompt uses approximate checks around:

```text
+3 days
+7 days
+14 days
+30 days
```

These intervals are not claimed to be optimal for every learner or every grammar topic.

## Error categories can be ambiguous

One wrong sentence can have more than one possible explanation.

For example, an incorrect pronoun may result from:

- not knowing the pronoun form;
- choosing the wrong case;
- misunderstanding the verb;
- misreading the task;
- a typing mistake.

The language model has to infer the likely reason from the available evidence.

That inference can be wrong.

## Open answers are difficult to score consistently

Writing tasks can have several correct answers.

The prompt tells the model to accept valid alternatives, but evaluation of:

- naturalness;
- coherence;
- vocabulary;
- task fulfilment

can vary between models and between runs.

## Images add another source of error

When answers are submitted as photos, the model can misread:

- handwriting;
- punctuation;
- umlauts;
- crossed-out text;
- overwritten answers;
- page order.

Typed answers are easier to evaluate reliably.

## Generated examples can be unnatural

Even grammatically correct generated sentences can sometimes sound artificial or uncommon.

The prompt explicitly asks for natural examples, but this is not guaranteed.

## It can reinforce a wrong correction

If the model makes an incorrect correction and records it as a learning problem, later tests may repeat that incorrect assumption.

When something looks suspicious, it should be checked against a reliable grammar source, course material, or teacher.

## No teacher replacement

The project can provide additional practice.

It cannot reliably replace a teacher's judgement about:

- why a learner makes a recurring mistake;
- whether a structure is appropriate for the learner's current level;
- pronunciation and speaking;
- communication problems that are not visible in written exercises;
- broader learning strategy.

## No guarantee of continuity

The method works best when:

- the same chat is used;
- previous answers remain available;
- the state is preserved;
- the model follows the prompt consistently.

None of these conditions is guaranteed by the prompt itself.
