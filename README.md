# Software Delivery Coach plugin

This repository is packaged as an Agent Plugins 1.0 plugin. It provides a Copilot-specific **Software Delivery Coach** agent and portable skills for focused delivery workflows.

## Contents

- `com.github.copilot/agents/software-delivery-coach.agent.md` — the project-aware coach and workflow router.
- `skills/` — on-demand skills for discovery, event storming, architecture, quality engineering, and incremental delivery.
- [`Software-develiery.md`](Software-develiery.md) — the full software delivery reference.
- [`EVENT_STORMING_PLAYBOOK.md`](EVENT_STORMING_PLAYBOOK.md) — the detailed event-storming reference.

The skills are concise working procedures; the two original playbooks remain the detailed source material. The coach is available for explicit use or host-supported agent routing. Installing the plugin does not guarantee that every general chat will automatically invoke it.

## Compatibility and installation

The root `plugin.json` uses the portable Agent Plugins 1.0 manifest. Skills use the standard `skills/<name>/SKILL.md` location. The custom coach agent is in `com.github.copilot/agents/`, the Copilot-specific component location.

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
