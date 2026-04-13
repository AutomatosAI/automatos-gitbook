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
- **Quick actions** — shortcut buttons below the input for common tasks

<!-- IMAGE: Close-up of the chat input bar with Auto mode and quick actions -->

### Voice chat

Automatos supports voice-in, voice-out conversations. Click the microphone icon in the input bar to speak your message — it's transcribed, processed by the assigned agent, and the response is spoken back using text-to-speech.

Voice features:
- **Speech-to-text** — your voice is transcribed automatically
- **Text-to-speech** — agent responses are read aloud
- **Voice profiles** — choose from different voice options, including custom cloned voices
- **Audio playback** — listen to responses via the built-in player

Go to **Settings → Voice Profiles** to manage voice options. See [Voice Chat](voice.md) for the full guide.

## Quick actions

Below the chat input, you'll see shortcut buttons:

| Action | What it does |
| --- | --- |
| **Code** | Start a coding task — routes to your code-focused agents |
| **Create an Agent** | Jump to agent creation without leaving chat |
| **Knowledge Base** | Ask questions about your uploaded documents |
| **Recipes** | Browse and run multi-step workflows |
| **Edit Tools** | Manage tool assignments for your agents |

## What to try first

**Ask a question about your documents:**
> "What does our API authentication flow look like?"

**Start a coding task:**
> "Review the login component for security issues"

**Check on your agents:**
> "What did Sentinel find in today's audit?"

**Run a workflow:**
> "Run the nightly test suite recipe"

### Switching agents mid-conversation

You can switch to a different agent at any time during a conversation. Click the agent name in the chat header or use the Auto dropdown to pick a new agent. The new agent picks up the conversation context seamlessly.

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
| [Voice Chat](voice.md) | Voice input/output and voice profiles |
