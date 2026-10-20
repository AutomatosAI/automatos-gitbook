---
description: How the Universal Router sends your messages to the right agent.
---

# Routing & Auto Mode

When you send a message in Chat, the Universal Router decides which agent should handle it. This happens automatically, but you have full control over the process.

## Auto mode (default)

When **Auto** is selected in the chat input, the router uses a multi-tier system:

{% tabs %}
{% tab title="Tier 0 — User Override" %}
If you've manually selected a specific agent from the dropdown, the message goes directly to that agent. No routing logic runs.
{% endtab %}

{% tab title="Tier 1 — Cache" %}
If you've asked a similar question before and it was successfully routed, the system reuses that routing decision. This is fast and free (no LLM call).
{% endtab %}

{% tab title="Tier 2 — Rules" %}
Keyword-based rules match your message against known patterns. For example, a rule could send messages that mention "logo" or "brand colours" to the Brand Designer.
{% endtab %}

{% tab title="Tier 2.5 — Semantic" %}
If rules don't match, the router uses semantic similarity to compare your message against agent descriptions and past successful routings.
{% endtab %}

{% tab title="Tier 3 — LLM" %}
As a final fallback, an LLM classifies your message and picks the best agent. This is the most expensive tier but handles novel queries well.
{% endtab %}
{% endtabs %}

## Selecting a specific agent

Click the **Auto** dropdown in the chat input to see all available agents. Select one to bypass routing entirely.

<!-- IMAGE: Agent selector dropdown in chat input showing available agents -->

{% hint style="info" %}
Selecting a specific agent is useful when you know exactly who you want to talk to, or when you're testing a new agent's responses.
{% endhint %}

## Routing corrections

If the router picks the wrong agent, you can correct it. The system learns from corrections and improves over time.

When you notice a response came from the wrong agent:
1. The response header shows which agent handled it
2. Use the correction mechanism to reassign
3. Future similar messages will route correctly

## How routing decisions are stored

Every routing decision is logged to a database table. This means:
- The system builds a history of which agents handle which types of messages
- Corrections you make feed directly into future routing
- You can view routing patterns in **Analytics → Agents**

## Tips

- **New agents** take a few interactions to get into the routing cache. Be patient.
- **Specific keywords** in agent descriptions help the rule-based tier match faster.
- **Semantic routing** works better when agents have detailed, distinct descriptions.

## Channel routing

The Universal Router also handles messages that arrive from external channels (Telegram, Slack and WhatsApp). They go through the same multi-tier routing system, so agent selection works the same way wherever the message comes from.

See [Channels](../tools/channels.md) for setting up channels.
