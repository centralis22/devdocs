---
title: "API Basics"
description: "Standardized format and requirements for all frontend to server transmissions."
lead: "Standardized format and requirements for all frontend to server transmissions."
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

## Metadata and credentials

:warning: Subject to change.

Credentials needs to be preserved across pages. The application will either be 
designed as an SPA, or a cookie will be saved. Password encryption is not used in 
this stage of development.

:o: All requests from the frontend to the server must contain the credential section.

:o: All requests from the frontend to the server must contain at most one action.

### Team

```json
{
    "session": xxx,
    "teamName": xxx,
    // Additional content
}
```

### Admin/Instructor

```json
{
    "session": (Optional) xxx,
    "userName": xxx,
    "password": xxx,
    // Aditional content
}
```
