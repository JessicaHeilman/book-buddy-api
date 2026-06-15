---
# markdownlint-disable
# vale off
layout: default
nav_order: 2
description: Describes how to configure your local computer to run a local instance of the Book Buddy API.
topic_type: tutorial
tags: 
    - introduction
categories: 
    - tutorial
ai_relevance: high
importance: 9
prerequisites: []
related_pages: []
examples: []
api_endpoints: []
version: "v1.0"
last_updated: "2026-06-14"
# vale on
# markdownlint-enable
---

# Before you start a tutorial

These are the steps you must do before you can run
the tutorials for the **Book Buddy API**.

Expect this preparation to take about 20 minutes to complete.

## Preparing for the tutorials

To complete the tutorials in this section, you need the following.
You might want to open the links in separate browser tabs before you start installing the software.

<!-- vale Google.Acronyms = NO -->

- A [GitHub account](https://github.com)
- A development system running a current version or a
long-term support, also known as _LTS_, version of the Windows, MacOS, or Linux operating system.
- The following software on your development system:
    - [Git, command line](https://docs.github.com/en/get-started/quickstart/set-up-git)
    - [GitHub Desktop](https://desktop.github.com). This is optional, but recommended.
    - A fork of the [Book Buddy API repository](https://github.com/JessicaHeilman/book-buddy-api)
    - A [current or LTS version of `node.js`](https://nodejs.org/en/download)
    - Version 0.17.4 of [json-server](https://www.npmjs.com/package/json-server/v/0.17.4)
    - A current copy of the database file. You can get this by syncing your fork.

        **Tip**: if you're using a fork of the repository, create a working branch in which to
        do your tutorials. Create a new branch for each tutorial to prevent a mistake in one from
        affecting your work in another.
    - The [Postman desktop app](https://www.postman.com/downloads/).
        Because you run the **Book Buddy API** on your development system with an `http://localhost`
        host name, the web-version of Postman can't perform the exercises.

<!-- vale Google.Acronyms = YES -->

## Test your development system

To test your development system:

1. Create and checkout a test branch of your fork of the Book Buddy API repository.
    Your `GitHub repository workspace` is the directory that contains your fork of
    the `book-buddy-api` repository.

    ```shell
    cd <your GitHub repository workspace>
    ls
    # (see the book-buddy-api directory in the list)
    cd book-buddy-api
    git checkout -b tutorial-test
    json-server -w book-buddy-api-source.json
    ```

    If you installed the software correctly, you should see
    the service start and display the URL of the service: `http://localhost:3000`.

2. Make a test call to the service.

    ```shell
    curl http://localhost:3000/books
    ```

3. If the service is running correctly, you should see a list of books from the service,
    such as in this example.

    ```json
    [
        {
            "title": "Pride and Prejudice",
            "author": "Jane Austen",
            "genre": "Romance",
            "readingStatus": "completed",
            "id": 1
        },
        {
            "title": "The Hobbit",
            "author": "J.R.R. Tolkien",
            "genre": "Fantasy",
            "readingStatus": "reading",
            "id": 2
        },
        ...
    ]
    ```

You should see the list of books.
If you receive an error in any step of the procedure, investigate and correct the error before continuing.
Some common situations that cause errors include:

1. You mistyped a command.
2. You aren't in the correct directory.
3. A required software component didn't install correctly.
4. A required software component isn't up to date.

If you see the list of books from the service, you're ready to do
the [Tutorials](tutorials.md).
