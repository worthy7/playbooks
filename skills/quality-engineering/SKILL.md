---
name: quality-engineering
description: Use when choosing tests, planning quality checks, reviewing a change's verification, or improving the project's testing approach.
---

# Quality engineering

Verify the behavior that matters using the project's existing test and tooling conventions.

1. Identify the behavior or risk being changed and the closest meaningful observable outcome.
2. Inspect existing tests and test commands before adding new test infrastructure.
3. Choose a test level that gives useful confidence at reasonable cost: isolated domain tests for pure rules, integration tests for wired use cases and persistence, and end-to-end/acceptance tests for critical user behavior.
4. Include relevant boundaries and failure paths. Use realistic test data and working fakes when external services need substitutes; preserve the distinction between a fake and a production integration.
5. Run the smallest relevant test set, then expand validation if the change affects shared behavior or broad integration points. Report exactly what passed, failed, or could not be run.
6. Consider additional checks—formatting, linting, security, accessibility, and performance—when the changed behavior makes them relevant.

The playbook prefers implemented fakes and integration-first coverage over interaction-only mocks. Treat that as a preference to evaluate against the project's existing test strategy and the specific boundary being tested, not as a reason to rewrite unrelated tests.

For detailed guidance, see the quality engineering section of [`Software-develiery.md`](../../Software-develiery.md).
