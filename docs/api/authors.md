---
# markdownlint-disable
# vale off
# tags used by just-the-docs theme
layout: default
nav_order: 4
has_children: true
has_toc: false
# tags used by AI files
description: "Information about the `authors` resource"
topic_type: reference
tags: 
    - api
categories: 
    - api-reference
ai_relevance: high
importance: 8
prerequisites: []
related_pages: 
    - /tutorials/add-a-new-author
examples: []
api_endpoints:
    - /authors
version: "v1.0"
last_updated: "2026-06-20"
# vale  on
# markdownlint-enable
---

# `authors` resource

<!-- vale write-good = NO -->
<!-- vale Google.Passive = NO -->
<!-- vale Google.Headings = NO -->
<!-- vale Google.Parens = NO -->
<!-- vale Google.Acronyms = NO -->

Base endpoint:

```shell
{server_url}/authors
```

Contains information about authors stored in Book Buddy.

## Resource properties

Sample `authors` resource

```json

{
    "id": 1,
    "name": "Jojo Moyes",
    "booksPublished": "11",
    "genreSpeciality": "Romance Fiction"
}
```

<!-- markdownlint-disable MD013 -->

| Property name | Type | Description | Required |
| ------------- | ----------- | ----------- | ------- |
| `id` | number | The unique ID of the author | System-generated |
| `name` | string | The author's name | Yes |
| `booksPublished` | string | The number of published books the author has written | No |
| `genreSpeciality` | string | The most common genre of the author's works. Best practice is to use the [Library of Congress Genre/Form Terms](https://id.loc.gov/authorities/genreForms.html) | No |

<!-- markdownlint-enable MD013 -->

## READ

<!-- vale Vale.Terms = NO -->

* [Get all authors _(coming soon)_](#resource-properties)
* [Get author by ID _(coming soon)_](#resource-properties)

## CREATE

<!-- vale Vale.Terms = NO -->

* [Create an author _(coming soon)_](#resource-properties)
