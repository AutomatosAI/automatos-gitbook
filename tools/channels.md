---
description: Connect messaging platforms so agents can communicate through Telegram, Slack, WhatsApp, and more.
---

# Channels

Channels connect your Automatos workspace to external messaging platforms. Once connected, your agents can receive messages from and send responses through these platforms — extending your AI workforce beyond the Automatos chat interface.

## Supported channels

| Channel | Connection method | Notes |
| --- | --- | --- |
| **Telegram** | Bot token (polling-based) | Create a bot via @BotFather, paste the token |
| **Slack** | OAuth app installation | Installs as a Slack app in your workspace |
| **WhatsApp** | Webhook-based | Requires WhatsApp Business API setup |
| **Discord** | Bot token | Create a Discord bot application |
| **Microsoft Teams** | App registration | Requires Azure AD app registration |
| **Google Chat** | Service account | Uses Google Workspace integration |
| **iMessage** | Local adapter | Requires macOS with Messages access |
| **Matrix** | Homeserver credentials | Open-source, self-hosted messaging |
| **Signal** | Signal CLI | Privacy-focused encrypted messaging |

## Setting up a channel

1. Go to **Tools & Integrations** from the sidebar
2. Search for the messaging platform you want to connect
3. Click the app card and follow the authentication steps
4. Save your credentials

Once connected, the channel appears as "Live" on the Activity Dashboard.

## How channel messages are routed

Messages from all channels go through the same **Universal Router** as the Automatos chat interface. This means:
- The same multi-tier routing (cache → rules → semantic → LLM) applies
- Agents respond using the same tools, knowledge, and capabilities
- Responses are sent back through the originating channel

The system uses a `RequestEnvelope` format internally, so all channels are treated uniformly.

## Channel credentials

Channel tokens and credentials are stored securely in your workspace. Go to **Settings → Credentials** to:
- View connection status (without exposing the full token)
- Rotate credentials
- Test connections

{% hint style="warning" %}
Disconnecting a channel immediately stops all message flow. Agents will no longer receive or respond to messages on that platform.
{% endhint %}

## Monitoring channels

- **Activity → Dashboard** — "Channels Live" card shows how many channels are active
- **Activity → Feed** — see messages flowing from external channels
- **Analytics → Tools** — channel usage statistics

## Tips

- Start with one channel (Telegram is the easiest to set up)
- Test routing by sending messages from the external platform and checking the Activity Feed
- Channel-specific formatting (Slack blocks, Telegram markdown) is handled automatically
- Messages from channels appear in the same conversation history as Automatos chat

## Related

- [Connecting Apps](connecting-apps.md) — general guide to authenticating tools
- [Routing & Auto Mode](../chat/routing.md) — how the router handles all messages
- [Security](security.md) — credential management and audit trail
