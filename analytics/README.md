---
description: Performance metrics, cost tracking, and optimisation insights.
---

# Analytics

The Analytics page gives you full visibility into your workspace performance, costs, and optimisation opportunities across seven tabs.

<!-- IMAGE: Analytics page showing Overview tab with performance charts -->

## Page layout

{% tabs %}
{% tab title="Overview" %}
High-level workspace metrics:
- Success rate trend over time
- Total executions
- Average response time
- Token efficiency
- Cost summary

[Full guide →](overview.md)
{% endtab %}

{% tab title="Agents" %}
Per-agent analytics:
- Individual agent performance comparison
- Task volume by agent
- Success rate rankings
- Model usage per agent

[Full guide →](agents.md)
{% endtab %}

{% tab title="Workflows" %}
Playbook and workflow execution analytics:
- Completion rates
- Average duration
- Step-level timing breakdown
- Failure analysis

[Full guide →](workflows.md)
{% endtab %}

{% tab title="Documents" %}
Knowledge base analytics:
- Processing pipeline throughput
- Search query volume and hit rates
- Chunk utilisation
- Storage growth trends

[Full guide →](documents.md)
{% endtab %}

{% tab title="LLM & Costs" %}
Detailed cost tracking:
- Total cost over time
- Cost by model, by agent
- Token usage (input vs. output)
- Cost per request
- Cost projections

[Full guide →](llm-costs.md)
{% endtab %}

{% tab title="Tools & Integrations" %}
Tool usage analytics:
- Most-used tools
- Call volume by integration
- Error rates per tool
- Latency distribution

[Full guide →](tools.md)
{% endtab %}
{% endtabs %}

## Time range selector

All analytics tabs support time range filtering:
- **My Workspace** — scope to your workspace
- **30 Days** / **7 Days** / **24 Hours** — time windows
- **Refresh** — reload data

<!-- IMAGE: Time range selector showing workspace scope and date range options -->

{% hint style="info" %}
Analytics data refreshes periodically. Click **Refresh** for the latest numbers.
{% endhint %}

## Enhanced real-time analytics

The analytics dashboard includes advanced metrics updated in real-time:

| Metric | Description |
| --- | --- |
| **System load trend** | 24-hour system utilisation with colour coding (green/yellow/red) |
| **Cost per execution** | Calculated from actual LLM usage data, not estimates |
| **Predictive capacity alerts** | Early warnings when you're approaching resource limits |
| **Resource bottleneck detection** | Identifies which component is slowing things down, with recommendations |

These metrics are available on the Overview tab and refresh automatically.
