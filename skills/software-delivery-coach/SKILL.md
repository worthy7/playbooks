---
name: software-delivery-coach
description: Apply the software delivery playbooks to substantial feature planning, requirements clarification, architectural decisions, and delivery risks. Use when asked for delivery coaching or to apply the playbooks; route focused work to the relevant workflow.
---

# Software delivery coach

Help the user apply the packaged playbooks to the project they are actually working in. This workflow does not require a separate agent or agent-to-agent delegation.

## Working approach

- First account for the user's request, repository instructions, existing architecture, conventions, and constraints. Do not assume the project is greenfield or that the playbook's preferred stack or patterns apply.
- Treat the playbooks as guidance, not universal policy. Prefer the project's established practices unless they conflict with the user's requirements, correctness, or safety.
- Choose only the relevant workflow below. Do not force a full lifecycle review onto a narrow code change.
- For unclear business behavior, distinguish confirmed requirements from assumptions and open questions. Do not invent business rules or customer-agreed test data.
- For architecture choices, explain the trade-offs and keep the design proportional to the demonstrated complexity. Do not introduce DDD, CQRS, microservices, or other patterns just because they appear in the playbook.
- When asked to implement, follow the repository's contribution instructions, make focused changes, and validate the requested behavior with the most relevant available checks.
- State important uncertainty and verification limits explicitly.

## Choose a workflow

| Need | Workflow |
| --- | --- |
| Clarify users, requirements, behavior, or acceptance criteria | [Delivery discovery](../delivery-discovery/SKILL.md) |
| Explore a complex business process with domain experts | [Event storming](../event-storming/SKILL.md) |
| Decide boundaries, responsibilities, persistence, or integrations | [Architecture design](../architecture-design/SKILL.md) |
| Select tests or verify a change | [Quality engineering](../quality-engineering/SKILL.md) |
| Slice work or manage release and deployment risks | [Incremental delivery](../incremental-delivery/SKILL.md) |

Use the host's skill-loading mechanism when available; otherwise read the linked workflow directly. Delegation is optional: use another agent only when the host supports it and the task benefits from it. Do not assume a particular tool name, model, or approval mechanism.

## Detailed references

- [Software Delivery Playbook](../../Software-develiery.md)
- [Event Storming Playbook](../../EVENT_STORMING_PLAYBOOK.md)

Resolve links relative to this installed skill, not the user's project. Read relevant sections on demand rather than loading both playbooks for every task. If a workflow or reference is unavailable, state that limitation instead of claiming to have consulted it.
