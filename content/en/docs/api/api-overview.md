---
title: "API Overview"
description: "API Technology and Configuration."
lead: "API Technology and Configuration."
date: 2022-09-24T00:00:00+00:00
lastmod: 2022-12-07T00:00:00+00:00
draft: false
images: []
menu:
  docs:
    parent: "api"
weight: 310
toc: true
---

## WebSocket and REST

Frontend-backend communication is done through WebSockets, 
mimicing REST architecture.

For a working backend example, see 
[StackOverflow implementation](https://stackoverflow.com/questions/27158106/websocket-with-sockjs-spring-4-but-without-stomp).

For a working frontend example, use the following code:

```javascript
// Default address: http://localhost:8080/.
var sock = new SockJS('<Enter your address>');

sock.onopen = function() {
    console.log('open');
    sock.send('test');
};

sock.onmessage = function(e) {
    console.log('message', e.data);
};

sock.onclose = function() {
    console.log('close');
};
```
