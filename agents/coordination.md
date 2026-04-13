---
description: Manage how agents work together as teams.
---

# Coordination

The Coordination tab manages multi-agent collaboration — how agents communicate, delegate tasks, and work together.

<!-- IMAGE: Coordination tab showing agent team assignments -->

## Team assignments

Group agents into teams for coordinated workflows. A team is a logical grouping where agents can:
- Hand off tasks to each other
- Share context within a workflow
- Report to a designated lead agent

## Delegation rules

Configure how agents can delegate work:

| Rule | Description |
| --- | --- |
| **Auto-delegate** | Agents can pass tasks to teammates automatically |
| **Approval required** | Delegation requires user confirmation |
| **Disabled** | Agents work independently only |

## Inter-agent communication

When agents work together on a recipe or mission:
- Each agent sees the output of previous steps
- Context is passed through the workflow pipeline
- Results are aggregated in the Activity feed

## How delegation works in practice

When an agent receives a task it can't fully handle alone:

1. The agent identifies which subtask needs a specialist
2. It creates a delegation request with context
3. The delegated agent receives the subtask and its context
4. The delegated agent completes the work and returns results
5. The original agent incorporates the results into its response

### Example: Code review with security

You ask Code Reviewer to review a pull request. It notices authentication changes and delegates a security review to Sentinel. Sentinel checks for vulnerabilities and passes findings back. Code Reviewer includes both code quality and security findings in the final response.

## Knowledge sharing between agents

Agents working on the same mission or recipe can share context through:
- **Workflow pipeline** — each step's output is available to the next step
- **Scratchpad** — a shared workspace for intermediate results
- **Memory** — agents can read each other's stored memories within the same workspace

{% hint style="info" %}
Coordination settings are most useful when running [Recipes](recipes.md) that chain multiple agents together.
{% endhint %}
