---
layout: single
title: AcmeTasker REST API
permalink: /S-Docs/AcmeTasker/rest-api/
---

# AcmeTasker REST API

Base URL: `https://api.acmetasker.com/v1`

## Endpoints

### GET /tasks
Fetch all tasks.

### POST /tasks
Create a new task.

### GET /tasks/{id}
Retrieve a single task by ID.

### PUT /tasks/{id}
Update an existing task.

### DELETE /tasks/{id}
Remove a task.

Authentication uses an API key sent in the `Authorization` header.
