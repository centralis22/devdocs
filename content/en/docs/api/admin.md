---
title: "Admin"
description: "API for admin users."
lead: "API for admin users."
date: 2022-09-24T00:00:00+00:00
lastmod: 2022-09-24T00:00:00+00:00
draft: false
images: []
menu:
  docs:
    parent: "api"
weight: 350
toc: true
---

## create_session

:warning: Subject to change.

The instructor creates a new session.

```json
{
    // Request
    "request": "create_session",
    "content": "",
}
```

```json
{
    // Respond
    "content": <int>,
}
```

- `status_code`: On success, 200.
- `content`: On success, server generated session ID.

## advance_stage

:warning: Subject to change.

The instructor advances the simulation to the next stage for all users. For 
example, from *Welcome* to *Discussion #1*.

```json
{
    // Request
    "request": "advance_stage",
    "content": <int>,
}
```

- `content`: -1, advance to next stage. Else, advance to a specific stage.

```json
{
    // Broadcast
    "broadcast": "advance_stage",
    "content": <int>,
}
```

- `content`: Same as request.
