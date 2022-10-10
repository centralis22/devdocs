---
title: "Team"
description: "API for team users."
lead: "API for team users."
date: 2022-09-24T00:00:00+00:00
lastmod: 2022-09-24T00:00:00+00:00
draft: false
images: []
menu:
  docs:
    parent: "api"
weight: 360
toc: true
---

## submit_poll

:warning: Subject to change.

The team submits their team decision poll.

```json
{
    // Request
    "request": "submit_poll",
    "content": {
        "poll_no": <int>,
        "poll_response": [xxx, xxx, xxx],
    },
}
```

- `poll_no`: 1 if 1st poll, 2 if 2nd poll.
- `poll_response`: An arrary. 0th item is response to 1st question.
