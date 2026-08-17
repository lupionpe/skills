---
name: ponytail-review
description: Review a code change for removable complexity.
disable-model-invocation: true
---

Review the requested diff for the smallest boring solution that preserves required behavior.

1. Inspect the diff and enough surrounding code to understand every changed path.
2. Account for every added concept: abstraction, dependency, configuration point, helper, layer, or duplicated implementation.
3. Prefer deletion, existing code, standard-library or native capabilities, then direct code.
4. Report only concrete simplifications whose replacements preserve behavior, safety, accessibility, performance requirements, and proportionate tests. Do not apply them.

Format each finding:

`<file>:L<line> — <what to remove> → <replacement>; <evidence it is sufficient>.`

Order findings by impact. If none remain, say `Lean already. Ship.`
