---
description: Step-by-step guide to creating a new agent.
---

# Creating an Agent

Click **+ Create Agent** from the Agent Management page to open the creation dialog. It has five steps: **Config**, **Persona**, **Model**, **Tools** and **Capabilities**. Use **Next** and **Previous** to move between them.

{% hint style="info" %}
There are no agent templates in this dialog. To start from a ready-made agent, install one from the [Marketplace](../marketplace/agents.md) and customise it.
{% endhint %}

## Step 1: Config

| Field | Required | Description |
| --- | --- | --- |
| **Category** | Yes | The kind of work the agent does: Analytics, Business, Communication, Design, Development, Education, General, HR, Legal, Marketing, Productivity, Research, Sales, Support, Writing or Custom |
| **Agent Name** | Yes | A display name for the agent |
| **Description** | Recommended | What the agent does — used by the router for matching |
| **Tags** | No | Comma-separated keywords that describe the agent's strengths |
| **Share to Marketplace** | No | Submits the agent to the marketplace approval queue with the same name, description, category and tags |

{% hint style="info" %}
Write a clear, specific description. The Universal Router uses it to decide when to send messages to this agent. "Handles code reviews for JavaScript and TypeScript" is better than "Code stuff".
{% endhint %}

## Step 2: Persona

A persona sets the agent's personality, voice and working style. Choose one of three options:

- **No Persona** — default behaviour
- **Predefined** — pick a persona preset. The list shows the presets that match the category you chose in step 1 (choose the Custom category to see them all). The built-in presets are Senior Engineer, Code Reviewer, DevOps / SRE Engineer, Content Strategist, SEO Specialist, Sales Development Representative, Account Executive, Customer Success Manager, Technical Support Engineer and Customer Advocate, plus any personas your workspace has added.
- **Custom** — write your own persona prompt. If you selected a preset first, its prompt is filled in as a starting point.

<!-- IMAGE: Persona step in the create agent dialog -->

## Step 3: Model

Choose which model powers this agent and tune its parameters:

| Setting | Description |
| --- | --- |
| **Runtime** (local edition only) | Where the agent runs: an API model, or your own Claude Code / CLI session |
| **Model** | The model, and the provider that serves it |
| **Temperature** | Controls creativity (0 = deterministic, higher = more creative) |
| **Max Output Tokens** | Maximum response length |
| **Top P**, **Frequency Penalty**, **Presence Penalty** | Advanced sampling settings |
| **Fallback Model** | Optional model used if the main one is unavailable |

<!-- IMAGE: Model step showing the model selector and parameters -->

## Step 4: Tools

Choose the tools this agent can use, from the apps connected in [Tools & Integrations](../tools/README.md). If no tools are listed, connect an app there first.

## Step 5: Capabilities

Choose the capabilities (plugins enabled for your workspace) that teach the agent new skills. If none are enabled yet, you can assign capabilities later.

Click **Create Agent**. The agent appears on the roster immediately and is ready to receive messages through Chat.

{% hint style="success" %}
You can change these settings later from the [Agent Details](details.md) panel.
{% endhint %}

## Testing your agent

After creating an agent, test it before relying on it for production work:

1. **Chat test** — open Chat, select your agent from the dropdown, and send a few messages. Check that it responds appropriately and uses its assigned tools.
2. **Capability test** — from the Agent Details panel, click **Run Capability Test**. This runs a comprehensive evaluation and returns a scored report covering:
   - Response quality
   - Tool usage accuracy
   - Persona adherence
   - Error handling
3. **Review routing** — send messages in Auto mode and check that the router correctly directs relevant queries to your new agent. If not, improve the agent's description.

{% hint style="info" %}
New agents take a few routing cycles to be picked up by the semantic and cache tiers. Give it 5-10 interactions before evaluating routing accuracy.
{% endhint %}

## Prompt engineering tips

Your agent's system prompt is the single biggest factor in response quality. Follow these guidelines:

### Be specific about the role
Bad: "You are a helpful assistant"
Good: "You are a senior TypeScript developer specialising in React performance optimisation. You review code for render bottlenecks, unnecessary re-renders, and bundle size issues."

### Define output format
Tell the agent how to structure responses: "Always list findings as numbered items with severity (HIGH/MEDIUM/LOW) and a one-line fix suggestion."

### Set boundaries
Specify what the agent should NOT do: "Do not suggest rewriting entire components. Focus on targeted fixes to the specific code provided."

### Include examples
Provide 1-2 example interactions showing the expected input and output. This dramatically improves consistency.

### Reference tools explicitly
If the agent has tools, mention them: "Use the GitHub tool to fetch pull request diffs before reviewing. Always check the latest commit, not just the PR description."
