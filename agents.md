---
title: Agent Management
---

Agents encapsulate **role**, **tools**, and a default **policy**.

## Create an Agent
1. Go to **Agents → New**.  
2. Fill **Name**, **Description** (optional).  
3. Pick **Default Policy**.  
4. Enable **Tools** and set budgets/timeouts.  
5. **Save**.

**API**  
> **Authentication**  
> All API calls require headers:  
> ```http
> X-API-Key: <your_key>
> Authorization: Bearer <your_token>
> ```

- `POST /api/agents`  
```json
{ "name":"Code Assistant","policy_id":"code_assistant","tools":["search","exec"],"limits":{"max_tokens":4096,"budget_usd":5} }
```

## Edit / Delete
Update policy/tools/limits or remove unused agents.

**API**  
- `GET /api/agents` (list)  
- `GET /api/agents/{id}` (detail)  
- `PUT /api/agents/{id}` (update)  
- `DELETE /api/agents/{id}` (delete)

## Runs
Inspect recent runs for a given agent.

**API**  
`GET /api/runs?agent_id={id}&limit=50`

## Tips
- Start with a conservative **budget**.  
- Keep tool lists minimal per agent to reduce ambiguity.
