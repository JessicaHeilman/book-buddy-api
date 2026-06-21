---
# markdownlint-disable
# vale off
layout: default
nav_order: 1
description: Describes the Book Buddy API for a new user
topic_type: overview
tags: 
    - introduction
categories: 
    - tutorial
ai_relevance: high
importance: 9
prerequisites: []
related_pages: 
    - /before-you-start-a-tutorial
    - /tutorials/get-all-books
    - /tutorials/add-a-new-author
examples: []
api_endpoints: []
version: "v1.0"
last_updated: "2026-06-14"
# vale on
# markdownlint-enable
---

# Book Buddy API

Book Buddy is a simple REST API to manage books, reading progress, and author information.

It is intended for avid readers or anyone who would like to manage their personal library,
track their reading progress, and rate books they have read.

## Key features

- Track books you own or want to read
- Monitor reading progress
- Store author information
- Organize books

## Resources

The Book Buddy API has two resources.

- [Books](api/books.md)
- [Authors](api/authors.md)

## Base URL

`http://localhost:3000`

## Authentication

All endpoints require bearer token authentication.

## Next steps

If you're new to Book Buddy, start with [Before you start a tutorial](before-you-start-a-tutorial.md).