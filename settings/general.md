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
