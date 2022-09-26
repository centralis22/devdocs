---
title: "API Basics"
description: "Standardized format and requirements for all communications."
lead: "Standardized format and requirements for all communications."
date: 2022-09-24T00:00:00+00:00
lastmod: 2022-09-24T00:00:00+00:00
draft: false
images: []
menu:
  docs:
    parent: "api"
weight: 320
toc: true
---

## Client requests

:warning: Subject to change.

This metadata must be provided in each frontend-to-server transmission. Password 
encryption is not used in this stage of development.

:o: All requests from the frontend to the server must contain at most one action.

```json
{
    "user": (See below),
    "session": <int>,
    "request_id": <int>,
    // Request
}
```

- `session`: Required when joining a session. Not required when creating a new 
session.
- `request_id`: Requests may be processed out of order because of multithreading. 
If the client requires a request to be executed in order, he must wait for a 
success response, before submitting the next.

### Admin/Instructor

```json
"user": {
    "type": "admin",
    "username": <string>,
    "password": <string>,
}
```

### Team

```json
"user": {
    "type": "team",
    "username": <string>
}
```

## Server responses

:warning: Subject to change.

The server must provide a response for each request. It indicates if the request 
is a success, failure, or other. These responses are analogous to HTTP reponses.

```json
{
    "message_type": "respond",
    "respond_id": <int>,
    "status_code": <int>,
    "status_message": <string>,
    // Respond
}
```

## Server broadcasts

:warning: Subject to change.

The server may broadcast a message to all clients. All client must actively listen 
to a broadcast.

```json
{
    "message_type": "broadcast",
    // Broadcast
}
```