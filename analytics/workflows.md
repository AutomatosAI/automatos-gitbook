---
description: Recipe and workflow execution analytics.
---

# Workflow Analytics

The Workflows tab tracks recipe execution performance.

<!-- IMAGE: Workflow Analytics showing execution history and duration charts -->

## Key metrics

| Metric | Description |
| --- | --- |
| **Total Runs** | Number of recipe executions |
| **Completion Rate** | Percentage that finished all steps |
| **Avg Duration** | Mean end-to-end execution time |
| **Failure Rate** | Percentage of failed executions |

## Execution history

A table of recent recipe runs:
- Recipe name
- Start time and duration
- Status (completed, failed, in-progress)
- Step progress (e.g., 4/5 steps completed)
- Triggering method (manual, scheduled, chat)

## Step-level analysis

Drill into a specific run to see:
- Time spent on each step
- Which agent handled each step
- Token usage per step
- Error details for failed steps

## Trends

- **Executions over time** — line chart
- **Duration trends** — are recipes getting faster or slower?
- **Failure patterns** — which steps fail most often?

{% hint style="info" %}
Consistently failing steps usually indicate a tool connection issue or an agent that needs a better prompt. Check [Activity → Feed](../activity/feed.md) for error details.
{% endhint %}
