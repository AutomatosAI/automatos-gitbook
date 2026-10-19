---
description: Create, configure, and manage your AI workforce.
---

# Agents

The Agent Management page is where you build and manage your AI workforce. Each agent is a specialised AI worker with its own model, persona, tools, and skills.

<!-- IMAGE: Agent Management page showing roster with agent cards and stats bar -->

## Page layout

The Agent Management page has four main tabs:

{% tabs %}
{% tab title="Agent Roster" %}
Your agent directory. Browse all agents as cards, filter by status (Active / Idle), search by name or capability. Each card shows:
- Agent name, category, and model
- Success rate percentage
- Tasks completed and capabilities count
- Status indicator (online/offline)

[Full guide →](roster.md)
{% endtab %}

{% tab title="Configuration" %}
Global agent settings — default models, shared prompts, and system-wide configuration that applies across agents.

[Full guide →](configuration.md)
{% endtab %}

{% tab title="Coordination" %}
Manage how agents work together — team assignments, delegation rules, and inter-agent communication settings.

[Full guide →](coordination.md)
{% endtab %}

{% tab title="Playbooks" %}
Multi-step workflows that chain agents together. Create, edit, and manage playbooks that coordinate multiple agents to complete complex tasks.

[Full guide →](playbooks.md)
{% endtab %}
{% endtabs %}

## Stats bar

At the top of the page, four metric cards give you an at-a-glance view:

| Metric | What it shows |
| --- | --- |
| **Total Agents** | Number of agents in your workspace |
| **Active Agents** | Agents currently online and processing |
| **Categories** | How many distinct agent types you have |
| **Avg Performance** | Aggregate success rate across all agents |

## Quick start: Create your first agent

1. Click **+ Create Agent** in the top right
2. Pick a category and give the agent a name
3. Choose a predefined persona (for example the Code Reviewer or Content Strategist persona), write your own, or skip it
4. Select a model, then add tools and capabilities
5. Click **Create Agent**

Your agent appears on the roster immediately and is ready to receive messages. See [Creating an Agent](creating.md) for each step.

### Agents on day one

- **Hosted Studio:** a new hosted workspace starts with Auto and a Brand Designer. Auto builds the rest of your team during onboarding, from a package or from scratch.
- **Local edition:** a fresh local install starts with five agents: Auto, a Brand Designer and a starter team of Researcher, Writer and Analyst.

The Studio marketplace has 100+ ready-made agents you can install. See [Marketplace Agents](../marketplace/agents.md).

{% hint style="success" %}
Start from a predefined persona or a marketplace agent. You can always customise the agent later from the [Agent Details](details.md) panel.
{% endhint %}

## Subpages

| Page | Description |
| --- | --- |
| [Agent Roster](roster.md) | Browsing, filtering, and managing your agents |
| [Creating an Agent](creating.md) | Step-by-step agent creation guide |
| [Agent Details](details.md) | The per-agent detail panel (Overview, Performance, Plugins, Reports) |
| [Configuration](configuration.md) | Global agent configuration |
| [Coordination](coordination.md) | Multi-agent teamwork settings |
| [Playbooks](playbooks.md) | Creating and managing multi-step workflows |
