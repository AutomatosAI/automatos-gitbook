---
title: MCP Control
---

Automate Automatos from other agents via **Model Context Protocol (MCP)**.

## Transport & Auth
- Use the same API host as your backend.
- Forward `X-API-Key` and `Authorization` headers in your MCP client/bridge.

## Tools (Commands)

### Agents
- `list_agents()` → returns `{ id, name, policy_id }[]`
- `create_agent({"name","policy_id","tools?","limits?"})`
- `delete_agent({"id"})`

### Workflows
- `list_workflows()`
- `run_workflow({"id","input"})` → `{ run_id }`

### Policies
- `get_policy({"policy_id"})`
- `update_policy({"policy"})`

### Playbooks
- `mine_playbooks({"tenant_id","min_support","top_k"})`
- `promote_playbook({"playbook_id","name"})`

## Example Call
```json
{
  "tool_name": "run_workflow",
  "arguments": {"id": "wf_123", "input": {"query": "Summarize ticket #431"}}
}
```

## Error Handling
MCP should surface API errors verbatim. Standard format:
```json
{ "error": {"code":"BAD_REQUEST","message":"...", "details":{} } }
```
