# API Reference

## Authentication
All requests must include:
```
X-API-Key: YOUR_KEY
Authorization: Bearer YOUR_TOKEN
```

## Agents
- `GET /api/agents`
- `POST /api/agents`
- `GET /api/agents/{id}`
- `PUT /api/agents/{id}`
- `DELETE /api/agents/{id}`

## Workflows
- `GET /api/workflows`
- `POST /api/workflows`
- `GET /api/workflows/{id}`
- `PUT /api/workflows/{id}`
- `DELETE /api/workflows/{id}`

## Policies
- `GET /api/policy/{id}`
- `PUT /api/policy/{id}`
- `POST /api/policy/{id}/assemble`

## Knowledge
- `GET /api/sources`
- `POST /api/sources`
- `POST /api/sources/{id}/index`
- `DELETE /api/sources/{id}`
- `GET /api/documents`
- `POST /api/codegraph/search`

## Playbooks
- `GET /api/playbooks`
- `POST /api/playbooks/mine`
- `POST /api/playbooks/promote`
