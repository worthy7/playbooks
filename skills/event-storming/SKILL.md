---
name: event-storming
description: Use to facilitate or prepare an event-storming session, clarify a complex business process, surface domain risks, or map workshop findings to implementation slices.
---

# Event storming

Use this framework-agnostic sequence with domain experts. Adapt the timebox and depth to the decision being made.

1. **Set scope:** agree the business outcome, start/end points, timebox, participants, and decisions expected.
2. **Capture events first:** write past-tense facts on a timeline. Merge duplicates without losing alternate flows.
3. **Add commands and actors:** identify what triggered each event and who or what issued the command.
4. **Add policies and rules:** capture conditional reactions, retries, service-level expectations, and compliance constraints.
5. **Mark hotspots:** record uncertainty, disagreement, data quality, integration, performance, and regulatory risks as explicit follow-ups.
6. **Explore consistency:** group commands and events around the invariants that must hold together; keep candidate aggregates small.
7. **Identify context boundaries:** cluster language and behavior, assign ownership, and note the relationships and contracts between contexts.
8. **Map findings to delivery:** identify use cases, read needs, external adapters, risks, and a small set of prioritized, testable implementation slices.

Keep the timeline business-led: do not jump to tables, services, or aggregates before the events and rules are understood. Treat the resulting model as a first-cut shared understanding, not a final architecture. Leave with unresolved hotspots, owners, and next actions visible.

For facilitation details, notation, DDD mapping, and workshop templates, see [`EVENT_STORMING_PLAYBOOK.md`](../../EVENT_STORMING_PLAYBOOK.md).
