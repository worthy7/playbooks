# Software Delivery Coach plugin

Harness-agnostic software delivery playbooks and Agent Skills, packaged as an Agent Plugins 1.0 plugin. The **Software Delivery Coach** is a portable skill; an optional Copilot agent adapter exposes the same workflow as a specialist agent.

## Contents

- [`skills/software-delivery-coach/SKILL.md`](skills/software-delivery-coach/SKILL.md) — the portable coach and workflow router.
- `skills/` — on-demand skills for discovery, event storming, architecture, quality engineering, and incremental delivery.
- [`com.github.copilot/agents/software-delivery-coach.agent.md`](com.github.copilot/agents/software-delivery-coach.agent.md) — an optional Copilot adapter, not the source of the delivery guidance.
- [`Software-develiery.md`](Software-develiery.md) — the full software delivery reference.
- [`EVENT_STORMING_PLAYBOOK.md`](EVENT_STORMING_PLAYBOOK.md) — the detailed event-storming reference.

The skills are concise working procedures; the two original playbooks remain the detailed source material. The main agent can apply the coach skill directly without switching agents or supporting subagents. Automatic discovery, invocation, and delegation depend on the host; installation does not guarantee that every general chat will invoke the coach.

## Compatibility and installation

### Other agent harnesses

- **Agent Plugins 1.0 clients:** install the repository using the client's plugin installation mechanism. The root `plugin.json` and `skills/<name>/SKILL.md` layout follow the portable standard. Clients that do not implement the `com.github.copilot` namespace can ignore that optional adapter.
- **Agent Skills clients without plugin support:** clone this repository and configure the host to discover its `skills/` directory, where supported. Preserve the complete checkout: skills link to sibling workflows and the full playbooks at the repository root. Copying an individual skill directory alone does not include those dependencies.
- **Other clients:** provide the relevant playbook as reference material. There is no universal installation command or custom-agent format across all harnesses.

Only Copilot CLI installation has been verified here; other clients must support the relevant standard and their discovery and file-access rules may differ.

For automatic use, expose the skills to the main agent through the host's discovery mechanism. If routing needs to be explicit, add a host-appropriate user instruction such as: "Use the software-delivery-coach skill for substantial feature planning, requirements clarification, and architectural decisions; skip it for routine edits."

### Copilot

The optional custom agent is in `com.github.copilot/agents/`, the Copilot-specific component location. All delivery workflows remain in the portable skills.

Copilot surfaces differ in how plugins are added, enabled, and scoped. For a persistent Copilot CLI install, use the included marketplace catalog:

```sh
copilot plugin marketplace add worthy7/playbooks
copilot plugin install software-delivery-coach@playbooks
```

To update an existing installation:

```sh
copilot plugin marketplace update playbooks
copilot plugin update software-delivery-coach@playbooks
```

For local development, register a local checkout with `copilot plugin marketplace add .`, or load it without installing with `copilot --plugin-dir .`. In VS Code, add or install the plugin through the Agent Plugins/customizations UI for the desired user or workspace scope.

Follow the selected Copilot surface's current instructions; marketplace registration, plugin installation, and user-level enablement are separate steps.
