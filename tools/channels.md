---
description: Connect Telegram, Slack, Discord or WhatsApp to your workspace, or send results to your own webhook.
---

# Channels

Channels connect your Automatos workspace to external messaging platforms. Once a channel is connected, your agents can receive messages from it and send responses through it, beyond the Automatos chat interface.

## Supported channels

Automatos supports four chat channels, Telegram, Slack, Discord and WhatsApp, plus a generic webhook.

| Channel | What you need | Notes |
| --- | --- | --- |
| **Telegram** | A bot token from @BotFather | Two connection modes: **Webhook** (recommended on hosted) or **Polling**. Polling needs no public URL, so it is the default on the local edition |
| **Slack** | A Slack app's bot token (`xoxb-…`), signing secret and app token (`xapp-…`) | After connecting, paste the webhook URL shown on the Slack card into your Slack app's event settings |
| **WhatsApp** | A phone number ID and a permanent access token from Meta (WhatsApp Cloud API) | After connecting, paste the webhook URL shown on the WhatsApp card into Meta's webhook settings. The optional verify token is used for Meta's handshake |
| **Discord** | A bot token from the Discord developer portal | Agents can post to Discord. Receiving messages from Discord is not available yet |
| **Generic webhook** | An HTTPS URL | Outbound only: results are sent as a JSON POST to your own endpoint (for example Zapier, n8n or your own service). Choose **Webhook URL** where a delivery destination is offered, such as an agent's heartbeat settings |

{% hint style="info" %}
Only the channels above carry messages today. Other platform cards on the Channels page have no connector yet.
{% endhint %}

## Setting up a channel

1. Go to **Settings → Channels**
2. Find the card for the platform you want to connect
3. Enter the credentials it asks for (use **Setup Guide** on the card for the platform's own instructions)
4. For Telegram, choose the connection mode
5. Click **Connect**

Once connected, the card shows the channel's status, message count, connection mode and, for webhook-mode channels, the webhook URL to copy into the platform. Use **Test** to check the connection again.

{% hint style="warning" %}
**Local edition:** inbound messages on webhook-mode channels need a public URL in front of your install (for example a tunnel). Outbound delivery works without one, and Telegram in polling mode needs no public URL.
{% endhint %}

## How channel messages are routed

Incoming messages go through the same **Universal Router** as the Automatos chat interface. This means:
- The same multi-tier routing (cache → rules → semantic → LLM) applies
- Agents respond using the same tools, knowledge, and capabilities
- Responses are sent back through the originating channel

The system uses a `RequestEnvelope` format internally, so all channels are treated uniformly.

## Channel credentials

Channel tokens are entered on the channel's card in **Settings → Channels** and stored in your workspace. They are not shown again after you connect. To change a token, disconnect the channel and connect it again with the new one.

{% hint style="warning" %}
**Disconnect** asks you to confirm, then removes the channel from your workspace and stops its webhook or polling. Agents will no longer receive or respond to messages on that platform.
{% endhint %}

## Monitoring channels

- **Settings → Channels** — status, message count and last activity on each card
- **Analytics → Overview** — the Channel Activity card shows message counts for web chat, Telegram, Slack, Discord and webhooks

## Tips

- Start with one channel (Telegram is the easiest to set up)
- Test routing by sending a message from the external platform and checking that the reply comes back

## Related

- [Routing & Auto Mode](../chat/routing.md) — how the router handles all messages
- [Security](security.md) — credential management and audit trail
