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

See Database. Includes:

- `Instructor`
- `SimSession`
- `Survey`
- `Team` 

## SimUser

`SimUser` is a network user who is currently connected to the server 
through a WebSocket. It is a volatile connection, actively monitored 
by the program, and not persisted by the database.

For example, a new `SimUser` is created when a network user accesses 
the website. It is removed when he voluntarily exits the website, or 
when the connection is terminated because of network instability, etc. 
