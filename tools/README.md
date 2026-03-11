---
description: Connect your agents to 500+ external apps and services.
---

# Tools & Integrations

The Tools page lets you connect external applications to your workspace. Once connected, you can assign tools to agents so they can interact with GitHub, Slack, Jira, databases, and hundreds more.

<!-- IMAGE: Tools & Integrations page showing connected apps grid -->

## Page layout

{% tabs %}
{% tab title="Applications" %}
Browse and manage connected tools. Each tool card shows:
- App name and icon
- Connection status (Connected / Available)
- Number of tools and triggers available
- Assigned agent count

Search and filter by category: api services, productivity, developer tools, CRM, email marketing, analytics, and more.

[Managing connections →](connecting-apps.md)
{% endtab %}

{% tab title="Security" %}
Security status for your tool connections:
- Authentication health
- Permission scopes
- Credential expiry warnings
- Access audit log

[Security details →](security.md)
{% endtab %}
{% endtabs %}

## How tools work

1. **Connect** an app (e.g., GitHub) — authenticate via OAuth or API key
2. **Assign** it to one or more agents
3. **Agents use it** automatically when relevant — the tool router decides when to call tools based on the conversation context

Tools are powered by **Composio**, which provides 500+ pre-built integrations with a unified API.

## Stats bar

| Metric | Description |
| --- | --- |
| **Connected** | Number of apps currently authenticated |
| **Available** | Total integrations you can connect |
| **Sync** | Button to refresh connection status |

<!-- IMAGE: Stats bar showing 19 Connected, 500+ Available -->

{% hint style="info" %}
You don't need to connect everything upfront. Start with the tools your agents need most (GitHub, Slack, etc.) and add more as needed.
{% endhint %}

## Subpages

| Page | Description |
| --- | --- |
| [Connecting Apps](connecting-apps.md) | How to authenticate and connect a new tool |
| [Assigning Tools to Agents](assigning.md) | Give agents access to specific tools |
| [Security](security.md) | Tool connection security and permissions |
