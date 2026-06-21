---
# markdownlint-disable
# vale off
# tags used by just-the-docs theme
layout: default
nav_order: 2
parent: Tutorials
# tags used by AI files
description: Get all `books` resources from Book Buddy
topic_type: tutorial
tags:
    - api
categories: 
    - tutorial
ai_relevance: high
importance: 6
prerequisites:
    - /before-you-start-a-tutorial
    - /api/books
related_pages: []
examples: []
api_endpoints:
    - GET /books
version: "v1.0"
last_updated: "2026-06-21"
# vale  on
# markdownlint-enable
---

# Tutorial: Get all books

## What you'll learn

In this tutorial, you learn the operations to call to
get all books from the Book Buddy database.

Expect this tutorial to take about 15 minutes to complete.

## Before you start

Make sure you've completed the [Before you start a tutorial](../before-you-start-a-tutorial.md)
topic on the development system you'll use for the tutorial.

## Get all books

To get all books from the database, you'll use the `GET` method to retrieve all
[`books`](../api/books.md) resources from the service.

In this tutorial, you'll use the Postman app.

To get all books:

1. Make sure your local service is running. If it's not, start it by using this command.

```shell
    cd <your-github-workspace>/book-buddy-api/api
    json-server -w book-buddy-api-source.json
```

2. Open the Postman app on your desktop.

3. In Postman, create a new request with these values:
    * **METHOD**: GET
    * **URL**: `{{base_url}}/books`
    * **Headers**:
        * `Content-Type: application/json`

4. In the Postman app, choose **Send** to make the request.
5. Check the response body. It should look something like this.

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

After doing this tutorial in Postman, you might like to repeat it in
your favorite programming language. To do this, adapt the values from
the tutorial to the properties and arguments that the language uses to
make REST API calls.