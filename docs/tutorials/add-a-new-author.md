---
# markdownlint-disable
# vale off
# tags used by just-the-docs theme
layout: default
nav_order: 2
parent: Tutorials
# tags used by AI files
description: Add an `authors` resource to the service
topic_type: tutorial
tags:
    - api
categories: 
    - tutorial
ai_relevance: high
importance: 6
prerequisites:
    - /before-you-start-a-tutorial
    - /api/authors
related_pages: []
examples: []
api_endpoints:
    - POST /authors
version: "v1.0"
last_updated: "2026-06-21"
# vale  on
# markdownlint-enable
---

# Tutorial: Add a new author

## What you'll learn

In this tutorial, you learn the operations to call to
add a new author to the Book Buddy database.

Expect this tutorial to take about 15 minutes to complete.

## Before you start

Make sure you've completed the [Before you start a tutorial](../before-you-start-a-tutorial.md)
topic on the development system you'll use for the tutorial.

## Add a new author

To add a new author to the database, you'll use the `POST` method to store the details of
the new [`author`](../api/authors.md) in the service.

In this tutorial, you'll use the Postman app.

To add a new author:

1. Make sure your local service is running. If it's not, start it by using this command.

```shell
    cd <your-github-workspace>/book-buddy-api/api
    json-server -w book-buddy-api-source.json
```

2. Open the Postman app on your desktop.

3. In Postman, create a new request with these values:
    * **METHOD**: POST
    * **URL**: `{{base_url}}/authors`
    * **Headers**:
        * `Content-Type: application/json`
    * **Request body**:
        Change the values of each property for the author you want to add.

```json
        {
            "name": "Thomas Brussig",
            "booksPublished": "4",
            "genreSpeciality": "Satirical literature"
        }
```

4. In the Postman app, choose **Send** to make the request.
5. Check the response body. It should look something like this.

    Note: The names should be the same as you used in
    your **Request body** and the response should include the new author's `id`.

```json
    {
        "id": 6,
        "name": "Thomas Brussig",
        "booksPublished": "4",
        "genreSpeciality": "Satirical literature"
    }
```

After doing this tutorial in Postman, you might like to repeat it in
your favorite programming language. To do this, adapt the values from
the tutorial to the properties and arguments that the language uses to
make REST API calls.