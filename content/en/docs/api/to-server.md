---
title: "To Server"
description: "Frontend to server API."
lead: "Frontend to server API."
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

## Action: advance_stage

:warning: Subject to change.

The instructor requests the simulation to advance to the next stage. 
For example, from *Welcome* to *Discussion #1*.

```json
{
    // Continue from credentials
    "action": "advance_stage",
    "content": xxx,
}
```

If `content` = -1, advance to next stage. Else, advance to a specific stage.

## Action: submit_poll

:warning: Subject to change.

The team submits their team decision poll.

```json
{
    // Continue from credentials
    "action": "submit_poll",
    "content": {
        "poll_no": xxx,
        "response": [xxx, xxx, xxx],
    },
}
```

`poll_no` indicates if this is the first or second poll.

`response` contains an array, the 0th entry is the response to the first question, 
etc.
