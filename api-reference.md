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

### System

| Method | Endpoint | Description |
| --- | --- | --- |
| `GET` | `/api/health` | Health check |
| `GET` | `/api/system/metrics` | System metrics |

### Agents

| Method | Endpoint | Description |
| --- | --- | --- |
| `GET` | `/api/agents` | List all agents |
| `GET` | `/api/agents/{id}` | Get agent details |
| `POST` | `/api/agents` | Create an agent |
| `PUT` | `/api/agents/{id}` | Update an agent |
| `DELETE` | `/api/agents/{id}` | Delete an agent |

### Chat

| Method | Endpoint | Description |
| --- | --- | --- |
| `POST` | `/api/chat` | Send a message (SSE streaming response) |
| `GET` | `/api/chat/conversations` | List conversations |
| `GET` | `/api/chat/conversations/{id}` | Get conversation history |

### Documents

| Method | Endpoint | Description |
| --- | --- | --- |
| `GET` | `/api/documents` | List documents |
| `POST` | `/api/documents/upload` | Upload a document |
| `DELETE` | `/api/documents/{id}` | Delete a document |
| `POST` | `/api/documents/search` | Semantic search |

### Workflows / Recipes

| Method | Endpoint | Description |
| --- | --- | --- |
| `GET` | `/api/workflows` | List recipes |
| `POST` | `/api/workflows` | Create a recipe |
| `POST` | `/api/workflows/{id}/run` | Execute a recipe |

### Workspaces

| Method | Endpoint | Description |
| --- | --- | --- |
| `GET` | `/api/workspaces/current` | Get current workspace |
| `GET` | `/api/workspaces/members` | List workspace members |

### Analytics

| Method | Endpoint | Description |
| --- | --- | --- |
| `GET` | `/api/analytics/overview` | Workspace metrics summary |
| `GET` | `/api/analytics/costs` | LLM cost breakdown |
| `GET` | `/api/analytics/agents` | Per-agent analytics |

{% hint style="info" %}
For the complete endpoint list with request/response schemas, use the interactive Swagger docs at `/docs` on your instance.
{% endhint %}
