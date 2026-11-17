---
name: incremental-delivery
description: Use when breaking a feature into deliverable work, planning implementation order, or considering release and deployment risks.
---

# Incremental delivery

Prefer small, reviewable increments that demonstrate user or operational value.

1. Start from an agreed behavior or operational outcome, not a technical layer.
2. Break the work into thin end-to-end slices that can be tested and demonstrated independently. Make prerequisites and technical enablers explicit as they emerge.
3. For each slice, identify acceptance checks, data/API compatibility, external dependencies, observability, and material risks.
4. Keep changes compatible with the project's release model. Consider migration sequencing, feature flags, rollback or forward-fix options, and deployment ownership when relevant.
5. Use the repository's existing branch, commit, and review practices. Keep changes focused and preserve a releasable mainline where the project expects one.
6. Validate and report each increment; do not claim deployment or production readiness based only on a successful local build.

Do not impose a deployment pipeline or infrastructure pattern without understanding the project's hosting, maturity, and non-functional requirements.

For detailed guidance, see the vertical slices, infrastructure design, and release/deployment sections of [`Software-develiery.md`](../../Software-develiery.md).
