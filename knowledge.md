---
title: Knowledge
cover: assets/social-card.jpeg
---

Manage **Sources** (docs/repos), explore **Documents**, and search the **Code Graph**.

## Sources
Add, index, and delete sources; track status and size.

**API**  
> **Authentication**  
> All API calls require headers:  
> ```http
> X-API-Key: <your_key>
> Authorization: Bearer <your_token>
> ```

- `GET /api/sources`  
- `POST /api/sources` (body: `{"name":"Repo","type":"git","config":{"url":"..."}}`)  
- `POST /api/sources/{id}/index`  
- `DELETE /api/sources/{id}`

## Documents
Search and filter documents; reindex when schemas change.

**API**  
- `GET /api/documents?source_id=&q=&limit=&offset=&tag=`  
- `POST /api/documents/reindex` (body: `{"source_id":"..."}`)

## Code Graph
Search project code and emit a compact **CODE slot** block.

**API**  
- `POST /api/codegraph/index` (body: `{"project":"automatos-ai","root_dir":"/repo"}`)  
- `GET /api/codegraph/search?project=&q=&limit=`
