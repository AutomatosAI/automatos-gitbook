---
description: REST API endpoints for programmatic access.
---

# API Reference

Automatos AI exposes a REST API for programmatic access to all platform features.

## Base URL

```
https://your-instance.railway.app/api
```

Or locally: `http://localhost:8000/api`

## Authentication

All API calls require authentication headers:

```http
Authorization: Bearer <your_clerk_token>
X-Workspace-ID: <your_workspace_id>
```

## Interactive docs

The full API documentation with request/response schemas is available at:

```
https://your-instance.railway.app/docs
```

This is an auto-generated Swagger/OpenAPI interface where you can test endpoints directly.

<!-- IMAGE: Swagger API docs interface -->

## Key endpoint groups

### Chat

| Method | Endpoint | Description |
| --- | --- | --- |
| `POST` | `/api/chat` | Send a message (returns SSE streaming response) |
| `POST` | `/api/chat/voice` | Send a voice message (audio upload → STT → agent → TTS) |
| `GET` | `/api/chat/conversations` | List conversations for the current user |
| `GET` | `/api/chat/conversations/{id}` | Get conversation history |
| `PUT` | `/api/chat/conversations/{id}/title` | Update conversation title |
| `POST` | `/api/chat/conversations/{id}/vote` | Submit feedback on a response |
| `POST` | `/api/chat/conversations/{id}/switch-agent` | Switch to a different agent mid-conversation |

### Agents

| Method | Endpoint | Description |
| --- | --- | --- |
| `GET` | `/api/agents` | List all agents in the workspace |
| `GET` | `/api/agents/{id}` | Get agent details |
| `POST` | `/api/agents` | Create an agent |
| `POST` | `/api/agents/batch` | Create multiple agents at once |
| `PUT` | `/api/agents/{id}` | Update an agent |
| `DELETE` | `/api/agents/{id}` | Delete an agent |
| `POST` | `/api/agents/{id}/test` | Run capability test on an agent |
| `POST` | `/api/agents/{id}/feedback` | Submit feedback to improve an agent |
| `GET` | `/api/agents/{id}/usage` | Get token usage and cost stats for an agent |

### Missions

| Method | Endpoint | Description |
| --- | --- | --- |
| `POST` | `/api/missions` | Create a new mission |
| `GET` | `/api/missions` | List active missions |
| `GET` | `/api/missions/{id}` | Get mission detail (tasks + events) |
| `POST` | `/api/missions/{id}/approve` | Approve a mission plan |
| `POST` | `/api/missions/{id}/reject` | Reject a mission plan |
| `POST` | `/api/missions/{id}/pause` | Pause a running mission |
| `POST` | `/api/missions/{id}/resume` | Resume a paused mission (optional budget increase) |
| `POST` | `/api/missions/{id}/cancel` | Cancel a mission |
| `GET` | `/api/missions/{id}/events` | Paginated event timeline |
| `GET` | `/api/missions/{id}/costs` | Task cost breakdown |
| `GET` | `/api/missions/archived` | List archived missions with search |
| `POST` | `/api/missions/{id}/save-as-routine` | Convert completed mission to playbook |
| `GET` | `/api/missions/stats` | Workspace-wide mission statistics |

### Documents & Knowledge

| Method | Endpoint | Description |
| --- | --- | --- |
| `GET` | `/api/documents` | List documents with filtering and pagination |
| `POST` | `/api/documents/upload` | Upload and process a document |
| `GET` | `/api/documents/{id}` | Get document metadata |
| `GET` | `/api/documents/{id}/download` | Download via presigned S3 URL |
| `GET` | `/api/documents/{id}/content` | Get document text content |
| `DELETE` | `/api/documents/{id}` | Delete a document |
| `POST` | `/api/documents/search` | Semantic search across document chunks |
| `POST` | `/api/documents/rag` | RAG context retrieval optimised for LLM augmentation |
| `POST` | `/api/documents/{id}/reprocess` | Re-chunk and re-embed a document |
| `POST` | `/api/documents/reprocess-all` | Bulk re-processing with semantic chunking |
| `GET` | `/api/documents/queue-status` | Processing queue depth |
| `GET` | `/api/documents/analytics` | Document usage statistics |

### Knowledge Graph

| Method | Endpoint | Description |
| --- | --- | --- |
| `GET` | `/api/knowledge-graph/entities` | List entities with type filtering |
| `GET` | `/api/knowledge-graph/entities/{id}` | Entity detail and relationships |
| `GET` | `/api/knowledge-graph/search` | Full-text entity search |
| `GET` | `/api/knowledge-graph/visualise` | Graph visualisation data |
| `GET` | `/api/knowledge-graph/path` | Find connection path between two entities |
| `POST` | `/api/knowledge-graph/rebuild` | Trigger graph rebuild |
| `GET` | `/api/knowledge-graph/stats` | Entity and relationship counts |

