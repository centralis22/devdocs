---
title: "API Overview"
description: "API Overview."
lead: "API Overview."
date: 2022-09-24T00:00:00+00:00
lastmod: 2022-09-24T00:00:00+00:00
draft: false
images: []
menu:
  docs:
    parent: "api"
weight: 310
toc: true
---

## WebSocket

WebSocket, wrapped under SockJS, without STOMP protocol, is used for communication 
between backend and frontend. It is chosen to facilitate real-time communication 
of Admin/Instructors -> Server -> Teams. STOMP is disregarded because 
[stompjs](https://github.com/stomp-js/stompjs) 
is in maintenance mode.

The backend implementation is split among the following files:

- `config/WebSocketConfig`
- `(TBD) handler/GreetingHandler`

The frontend requires the following code:

```javascript
// Deployment address TBD.
var sock = new SockJS('http://localhost:8080/greeting');

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

See 
[Github dummy implementation](https://stackoverflow.com/questions/27158106/websocket-with-sockjs-spring-4-but-without-stomp).

## CORS

To bypass CORS with Spring, refer to 
[Spring Docs 25.2.6 WebSocket: Configuring allowed origins](https://docs.spring.io/spring-framework/docs/4.2.x/spring-framework-reference/html/websocket.html)
and 
[setAllowedOriginPatterns()](https://stackoverflow.com/questions/66060750/cors-error-when-using-corsfilter-and-spring-security).
