---
description: Browse and manage all agents in your workspace.
---

# Agent Roster

The Agent Roster is the default view on the Agents page. It shows all agents in your workspace as cards in a grid layout.

<!-- IMAGE: Agent Roster tab showing grid of agent cards with status indicators -->

## Agent cards

Each card displays:

| Field | Description |
| --- | --- |
| **Name** | The agent's display name (e.g., Code Reviewer, Sentinel) |
| **Category** | Agent type — custom, support, code_architect, etc. |
| **Model** | The LLM model this agent uses (shown as a badge) |
| **Success Rate** | Percentage of tasks completed successfully |
| **Tasks Completed** | Total number of tasks this agent has handled |
| **Capabilities** | Tags showing the agent's key skills |
| **Status** | Green dot = online, grey = idle |

<!-- IMAGE: Close-up of a single agent card showing all fields -->

## Filtering and search

### Status filter

Toggle between:
- **Active** — agents currently online and working
- **Idle** — agents that are configured but not actively processing

### Search

Type in the search bar to filter agents by name, type, or capabilities. Search is instant and filters the card grid in real-time.

<!-- IMAGE: Search bar with filter results showing matching agents -->

## Agent actions

Click any agent card to open the [Agent Details](details.md) panel. From there you can:
- View performance metrics and workload
- Edit configuration
- Assign or remove plugins
- Read agent reports

Right-click or use the card menu (three dots) for quick actions:
- **Edit** — modify agent settings
- **Duplicate** — create a copy with the same configuration
- **Delete** — remove the agent from your workspace

{% hint style="warning" %}
Deleting an agent is permanent. Its conversation history and reports are retained, but the agent configuration is removed.
{% endhint %}

## Refresh

Click **Refresh** in the top right to reload agent statuses. This is useful after deploying changes or restarting services.
