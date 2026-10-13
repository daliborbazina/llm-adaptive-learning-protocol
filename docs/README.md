# Documentation

This directory explains the prompt without repeating the full prompt text.

## Files

### `how-it-works.md`

Explains the normal test cycle:

```text
test
-> answers
-> correction
-> mistake tracking
-> later checks
-> next test
```

### `rules.md`

Lists the main rules used by the prompt, including:

- 14 tasks;
- 266 total points;
- maximum level B1;
- specific mistakes are tracked separately where possible;
- unresolved mistakes return in the next test;
- corrected areas are checked again later;
- later checks should use new examples;
- correct answers should not be repeated without a reason.

### `limitations.md`

Explains what the project does not claim and where the approach can fail.

This file is important because the rules are executed by a language model rather than by deterministic program code.

## Scope

The documentation describes the intended behaviour of the prompt.

If the documentation and the current prompt differ, the prompt file in `../prompt/` is the version that is actually used.
