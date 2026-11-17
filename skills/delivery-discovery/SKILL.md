---
name: delivery-discovery
description: Use when a feature's users, business behavior, requirements, or acceptance criteria need clarification before implementation.
---

# Delivery discovery

Use this workflow to turn a request into an agreed, testable description of behavior. Adapt it to the project's scale and the time available; do not treat every activity as mandatory for a small, well-understood change.

1. Establish the desired outcome, actors, scope, constraints, and what decision or deliverable is needed.
2. Use the project's domain language. Identify terms with conflicting meanings and keep unresolved questions visible.
3. Describe the important user workflows, including reads/lists, alternate paths, failure behavior, and relevant non-functional requirements.
4. For complex or disputed processes, use the `event-storming` skill before settling on a design.
5. Write business-readable scenarios for the required behaviors. Separate the general behavior pattern from concrete examples and values that need domain-expert confirmation.
6. Trace implementation and verification back to the agreed behavior. Mark assumptions, risks, and open questions; do not present a draft as validated requirements.

Do not silently guess business thresholds, permissions, error outcomes, or acceptance-test data. Ask for clarification when those details materially affect correctness; otherwise record the assumption and its impact.

For the detailed source guidance, see the discovery and acceptance-test sections of [`Software-develiery.md`](../../Software-develiery.md).
