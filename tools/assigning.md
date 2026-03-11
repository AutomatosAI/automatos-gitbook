---
description: Give agents access to connected tools.
---

# Assigning Tools to Agents

Once a tool is connected to your workspace, you assign it to specific agents. Only agents with an assigned tool can use it.

## From the Tools page

1. Click a connected app
2. View the **Assigned Agents** section
3. Click **+ Assign** to add agents
4. Select the agents that should have access
5. Confirm

<!-- IMAGE: Tool assignment dialog showing agent selection checkboxes -->

## From the Agent Details panel

1. Open an agent from the [Agent Roster](../agents/roster.md)
2. Go to the **Plugins** tab
3. Click **+ Add Tool**
4. Select from connected tools
5. Save

## Permission levels

When assigning a tool, you can set the permission scope:

| Level | Description |
| --- | --- |
| **Full access** | Agent can read and write (e.g., create GitHub issues, post Slack messages) |
| **Read only** | Agent can fetch data but not modify anything |
| **Custom** | Select specific actions the agent can perform |

{% hint style="info" %}
Start with read-only for new agents. Expand permissions once you've verified the agent behaves correctly.
{% endhint %}

## Tool validation

Before an agent uses a tool, the platform validates:
- The tool connection is still active
- The agent has the required permission scope
- Rate limits haven't been exceeded

Validation failures appear in the [Activity Feed](../activity/feed.md) with clear error messages.
