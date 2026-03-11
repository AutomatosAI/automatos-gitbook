---
description: The per-agent detail panel with performance, plugins, and reports.
---

# Agent Details

Click any agent card on the roster to open the Agent Details panel. This is a slide-over modal with everything about a specific agent.

<!-- IMAGE: Agent Details panel showing Overview tab with stats and configuration -->

## Tabs

{% tabs %}
{% tab title="Overview" %}
Summary view showing:
- Agent name, category, model, and status
- Creation date and last active timestamp
- System prompt preview
- Assigned tools and skills list
- Quick edit buttons

<!-- IMAGE: Agent Details Overview tab -->
{% endtab %}

{% tab title="Performance" %}
Metrics for this specific agent:
- **Success rate** — percentage of tasks completed without errors
- **Avg response time** — how long the agent takes to respond
- **Tasks completed** — total count with trend over time
- **Token usage** — input/output tokens consumed
- Performance chart over time

<!-- IMAGE: Agent Performance tab with charts and metrics -->
{% endtab %}

{% tab title="Workload" %}
Current and recent workload:
- Active tasks in progress
- Queue depth
- Recent task history with status indicators
- Resource utilisation

<!-- IMAGE: Agent Workload tab showing active tasks -->
{% endtab %}

{% tab title="Plugins" %}
Manage plugins, skills, and tools assigned to this agent:
- View installed plugins with version info
- Add or remove plugins from the marketplace
- Configure plugin-specific settings
- View skill repositories linked to this agent

<!-- IMAGE: Agent Plugins tab showing installed plugins -->
{% endtab %}

{% tab title="Reports" %}
Agent standup reports and output:
- Latest report with timestamp
- Report history with date navigation
- Grade/rating system for report quality
- Linked files and artifacts

Reports are generated automatically when agents complete scheduled tasks, or manually via the `platform_submit_report` tool.

<!-- IMAGE: Agent Reports tab showing a standup report -->
{% endtab %}
{% endtabs %}

## Editing an agent

From the Overview tab, click **Edit** to modify:
- Name, description, and category
- Model and temperature settings
- System prompt
- Persona
- Tool assignments

Changes take effect immediately — no restart required.

{% hint style="warning" %}
Changing an agent's model may affect its behaviour and cost. Test after switching.
{% endhint %}
