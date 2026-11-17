---
name: architecture-design
description: Use when a feature or system change requires domain modeling, boundaries, integration design, persistence choices, or an architectural decision.
---

# Architecture design

Start with the behavior and constraints, then choose the smallest architecture that supports them.

1. Inspect the existing system boundaries, dependency directions, persistence, integrations, and conventions before proposing a new design.
2. Use agreed scenarios and non-functional requirements to identify responsibilities, invariants, read needs, external dependencies, and operational constraints.
3. Apply domain modeling where business rules and language warrant it. Define terms and candidate boundaries with domain experts; do not introduce tactical DDD patterns where simple code is sufficient.
4. Keep business behavior independent of infrastructure where practical. Define explicit application/use-case responsibilities and adapters for external systems when they provide useful boundaries.
5. Make transaction, consistency, idempotency, authorization, tenant isolation, and failure/retry behavior explicit when relevant.
6. Compare viable options by complexity, reliability, changeability, and fit with the current project. Record significant decisions and assumptions.

Do not default to microservices, CQRS, event sourcing, or a particular framework. Explain why a pattern is needed in this project and what it costs.

For detailed guidance, see the strategic domain modeling and architecture design sections of [`Software-develiery.md`](../../Software-develiery.md).
