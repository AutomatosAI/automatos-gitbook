# MCP Control

## Overview
Automatos AI can be controlled via the **Model Context Protocol (MCP)**.

## Available Commands

### Agents
- `list_agents`
- `create_agent`
- `delete_agent`

### Workflows
- `list_workflows`
- `run_workflow`

### Policies
- `get_policy`
- `update_policy`

### Playbooks
- `mine_playbooks`
- `promote_playbook`

## Example MCP Payload
```json
{
  "command": "create_agent",
  "params": {
    "name": "New Agent",
    "policy": "default"
  }
}
```
