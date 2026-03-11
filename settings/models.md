---
description: Configure available LLM models and provider settings.
---

# Models

The Models section controls which LLM models are available in your workspace and how they're configured.

<!-- IMAGE: Models configuration showing provider list and model settings -->

## Provider configuration

Set up each LLM provider:

{% tabs %}
{% tab title="OpenRouter" %}
OpenRouter gives access to 100+ models from all major providers through a single API key.

- **API Key** — set in [Credentials](credentials.md)
- **Base URL** — `https://openrouter.ai/api/v1` (default)
- **Default Model** — the model used when agents don't specify one

Popular models via OpenRouter:
- `anthropic/claude-sonnet-4-20250514`
- `google/gemini-2.5-pro`
- `deepseek/deepseek-chat`
- `openai/gpt-4`
{% endtab %}

{% tab title="OpenAI" %}
Direct OpenAI API access.

- **API Key** — set in [Credentials](credentials.md)
- **Organisation ID** — optional, for org-scoped billing

Models:
- `gpt-4`
- `gpt-4-turbo`
- `gpt-3.5-turbo`
{% endtab %}

{% tab title="Anthropic" %}
Direct Anthropic API access.

- **API Key** — set in [Credentials](credentials.md)

Models:
- `claude-opus-4-20250514`
- `claude-sonnet-4-20250514`
- `claude-haiku-4-5-20251001`
{% endtab %}

{% tab title="DeepSeek" %}
DeepSeek models for cost-effective tasks.

- **API Key** — set in [Credentials](credentials.md)

Models:
- `deepseek-chat`
- `deepseek-coder`
{% endtab %}
{% endtabs %}

## Default model

The default model is used when:
- An agent doesn't have a model explicitly set
- New agents are created without specifying a model
- System-level tasks (routing, classification) need an LLM

Set the default in [General Settings](general.md).

## Model fallback

Configure a fallback chain for resilience:
1. **Primary** — the agent's assigned model
2. **Fallback 1** — used if primary is unavailable or rate-limited
3. **Fallback 2** — last resort

{% hint style="info" %}
Using OpenRouter as your primary provider gives you built-in fallback — OpenRouter routes to alternative models automatically if one is down.
{% endhint %}

## Embedding model

The embedding model is used for document chunking and semantic search:
- Default: `qwen/qwen3-embedding-8b` via OpenRouter
- Dimensions: 2048
- Configurable in Settings

{% hint style="warning" %}
Changing the embedding model requires re-processing all documents. Existing embeddings become incompatible with the new model.
{% endhint %}
