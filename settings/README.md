---
description: System configuration, credentials, and audit logs.
---

# Settings

The Settings page is the control panel for your workspace. Manage system configuration, API keys, model preferences, and review audit logs.

<!-- IMAGE: Settings page showing configuration panel -->

{% hint style="info" %}
Settings is only accessible to workspace admins.
{% endhint %}

## Sections

{% tabs %}
{% tab title="General" %}
Platform-wide configuration:
- Workspace name and description
- Default language and timezone
- Feature flags
- Notification preferences

[Full guide →](general.md)
{% endtab %}

{% tab title="API Keys & Credentials" %}
Manage API keys for LLM providers and external services:
- Add, edit, and rotate credentials
- Test connection validity
- View expiry dates
- Credential type management

[Full guide →](credentials.md)
{% endtab %}

{% tab title="Models" %}
Configure available LLM models:
- Default model selection
- Provider priority order
- Model-specific parameters
- Fallback configuration

[Full guide →](models.md)
{% endtab %}

{% tab title="Audit Logs" %}
Complete record of system activity:
- User actions
- Agent operations
- Configuration changes
- Security events

[Full guide →](audit-logs.md)
{% endtab %}
{% endtabs %}

## Subpages

| Page | Description |
| --- | --- |
| [General](general.md) | Core platform settings |
| [API Keys & Credentials](credentials.md) | Managing secrets and API keys |
| [Models](models.md) | LLM model configuration |
| [Audit Logs](audit-logs.md) | Activity and security audit trail |

## Channels and integrations

Channel credentials (Telegram bot tokens, Slack app tokens and so on) are entered in **Settings → Channels**. They are not shown again after you connect; each channel's card shows its connection status. See [Channels](../tools/channels.md).

## BYOK — Bring Your Own Key

Users can provide their own API keys for LLM providers instead of using the workspace default. This is useful for teams where individuals have their own API accounts. Add your keys under **Settings → API Keys** and toggle each provider to choose whether your key is used for chat and agent execution.
