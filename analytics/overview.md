---
description: High-level workspace performance summary.
---

# Overview

The Overview tab shows aggregate metrics for your entire workspace.

<!-- IMAGE: Analytics Overview with key metric cards and trend charts -->

## Key metrics

| Metric | Description |
| --- | --- |
| **Total Executions** | Total number of agent tasks completed |
| **Success Rate** | Percentage of tasks completed without errors |
| **Avg Response Time** | Mean time from request to response |
| **Token Efficiency** | Ratio of useful output to total tokens consumed |
| **Cost (period)** | Total LLM spend for the selected time range |

## Trend charts

- **Success rate over time** — line chart showing daily/weekly trends
- **Execution volume** — bar chart of tasks per day
- **Response time distribution** — histogram of latencies

## Quick insights

The overview surfaces actionable insights:
- Agents with declining performance
- Unusual cost spikes
- Low-utilisation agents (consider reassigning or removing)
- High-error tool connections

{% hint style="info" %}
Click any metric card to drill down into the relevant tab (Agents, Costs, Tools) for detailed analysis.
{% endhint %}
