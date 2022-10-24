---
title: "security"
description: "security package"
lead: "security package"
date: 2022-10-16T00:00:00+00:00
lastmod: 2022-10-23T00:00:00+00:00
draft: false
images: []
menu:
  docs:
    parent: "backend"
weight: 600
toc: true
---

## Security Design

Current design is loosely based on Spring Security. Spring Security only 
supports HTTP, and WebSocket w/ STOMP. 

:memo: It is possible to adapt our application to use HTTP, since 
WebSocket does require an initial HTTP handshake. However, it will 
require considerable research.

But no no no.

## Security flow

[draw.io (right click, save)](securityflow.drawio)

![Flow](securityflow.drawio.png)
