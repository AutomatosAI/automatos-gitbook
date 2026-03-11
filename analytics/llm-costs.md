---
description: Track every dollar spent on LLM API calls.
---

# LLM & Costs

The LLM & Costs tab gives you complete visibility into your AI spending.

<!-- IMAGE: LLM & Costs tab showing cost cards and Cost by Model Over Time chart -->

## Cost cards

| Card | Description |
| --- | --- |
| **Total Cost** | Total spend for the selected period |
| **Total Tokens** | Input + output tokens consumed |
| **Cost Per Request** | Average cost per API call |
| **Top Spender** | The agent or model costing the most |

## Cost by Model Over Time

An interactive line chart showing cost trends broken down by model:
- Each model gets its own coloured line
- Hover for exact daily costs
- Toggle models on/off to compare
- Time range selector (7D, 30D, 90D)

<!-- IMAGE: Cost by Model Over Time chart with multiple model lines -->

## Cost breakdown

{% tabs %}
{% tab title="By Model" %}
Table showing each model's:
- Total cost
- Token count (input/output split)
- Request count
- Avg cost per request
{% endtab %}

{% tab title="By Agent" %}
Table showing each agent's:
- Total cost
- Primary model used
- Request count
- Cost trend (increasing/decreasing)
{% endtab %}

{% tab title="By Time" %}
Daily/weekly/monthly cost aggregation:
- Bar chart of spend over time
- Moving average trend line
- Projected monthly cost
{% endtab %}
{% endtabs %}

## Cost Projections

Based on current usage patterns, the platform projects:
- **Monthly estimate** — projected cost for the current month
- **Trend direction** — increasing, stable, or decreasing
- **Anomaly alerts** — unusual cost spikes flagged

{% hint style="warning" %}
Cost projections are estimates based on recent usage. Actual costs depend on usage patterns, which can change.
{% endhint %}

## Tips for cost optimisation

1. **Use cheaper models for simple tasks** — route straightforward queries to Haiku or GPT-3.5
2. **Monitor the Top Spender card** — investigate if one agent dominates costs
3. **Check token efficiency** — agents with low efficiency may need prompt optimisation
4. **Set cost alerts** — configure budget thresholds in Settings
