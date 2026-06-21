---
# markdownlint-disable
# vale off
# tags used by just-the-docs theme
layout: default
nav_order: 1
has_children: true
has_toc: false
# tags used by AI files
description: "Information about the `books` resource"
topic_type: reference
tags: 
    - api
categories: 
    - api-reference
ai_relevance: high
importance: 8
prerequisites: []
related_pages: 
    - /tutorials/add-a-new-book
examples: []
api_endpoints:
    - /books
version: "v1.0"
last_updated: "2026-06-20"
# vale  on
# markdownlint-enable
---

# `books` resource

<!-- vale write-good = NO -->
<!-- vale Google.Passive = NO -->
<!-- vale Google.Headings = NO -->
<!-- vale Google.Parens = NO -->
<!-- vale Google.Acronyms = NO -->

Base endpoint:

```shell
{server_url}/books
```

Contains information about books stored in Book Buddy.

## Resource properties

Sample `books` resource

```json

{
    "id": 1,
    "title": "How to be happy",
    "author": "Ruskin Bond",
    "genre": "Memoir",
    "readingStatus": "0 %",
    "rating": "0"
}
```

<!-- markdownlint-disable MD013 -->

| Property name | Type | Description | Required |
| ------------- | ----------- | ----------- | ------- |
| `id` | number | The unique ID of the book | System-generated |
| `title` | string | The title of the book | Yes |
| `author` | string | The name of the author | Yes |
| `genre` | string | The genre. Best practice is to use  the [Library of Congress Genre/Form Terms](https://id.loc.gov/authorities/genreForms.html) | No |
| `readingStatus` | string | The percentage of completion in the format `70 %`. | No |
| `rating` | string | User-defined rating as text or number | No |

<!-- markdownlint-enable MD013 -->

## READ

<!-- vale Vale.Terms = NO -->

* [Get all books _(coming soon)_](#resource-properties)
* [Get book by ID _(coming soon)_](#resource-properties)

## CREATE

<!-- vale Vale.Terms = NO -->

* [Create a book _(coming soon)_](#resource-properties)
