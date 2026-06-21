---
# markdownlint-disable
# vale off
# tags used by just-the-docs theme
layout: default
parent: books resource
nav_order: 1
# tags used by AI files
description: GET all from Book Buddy
topic_type: reference
tags:
    - api
categories:
    - api-reference
ai_relevance: high
importance: 7
prerequisites:
    - /api/books
related_pages: []
examples:
    - GET /books
test:
    test_apps:
        - json-server@0.17.4
    server_url: localhost:3000
    local_database: /api/book-buddy-api-source.json
    testable:
        - GET example
api_endpoints: 
    - /books
version: "v1.0"
last_updated: "2026-06-20"
# vale  on
# markdownlint-enable
---

# Get all books

Returns an array of [`books`](books.md) objects that contains all books entered in Book Buddy.

[Jump to examples](#examples)

## Endpoint

```shell
{server_url}/books
```

## Parameters

None

## Request headers

| Header | Value | Required |
| ------ | ----- | -------- |
| `Accept` | `application/json` | No |
| `Authorization` | `Bearer {token}` | Yes |

## Request body

None

## Response body

```json
[
    {
        "id": 1,
        "title": "How to be happy",
        "author": "Ruskin Bond",
        "genre": "Memoir",
        "readingStatus": "0 %",
        "rating": "0"
    },
    {
        "id": 2,
        "title": "Verity",
        "author": "Collen Hoover",
        "genre": "Thriller",
        "readingStatus": "70 %",
        "rating": "5"
    },
    ...
]
```

## Examples

### `GET` example request

```bash
curl -G -H "Accept: application/json" \
    --url "http://localhost:3000/books"
```

#### `GET` example response

```json
[
    {
        "id": 1,
        "title": "How to be happy",
        "author": "Ruskin Bond",
        "genre": "Memoir",
        "readingStatus": "0 %",
        "rating": "0"
    },
    {
        "id": 2,
        "title": "Verity",
        "author": "Collen Hoover",
        "genre": "Thriller",
        "readingStatus": "70 %",
        "rating": "5"
    },
    ...
]
```

## Response status

| HTTP status value | Description |
| ------------- | ----------- |
| 200 | **Success:** Requested data returned successfully |
| 400 | Bad request — the request was malformed or contains invalid parameters |
| 401 | Unauthorized — authentication is required or credentials are invalid | 
| 403 | Forbidden — the authenticated user does not have permission |
| 404 | Not found — the requested resource was not found |
| 429 | Too many requests — rate limit exceeded |
| 500 | Internal server error — an unexpected server error occurred|
| ECONNREFUSED | Service is offline. Start, or restart the service and try again. |
