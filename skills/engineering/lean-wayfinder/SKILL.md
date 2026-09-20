---
name: lean-wayfinder
description: Use Wayfinder to find the simplest sufficient route to a development goal.
disable-model-invocation: true
---

Use the skill [$mattpocock-skills:wayfinder](/Users/lupion/Documents/_CoS/03-toolkit/agents-configs/_all-skills/mattpocock-skills/skills/engineering/wayfinder/SKILL.md), applying the constraint below while naming the destination, charting the frontier, and resolving decisions.

## Simplest sufficient

Understand the goal and actual code flow first. Then stop at the first sufficient option: no change, existing code, standard library, native platform capability, installed dependency, minimal new code. Judge sufficiency against explicit requirements, correctness, security, accessibility, and operational constraints; prefer maintainable simplicity over line count. For bugs, resolve the root cause across affected callers.

Every proposed abstraction, dependency, or decision ticket must earn its place through a present requirement or uncertainty blocking the destination. Put speculative needs out of scope. When extra complexity is necessary, name the concrete limitation that justifies it and the smallest useful check of the chosen approach.

When creating or adopting a map, add a link to this skill under Notes and require every session, including delegated research, to apply “Simplest sufficient.” Keep Wayfinder’s planning boundaries and completion rules.