### Database Knowledge (NL2SQL)

| Method | Endpoint | Description |
| --- | --- | --- |
| `GET` | `/api/database-knowledge` | List database knowledge sources |
| `POST` | `/api/database-knowledge` | Add a new database source |
| `POST` | `/api/database-knowledge/{id}/query` | Execute natural language query |
| `GET` | `/api/database-knowledge/{id}/schema` | Browse database schema |
| `POST` | `/api/database-knowledge/{id}/introspect` | Re-introspect schema |
| `GET` | `/api/database-knowledge/{id}/templates` | List query templates |
| `POST` | `/api/database-knowledge/{id}/training` | Add NL2SQL training example |
| `GET` | `/api/database-knowledge/{id}/benchmarks` | Run accuracy benchmark |
| `GET` | `/api/database-knowledge/{id}/audit` | Query audit log |

### Workflows & Playbooks

| Method | Endpoint | Description |
| --- | --- | --- |
| `GET` | `/api/workflows` | List all playbooks |
| `POST` | `/api/workflows` | Create a playbook |
| `GET` | `/api/workflows/{id}` | Get playbook details |
| `PUT` | `/api/workflows/{id}` | Update a playbook |
| `DELETE` | `/api/workflows/{id}` | Delete a playbook |
| `POST` | `/api/workflows/{id}/run` | Execute a playbook (returns SSE stream) |
| `GET` | `/api/workflow-recipes` | Browse marketplace playbooks |
| `POST` | `/api/workflow-recipes/{id}/install` | Install a marketplace playbook |
| `POST` | `/api/workflow-recipes/{id}/submit` | Submit playbook to marketplace |
| `GET` | `/api/workflow-recipes/categories` | List playbook categories |
| `GET` | `/api/workflow-recipes/featured` | Featured marketplace playbooks |
| `GET` | `/api/execution-history` | Paginated execution history |
| `GET` | `/api/execution-history/{id}` | Execution detail with pipeline stages |

### Memory

| Method | Endpoint | Description |
| --- | --- | --- |
| `POST` | `/api/memory/store` | Store a memory |
| `GET` | `/api/memory/retrieve` | Retrieve memories by query |
| `POST` | `/api/memory/augment` | Add external knowledge to memory |
| `POST` | `/api/memory/consolidate` | Trigger memory consolidation |
| `GET` | `/api/memory/stats` | Memory system statistics |

### Tools

| Method | Endpoint | Description |
| --- | --- | --- |
| `GET` | `/api/tools` | List all available tools and integrations |
| `GET` | `/api/tools/categories` | Tool categories |

### Analytics

| Method | Endpoint | Description |
| --- | --- | --- |
| `GET` | `/api/analytics/overview` | Workspace metrics summary |
| `GET` | `/api/analytics/costs` | LLM cost breakdown |
| `GET` | `/api/analytics/agents` | Per-agent analytics |
| `GET` | `/api/analytics/real/dashboard` | Enhanced real-time dashboard metrics |
| `GET` | `/api/analytics/real/system-load` | 24-hour system load trend |
| `GET` | `/api/analytics/real/cost-per-execution` | Cost per execution from real data |
| `GET` | `/api/analytics/real/capacity-alerts` | Predictive capacity alerts |
| `GET` | `/api/analytics/real/bottlenecks` | Resource bottleneck detection |
| `GET` | `/api/llm-analytics` | Detailed LLM usage analytics |

### Workspaces

| Method | Endpoint | Description |
| --- | --- | --- |
| `GET` | `/api/workspaces/current` | Get current workspace context |
| `GET` | `/api/workspaces/members` | List workspace members |
| `GET` | `/api/workspaces/settings/orchestrator` | Get orchestrator soul/personality/heartbeat |
| `PUT` | `/api/workspaces/settings/orchestrator` | Save orchestrator settings |
| `GET` | `/api/workspaces/settings/byok` | Get BYOK preferences |
| `PUT` | `/api/workspaces/settings/byok` | Save BYOK preferences |
| `GET` | `/api/workspaces/settings/integrations` | Get integration credentials (masked) |
| `PUT` | `/api/workspaces/settings/integrations` | Save integration credentials |

### Personas

| Method | Endpoint | Description |
| --- | --- | --- |
| `GET` | `/api/personas` | List available personas |
| `POST` | `/api/personas` | Create a persona |
| `PUT` | `/api/personas/{id}` | Update a persona |
| `DELETE` | `/api/personas/{id}` | Delete a persona |

