---
# markdownlint-disable
# vale off
# tags used by just-the-docs theme
layout: default
parent: books resource
nav_order: 3
# tags used by AI files
description: GET the `books` resource with the specified ID from the service
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
    - GET /books/{id}
test:
    test_apps:
        - json-server@0.17.4
    server_url: localhost:3000
    local_database: /api/book-buddy-api-source.json
    testable:
        - GET example / 200
api_endpoints: 
    - GET /books{id}
version: "v1.0"
last_updated: "2026-06-20"
# vale  on
# markdownlint-enable
---

# Get a book by ID

Returns an array of  [`books`](books.md) object that contains only
the book specified by the `id` parameter, if it exists.

[Jump to examples](#examples)

## Endpoint

```shell
{server_url}/books/{id}
```

## Parameters

| Name | Type | Value | Description |
| ----- | ------ | ------ | ------------ |
| `id` | path | number | The record ID of the `book` resource to return |

## Request headers

| Header | Value | Required |
| ------ | ----- | -------- |
| `Accept` | `application/json` | No |
| `Authorization` | `Bearer {token}` | Yes |

## Request body

None

## Response body

Returns a [`books` resource](./books.md#resource-properties)

## Examples

### `GET` example request

```bash
curl -G -H "Accept: application/json" \
    --url "http://localhost:3000/books/2"
```

#### `GET` example response

```json
{
    "id": 2,
    "title": "Verity",
    "author": "Collen Hoover",
    "genre": "Thriller",
    "readingStatus": "70 %",
    "rating": "5"
}
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
