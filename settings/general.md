---
description: Core platform configuration.
---

# General Settings

The General section contains workspace-wide configuration options.

<!-- IMAGE: General settings panel showing platform information and configuration fields -->

## Platform information (read-only)

| Field | Description |
| --- | --- |
| **Platform Version** | Current deployed version |
| **API Version** | Backend API version |
| **Installation ID** | Unique workspace identifier |

## Configurable settings

### Workspace

| Setting | Description |
| --- | --- |
| **Workspace Name** | Display name for your workspace |
| **Description** | Short description shown to team members |
| **Timezone** | Default timezone for schedules and reports |

### Defaults

| Setting | Description |
| --- | --- |
| **Default Model** | The LLM model used when not specified |
| **Max Tokens** | System-wide maximum response length |
| **Temperature** | Default creativity setting |

### Features

Toggle feature flags:
- **Agent memory** — enable/disable persistent memory
- **Cloud sync** — allow cloud storage connections
- **Workspace execution** — enable sandboxed code execution
- **Cost alerts** — notify on budget thresholds

{% hint style="info" %}
Changes to general settings take effect immediately. No restart required.
{% endhint %}

## Feature flags

Feature flags control optional platform capabilities. Available flags:

| Flag | Description |
| --- | --- |
| **Voice chat** | Enable/disable voice input and text-to-speech |
| **Advanced analytics** | Enable predictive alerts and bottleneck detection |
| **Knowledge graph** | Enable automatic entity extraction from documents |
| **Mission mode** | Enable autonomous multi-step mission execution |

Toggle flags from General settings. Changes take effect immediately.

## Notification preferences

Configure how and when you receive notifications:
- **In-app** — badges and alerts within the Automatos interface
- **Email** — summaries and critical alerts via email
- **Channel** — notifications sent to connected channels (Slack, Telegram, etc.)
