---
name: ponytail-review
description: Find removable complexity in a code change before code-review.
disable-model-invocation: true
---

Find the **simplest sufficient** implementation. This is a read-only simplification pass before code-review; report recommendations without applying them.

1. **Pin scope.** Establish the requested base and target, including staged, unstaged, or untracked changes when requested. Ask if ambiguous. Verify refs and record the exact comparison; stop if empty.
2. **Ground the review.** Read the originating request/spec and applicable repository standards. Trace changed paths, affected callers, and relevant tests. State missing evidence; absence of a spec is not proof that behavior is unnecessary.
3. **Account for complexity.** Examine every added or modified abstraction, dependency, configuration point, helper, layer, and duplicated implementation. Seek the first sufficient option: deletion, existing code, standard library, native platform capability, installed dependency, direct code. Speculative generality, middlemen, and duplication are leads to investigate, not automatic findings; one caller alone proves nothing.
4. **Prove the cut.** Report a simplification only when a concrete replacement preserves required behavior, safety, accessibility, operational constraints, and proportionate tests. Cite the requirement or code evidence supporting it. Repository standards constrain the replacement. Prefer fewer concepts and less maintenance over fewer lines; retain complexity that earns its place.

Order findings by maintenance impact:

`<file>:L<line> — <remove> → <replacement>; <supporting evidence>; check: <smallest useful verification>.`

Finish when every changed concept is accounted for and each finding meets that evidence bar. State review limitations and hand off to code-review for its Standards and Spec passes. If no findings: “No supported simplifications found. Next: code-review.”
