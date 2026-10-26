---
description: Talk to your AI agents through a unified chat interface.
---

# Chat

The Chat page is your primary way to interact with Automatos AI. Type a message and the platform automatically routes it to the best agent for the job.

<!-- IMAGE: Chat interface with welcome message and quick actions bar -->

## How it works

1. You type a message in the chat input
2. The **Universal Router** analyses your message
3. It selects the best agent based on content, context, and history
4. The agent responds — using its tools, knowledge, and skills as needed
5. You see the response streamed in real-time

{% hint style="info" %}
You don't need to know which agent to talk to. The router handles it. But you can override it if you want — see [Routing & Auto Mode](routing.md).
{% endhint %}

## The chat interface

The chat page has three main areas:

| Area | What it does |
| --- | --- |
| **Chat history** | Left sidebar — your previous conversations |
| **Message area** | Centre — the conversation thread with streaming responses |
| **Input bar** | Bottom — where you type, with quick actions and model selector |

### Input bar features

- **Attachment button** — upload files directly into the conversation
- **Auto mode selector** — shows which routing mode is active (Auto, or a specific agent)
- **Model indicators** — shows which LLM models are available
- **Voice button** — the microphone next to **Send**: hold it to talk to Auto
- **Quick actions** — shortcut buttons below the input for common tasks

<!-- IMAGE: Close-up of the chat input bar with Auto mode and quick actions -->

### Voice chat

You can talk to Auto instead of typing:

- **Hold to talk**, on every plan: hold the microphone button next to **Send**, speak, and let go. Your words go to Auto as a message in this conversation, and your browser reads the answer aloud.
- **Auto Live**: a real-time voice call with Auto, from the **Live** button. On the hosted edition it comes with the Business plan.

See [Voice Chat](voice.md) for the full guide.

## Quick actions

Below the chat input, you'll see shortcut buttons:

| Action | What it does |
| --- | --- |
| **Live** | Start or end an Auto Live voice call |
| **Code** | Open the Code canvas on your workspace's files |
| **Plan** | Plan mode: get a structured plan without taking any actions, then launch it as a Mission |
| **Mission** | Open Missions to give your agents a goal |
| **Pinned agents** | Send messages straight to an agent you've pinned |

See [Quick Actions](quick-actions.md) for details.

## What to try first

**Ask a question about your documents:**
> "What does our API authentication flow look like?"

**Start a coding task:**
> "Review the login component for security issues"

**Check on your agents:**
> "What did the Brand Designer work on today?"

**Run a workflow:**
> "Run the Two-minute brief playbook on electric bikes"

### Switching agents mid-conversation

You can switch to a different agent at any time during a conversation. Click the agent name in the chat header or use the Auto dropdown to pick a new agent. The new agent picks up the conversation context.

### File attachments

Attach files to your messages using the attachment button. Supported types include:
- PDFs, images, and documents (up to 20 MB)
- The agent can read and reference attached files in its response

### Context and streaming

- Responses stream in real-time via SSE (Server-Sent Events) — you see tokens as they arrive
- Each conversation maintains a context budget of approximately 60,000 tokens
- Long conversations are automatically summarised to preserve important context
- Conversations are independent — starting a new chat resets the context window

{% hint style="success" %}
The more agents and knowledge you add, the more capable your chat becomes. Start by uploading a few documents and creating one or two agents.
{% endhint %}

## Subpages

| Page | Description |
| --- | --- |
| [Routing & Auto Mode](routing.md) | How message routing works and how to override it |
| [Quick Actions](quick-actions.md) | Detailed guide to chat shortcuts |
| [Chat History](history.md) | Managing and searching past conversations |
| [Voice Chat](voice.md) | Talking to Auto by voice: hold to talk and Auto Live |
