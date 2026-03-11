---
description: Per-agent performance analytics.
---

# Agent Analytics

The Agents tab breaks down performance by individual agent.

<!-- IMAGE: Agent Analytics showing comparison table and performance charts -->

## Agent comparison table

| Column | Description |
| --- | --- |
| **Agent** | Name and category |
| **Tasks** | Total tasks completed |
| **Success Rate** | Percentage of successful completions |
| **Avg Time** | Mean response time |
| **Tokens** | Total tokens consumed (input + output) |
| **Cost** | Total LLM cost for this agent |

Sort by any column to find your top performers, highest-cost agents, or slowest responders.

## Performance charts

- **Tasks by agent** — bar chart comparing volume
- **Success rate by agent** — ranked comparison
- **Cost by agent** — pie chart of cost distribution

## Agent drill-down

Click any agent row to see:
- Detailed time-series performance
- Task type breakdown
- Error log for failed tasks
- Model usage history

{% hint style="info" %}
Use this tab to identify agents that need model upgrades, prompt tuning, or additional tools.
{% endhint %}