### Plugins & Skills

| Method | Endpoint | Description |
| --- | --- | --- |
| `GET` | `/api/agent-plugins/{agent_id}` | List plugins for an agent |
| `POST` | `/api/agent-plugins/{agent_id}` | Assign plugin to an agent |
| `DELETE` | `/api/agent-plugins/{agent_id}/{plugin_id}` | Remove plugin from agent |
| `GET` | `/api/workspace-plugins` | List workspace plugins |
| `GET` | `/api/workspace-skills` | List workspace skills |
| `POST` | `/api/workspace-skills` | Add a skill to the workspace |
| `GET` | `/api/marketplace-plugins` | Browse marketplace plugins |

### Voice

| Method | Endpoint | Description |
| --- | --- | --- |
| `POST` | `/api/chat/voice` | Send voice message |
| `GET` | `/api/chat/voice/health` | Voice service health check |
| `GET` | `/api/voice-profiles` | List voice profiles |
| `POST` | `/api/voice-profiles` | Create a voice profile |

### Widgets (Embedded SDK)

| Method | Endpoint | Description |
| --- | --- | --- |
| `POST` | `/api/widgets/chat` | Widget chat endpoint (SSE streaming) |
| `GET` | `/api/widgets/documents` | Widget document access |
| `GET` | `/api/widget-memory` | Widget memory endpoints |

### System

| Method | Endpoint | Description |
| --- | --- | --- |
| `GET` | `/api/health` | Health check |
| `GET` | `/api/system/metrics` | System metrics |
| `GET` | `/api/models` | List available models |
| `GET` | `/api/cache` | Cache management |

## Request/response examples

### Send a chat message

```http
POST /api/chat
Content-Type: application/json
Authorization: Bearer <token>
X-Workspace-ID: <workspace_id>

{
  "message": "Review the login component for XSS vulnerabilities",
  "conversation_id": "conv_abc123",
  "agent_id": null
}
```

Response: Server-Sent Events stream

```
data: {"type": "token", "content": "I'll review the login"}
data: {"type": "token", "content": " component for XSS..."}
data: {"type": "tool_call", "name": "github_get_file", "args": {"path": "src/login.tsx"}}
data: {"type": "done", "agent": "Sentinel", "tokens": {"input": 1234, "output": 567}}
```

### Create an agent

```http
POST /api/agents
Content-Type: application/json
Authorization: Bearer <token>
X-Workspace-ID: <workspace_id>

{
  "name": "API Tester",
  "category": "qa_engineer",
  "description": "Tests REST API endpoints for correctness and edge cases",
  "model_provider": "openrouter",
  "model_name": "anthropic/claude-sonnet-4-20250514",
  "temperature": 0.3,
  "persona": "technical"
}
```

### Semantic document search

```http
POST /api/documents/search
Content-Type: application/json
Authorization: Bearer <token>
X-Workspace-ID: <workspace_id>

{
  "query": "rate limiting implementation",
  "top_k": 5,
  "min_similarity": 0.7
}
```

## Error handling

All API errors follow a consistent format:

```json
{
  "detail": "Human-readable error message",
  "status_code": 400
}
```

Common status codes:

| Code | Meaning |
| --- | --- |
| `400` | Bad request — check your input |
| `401` | Unauthorized — invalid or missing token |
| `403` | Forbidden — insufficient permissions |
| `404` | Not found — resource doesn't exist |
| `422` | Validation error — request body schema mismatch |
| `429` | Rate limited — too many requests |
| `500` | Server error — contact support |

## Pagination

List endpoints support pagination via query parameters:

```http
GET /api/documents?page=1&limit=20&sort=created_at&order=desc
```

Response includes pagination metadata:

```json
{
  "items": [...],
  "total": 142,
  "page": 1,
  "limit": 20,
  "pages": 8
}
```

## Streaming responses

Chat and playbook execution endpoints return Server-Sent Events (SSE). Connect with any SSE-compatible client:

```javascript
const eventSource = new EventSource('/api/chat', {
  method: 'POST',
  headers: { 'Authorization': 'Bearer <token>' },
  body: JSON.stringify({ message: 'Hello' })
});

eventSource.onmessage = (event) => {
  const data = JSON.parse(event.data);
  console.log(data.content);
};
```

The SSE stream is compatible with the **Vercel AI SDK** for seamless frontend integration.

{% hint style="info" %}
For the complete endpoint list with request/response schemas, use the interactive Swagger docs at `/docs` on your instance. The Swagger UI lets you test endpoints directly from your browser.
{% endhint %}
