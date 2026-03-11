---
description: Browse and configure available language models.
---

# LLMs

The LLMs tab lets you explore all available language models, compare their capabilities, and configure which ones your agents can use.

<!-- IMAGE: LLMs tab showing model cards with provider, pricing, and capabilities -->

## Available providers

| Provider | Models |
| --- | --- |
| **OpenRouter** | Access to 100+ models from all providers |
| **OpenAI** | GPT-4, GPT-4 Turbo, GPT-3.5 |
| **Anthropic** | Claude Opus, Sonnet, Haiku |
| **DeepSeek** | DeepSeek Chat, DeepSeek Coder |
| **Google** | Gemini Pro, Gemini Flash |

## Model cards

Each model card shows:
- **Model name** and provider
- **Pricing** — per million input/output tokens
- **Context window** — maximum token capacity
- **Capabilities** — vision, function calling, JSON mode
- **Speed** — relative latency rating

## Selecting models

Models are assigned to agents during [agent creation](../agents/creating.md) or editing. The LLMs tab helps you compare options before deciding.

{% hint style="info" %}
OpenRouter is the default provider and gives you access to most models through a single API key. Configure your API key in [Settings → Credentials](../settings/credentials.md).
{% endhint %}

## Cost considerations

Track actual model costs in [Analytics → LLM & Costs](../analytics/llm-costs.md). The marketplace shows list pricing — your actual costs depend on usage volume and provider agreements.
