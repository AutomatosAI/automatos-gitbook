---
description: Manage API keys and secrets for LLM providers and integrations.
---

# API Keys & Credentials

Credentials are the API keys and secrets that connect your workspace to LLM providers and external services.

<!-- IMAGE: Credentials panel showing list of stored API keys -->

## Adding a credential

1. Click **+ Add Credential**
2. Select the credential type (OpenRouter, OpenAI, Anthropic, etc.)
3. Enter the API key or secret
4. Give it a label for identification
5. Click **Save**

<!-- IMAGE: Add Credential dialog with type selector and key input -->

## Credential types

| Type | What it connects |
| --- | --- |
| **OpenRouter** | Primary LLM provider (100+ models) |
| **OpenAI** | GPT models directly |
| **Anthropic** | Claude models directly |
| **Composio** | Tool integration framework |
| **Clerk** | Authentication service |
| **AWS** | S3 storage and vectors |
| **Custom** | Any API key for custom integrations |

## Managing credentials

For each stored credential:
- **Test** — verify the key is valid and connection works
- **Edit** — update the key (e.g., after rotation)
- **Delete** — remove the credential
- **View usage** — see which agents and tools use this credential

{% hint style="warning" %}
Deleting a credential immediately breaks all agents and tools that depend on it. Test the replacement before removing the old key.
{% endhint %}

## Security

- Credentials are encrypted at rest
- Keys are never displayed in full after saving (masked)
- All credential access is logged in [Audit Logs](audit-logs.md)
- Credentials are workspace-scoped — not shared between workspaces

## Rotation

To rotate a credential:
1. Create the new key in the external service
2. Edit the credential in Settings
3. Paste the new key
4. Click **Save**
5. Test to verify

No downtime — the new key takes effect immediately.
