---
title: "From Server"
description: "Server to frontend API."
lead: "Server to frontend API."
date: 2022-09-24T00:00:00+00:00
lastmod: 2022-09-24T00:00:00+00:00
draft: false
images: []
menu:
  docs:
    parent: "api"
weight: 370
toc: true
---

## Exceptions

Server to frontend transmissions do not contain the credential section.

## Listen: action_response

:warning: Subject to change.

The server may choose to provide a response for a previous action, indicating 
if the action is a success, or failure. These responses are analogous to HTTP 
reponses.

```json
{
    "listen": "action_response",
    "content": {
        "action_id": xxx,
        "status_code": xxx,
        "message": xxx,
    },
}
```

Example: `status_code: 404`, `message: Not found`.

## Listen: advance_stage

:warning: Subject to change.

The server notifies teams to advance to the specified stage.

```json
{
    // Continue from credentials
    "listen": "advance_stage",
    "content": xxx,
}
```

See action page on content.
