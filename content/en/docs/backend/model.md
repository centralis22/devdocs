---
title: "model"
description: "model package"
lead: "model package"
date: 2022-10-16T00:00:00+00:00
lastmod: 2022-10-16T00:00:00+00:00
draft: false
images: []
menu:
  docs:
    parent: "backend"
weight: 400
toc: true
---

## Persisting POJOs

Includes the `Instructor`, `SimUser`, `Team`, etc. See Database.

## SimUser

`SimUser` is a user who is currently connected to the server. It 
represents a client-server connection, that is volatile and actively 
monitored by the program. It is not persisted by the database.
