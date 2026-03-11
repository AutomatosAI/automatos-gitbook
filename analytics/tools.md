---
description: Tool usage analytics and integration health.
---

# Tools & Integrations Analytics

The Tools & Integrations tab tracks how your connected tools are being used.

<!-- IMAGE: Tools Analytics showing usage charts and error rates -->

## Key metrics

| Metric | Description |
| --- | --- |
| **Total Tool Calls** | Number of external API calls made by agents |
| **Success Rate** | Percentage of tool calls that completed successfully |
| **Avg Latency** | Mean response time for tool calls |
| **Error Rate** | Percentage of failed tool calls |

## Usage breakdown

- **Calls by tool** — which tools are used most (bar chart)
- **Calls by agent** — which agents make the most tool calls
- **Time distribution** — when tool calls happen (useful for spotting scheduled patterns)

## Error analysis

Failed tool calls are grouped by:
- **Error type** — authentication, rate limit, timeout, validation
- **Tool** — which integration is failing
- **Frequency** — how often the error occurs

{% hint style="info" %}
High error rates on a specific tool usually mean the connection needs re-authentication. Check [Tools → Security](../tools/security.md).
{% endhint %}

## Latency distribution

A histogram showing tool call response times. Look for:
- **Bimodal patterns** — some calls fast, others slow (possible rate limiting)
- **Long tails** — occasional very slow calls (timeout candidates)
- **Consistent high latency** — tool or network issues
