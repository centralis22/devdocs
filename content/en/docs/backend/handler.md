---
title: "handler"
description: "handler package"
lead: "handler package"
date: 2022-10-10T00:00:00+00:00
lastmod: 2022-10-10T00:00:00+00:00
draft: false
images: []
menu:
  docs:
    parent: "backend"
weight: 300
toc: true
---

## WebSocketAPIHandler

All WebSocket connections to the `/api` endpoint will be routed to 
`WebSocketAPIHandler`. It is the first layer in client-to-server communication.

Spring exposed methods `afterConnectionEstablished()` and 
`afterConnectionClosed()` are used to keep track of existing connections.
