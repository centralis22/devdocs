---
title: "All Users"
description: "API for all users."
lead: "API for all users."
date: 2022-10-09T00:00:00+00:00
lastmod: 2022-10-09T00:00:00+00:00
draft: false
images: []
menu:
  docs:
    parent: "api"
weight: 340
toc: true
---

## login

:warning: Subject to change.

All users may login. Password encryption is not used in this stage of development.

```json
{
    // Request
    "request": "login",
    "content": {
        "user_type": "admin/student",
        "user_name": <string>,
        "user_pswd": <string>,
        "session_id": <int>
    },
}
```

- `user_type`: Either admin or student.
- `user_name`: For admin users, their username. For students, their team name, or room name.
- `user_pswd`: For admin users only. Leave blank for students.
- `session_id`: Provide a `session_id` to join a created session. Leave blank for instructors
 when creating a new session. Required for admins and students when joining a session.
