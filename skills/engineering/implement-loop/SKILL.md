---
name: implement-loop
description: Implement a parent spec through serial ticket delegation, independent review, and ticket updates.
disable-model-invocation: true
---

# Implement tickets

Implement every ticket in the supplied parent spec, serially in blocking order. As lead agent, own independent reviews, required checks, and ticket updates.

1. For each next unblocked ticket, record its starting commit and give it to a dedicated sub-agent using $mattpocock-skills:implement as its review baseline. Scope the agent to that ticket; have it read the parent spec and ticket before coding.
2. After each sub-agent finishes, update the ticket with its commit and progress. Independently use $mattpocock-skills:code-review against the ticket’s starting commit, supplying the ticket and parent spec. Run repository-required checks and record review and check results in the ticket.
3. Send actionable findings and check failures to the same sub-agent to fix and commit; repeat step 3 against the unchanged baseline. Mark the ticket complete and advance only when findings are resolved and checks pass.
