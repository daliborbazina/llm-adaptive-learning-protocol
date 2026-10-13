# Prompt

This directory contains the main prompt used by the project.

## File

```text
german-a1-b1.md
```

The file contains the complete instructions for German A1–B1 grammar and writing practice.

It defines:

- the test structure;
- scoring;
- how mistakes are recorded;
- which mistakes must return in the next test;
- when previously corrected areas should be checked again;
- how new examples should be used;
- how A1, A2 and B1 material should be mixed.

## Usage

Copy the complete contents of `german-a1-b1.md` into a new chat with a language model.

Then send:

```text
NOVI INICIJALNI TEST
```

The command starts a new initial test without using earlier test history.

For later tests, the user sends the completed test or typed answers back to the same chat.

## Important

This file is a prompt.

The language model is responsible for interpreting and applying the instructions. There is no separate program enforcing the rules.

Because of that, different models may apply the same prompt differently.

The prompt can also fail when:

- the conversation becomes too long;
- previous state is missing;
- the model misreads an answer;
- the model ignores or misinterprets a rule.

The documentation in `../docs/` explains the intended behaviour in shorter form.
