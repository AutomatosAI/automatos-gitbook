---
description: Step-by-step guide to creating a new agent.
---

# Creating an Agent

Click **+ Create Agent** from the Agent Management page to open the creation dialog.

## Step 1: Choose a starting point

{% tabs %}
{% tab title="From Template" %}
Pick a pre-built template to get started fast. Templates come with sensible defaults for model, persona, tools, and system prompt.

Available templates include:
- **Code Reviewer** — reviews pull requests and code quality
- **QA Engineer** — runs tests and validates functionality
- **Sentinel** — security monitoring and auditing
- **Scribe** — documentation and report writing
- **Scout** — research and information gathering
- **Comms** — handles communication and email workflows

<!-- IMAGE: Template selection grid in the create agent dialog -->
{% endtab %}

{% tab title="From Scratch" %}
Start with a blank agent. You'll configure everything manually — useful when you need a custom specialist that doesn't match any template.
{% endtab %}
{% endtabs %}

## Step 2: Basic information

| Field | Required | Description |
| --- | --- | --- |
| **Name** | Yes | A display name for the agent |
| **Category** | Yes | The agent's type (custom, support, code_architect, etc.) |
| **Description** | Recommended | What the agent does — used by the router for matching |

{% hint style="info" %}
Write a clear, specific description. The Universal Router uses it to decide when to send messages to this agent. "Handles code reviews for JavaScript and TypeScript" is better than "Code stuff".
{% endhint %}

## Step 3: Model selection

Choose which LLM powers this agent:

| Setting | Description |
| --- | --- |
| **Provider** | OpenRouter, OpenAI, Anthropic, or DeepSeek |
| **Model** | The specific model ID (e.g., claude-sonnet-4-20250514, gpt-4, deepseek-chat) |
| **Temperature** | Controls creativity (0 = deterministic, 1 = creative) |
| **Max tokens** | Maximum response length |

<!-- IMAGE: Model selection dropdown showing available providers and models -->

## Step 4: Persona

Select a persona that defines the agent's communication style and personality:
- **Professional** — formal, detailed responses
- **Casual** — conversational and approachable
- **Technical** — precise, code-focused responses
- **Custom** — write your own persona description

## Step 5: Tools and skills

Assign tools from your connected integrations:
- **Tools** — apps like GitHub, Slack, Jira (via Composio)
- **Skills** — git-based capability packages
- **Plugins** — marketplace-installed bundles

{% hint style="success" %}
You can always add or remove tools later from the [Agent Details](details.md) panel.
{% endhint %}

## Step 6: Create

Click **Create** to deploy your agent. It appears on the roster immediately and is ready to receive messages through Chat.
