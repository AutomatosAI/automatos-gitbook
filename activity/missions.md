---
description: Track long-running objectives across agents and tasks.
---

# Missions

Missions are autonomous, multi-step objectives that your AI agents plan and execute independently. Think of them as giving your AI team a goal and letting them figure out how to achieve it.

## How missions work

1. You describe what you want accomplished
2. An agent creates an execution plan with tasks and milestones
3. You review and approve (or reject) the plan
4. Agents execute the plan step-by-step, using tools and knowledge as needed
5. You can monitor progress, pause, resume, or cancel at any time

## Creating a mission

1. Click **+ New Mission** from the Missions tab
2. Describe your objective in natural language — be as specific as you can
3. Optionally attach files (PDFs, images, documents — up to 20 MB)
4. The system generates an execution plan

### Writing good mission objectives

Be specific:
- Good: "Audit all API endpoints for missing rate limiting and create Jira tickets for each finding"
- Vague: "Check the API security"

Include success criteria when possible:
- "Reduce average API response time to under 200ms across all endpoints"
- "Complete Q1 security audit covering authentication, authorisation, and data encryption"

## Mission lifecycle

| Status | What it means | Your options |
| --- | --- | --- |
| **Plan Pending** | Agent has created a plan, waiting for your review | Approve or Reject |
| **Active** | Agents are executing the plan | Pause, Cancel, or monitor |
| **Paused** | Execution is on hold | Resume (optionally with increased budget) |
| **Completed** | All tasks finished successfully | Archive, or Save as Routine |
| **Cancelled** | You stopped the mission | Archive for reference |
| **Archived** | Stored for historical reference | View full snapshot |

## Monitoring progress

Each active mission shows:
- **Task list** — individual tasks with status (pending, in progress, completed, failed)
- **Event timeline** — chronological log of everything that happened
- **Cost breakdown** — per-task token usage and estimated cost
- **Agent involvement** — which agents worked on which tasks
- **Checkpoints** — saved state snapshots at key milestones

Click any task to see its detailed execution log, including tool calls, LLM interactions, and intermediate results.

## Budget management

Missions consume tokens as agents work. You can:
- View the **cost breakdown by task** to see where tokens are being spent
- **Pause** a mission if costs are exceeding expectations
- **Resume with increased budget** if a mission needs more resources than originally estimated

## File attachments

Attach files when creating a mission to give agents additional context:
- Supported formats: PDF, PNG, JPG, DOCX, TXT, and more
- Maximum file size: 20 MB
- Agents can reference attached files during execution

## Saving as a routine

Completed missions can be converted into reusable recipe templates:

1. Open a completed mission
2. Click **Save as Routine**
3. The system extracts the task pattern into a recipe
4. Run the recipe on demand or schedule it

This is great for turning one-off objectives into repeatable workflows.

## Searching archived missions

Use the archive search to find past missions by:
- Keyword search across mission descriptions and results
- Status filter (completed, cancelled)
- Date range
- Agent filter

{% hint style="info" %}
Mission statistics (total count, success rates, average duration) are available in **Analytics → Workflows**. Per-agent mission history is visible in the Agent Details panel.
{% endhint %}

## Related

- [Dashboard](dashboard.md) — see active missions alongside other workspace activity
- [Recipes](../agents/recipes.md) — reusable workflows that missions can be converted into
- [Analytics → Workflows](../analytics/workflows.md) — mission and recipe performance metrics
