---
description: Manage how agents work together as teams.
---

# Coordination

The Coordination tab manages multi-agent collaboration — how agents communicate, delegate tasks, and work together.

<!-- IMAGE: Coordination tab showing agent team assignments -->

## Team assignments

Group agents into teams for coordinated workflows. A team is a logical grouping where agents can:
- Hand off tasks to each other
- Share context within a workflow
- Report to a designated lead agent

## Delegation rules

Configure how agents can delegate work:

| Rule | Description |
| --- | --- |
| **Auto-delegate** | Agents can pass tasks to teammates automatically |
| **Approval required** | Delegation requires user confirmation |
| **Disabled** | Agents work independently only |

## Inter-agent communication

When agents work together on a recipe or mission:
- Each agent sees the output of previous steps
- Context is passed through the workflow pipeline
- Results are aggregated in the Activity feed

{% hint style="info" %}
Coordination settings are most useful when running [Recipes](recipes.md) that chain multiple agents together.
{% endhint %}
