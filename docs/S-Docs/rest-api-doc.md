---
layout: single
title: REST API
permalink: /S-Docs/rest-api/
toc: true
sidebar: S-Docs
---

## AcmeTasker REST API

The AcmeTasker REST API allows programmatic access to tasks, projects, and user data. All endpoints are under the base URL:

```
https://api.acmetasker.com/v1
```

## Authentication

Requests require an API key provided in the Authorization header:

```
Authorization: Bearer YOUR_API_KEY
```

### Error Codes

| Code | Meaning |
|------|---------|
| 400  | Bad Request |
| 401  | Unauthorized |
| 403  | Forbidden |
| 404  | Not Found |
| 500  | Internal Server Error |

## Common Parameters

- limit – number of items per page (default 25)
- offset – pagination offset
- sort – field to sort by (e.g. dueDate)
- filter – JSON object with filtering criteria

## Endpoints

### GET /tasks

Fetch a list of tasks.

**Query Parameters:** status, assignee, projectId

**Response:** 200 OK
```json
{
  "tasks": [
    {"id": 1, "title": "Sample task", "status": "open"}
  ],
  "pagination": {"limit":25, "offset":0, "total":100}
}
```

### POST /tasks

Create a new task.

**Body:**
```json
{
  "title": "New task",
  "description": "Details here",
  "dueDate": "2024-01-01",
  "projectId": 5
}
```

**Response:** 201 Created
```json
{"id": 42, "message": "Task created"}
```

### GET /tasks/{id}

Retrieve a single task by ID.

**Response:** 200 OK
```json
{"id":42, "title":"New task", "status":"open"}
```

### PUT /tasks/{id}

Update an existing task. Submit only fields to change.

**Body example:**
```json
{"status": "completed"}
```

### DELETE /tasks/{id}

Delete a task.

**Response:** 204 No Content

### /projects

Endpoints are analogous to /tasks and support the same query parameters.

### Webhooks

Register a callback URL via POST /webhooks to receive events such as task.created or task.updated.

## Versioning

All endpoints are prefixed with /v1; breaking changes will occur in /v2.

## Rate Limits

Requests are limited to 100 per minute per API key. Exceeding this returns 429 Too Many Requests.

## Example cURL

```
curl -H "Authorization: Bearer TOKEN" \
  https://api.acmetasker.com/v1/tasks?limit=10
```

Further details and SDKs for Python, JavaScript, and Java are available on the developer portal.
