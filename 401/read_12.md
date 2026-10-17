# 401_Read_12 - Socket.io

- [Web Sockets](#web-sockets)
  - [Answers.1](#answers1)
- [Socket.io Tutorial](#socketio-tutorial)
  - [Answers.2](#answers2)
- [Socket.io vs Web Sockets](#socketio-vs-web-sockets)
  - [Answers.3](#answers3)
- [OSI Model Explained](#video---osi-model-explained)
  - [Answers.4](#answers4)
- [TCP Handshakes Explained](#video---tcp-handshakes-explained)
  - [Answers.5](#answers5)
- [Bookmark & Review](#bookmark-and-review)
- [Things to Learn More About](#thing-to-learn-more-about)

## [Web Sockets](https://en.wikipedia.org/wiki/WebSocket)

WebSockets allow for messages to ve sent by either client(web browser) and/or server over an established connection, w/o the need for a new HTTP request to be made for every exchange (maintains 2-way connection).

Traditional HTTP comms. follow a *request-reponse* comm. pattern, whereas WebSockets establish a persistent connection between the client and server.

- **Full-duplex** - Both clent and erver are able to receive and send messages at the same time over the same connection.
- **Persistent connection** - Connection remains open until either side closes or the connection fails for other reasons.
- **HTTP Handshake** - WebSocket connections initiate with an HTTP request asking to upgrade to WebSocket.
- **Real-time comm.** - Useful for apps like messages, multiplayer games, live sports, etc.

### Answers.1

1. What is a **Web Socket**?
    - A communication protocol that establishes an ongoing, two-way connection between the client and server ().
2. Describe the Web Socket request/response handshake and what happens once the connection is established?
    - Begins w/ HTTP request to upgrade to WebSockets protocol from client to server.
    - If supported, server accepts and responds w/ HTTP `101 Switching Protocols` status.
    - Connection remains open to allow message exchanges until connection is closed.
3. Web Sockets provide a standardized way for the server to send content to a client without first receiving a __ from that client?
    - Request(s)

## [Socket.io Tutorial](https://www.tutorialspoint.com/socket.io/)

A JavaScript library used to facilitate real-time, 2-way comms.  
Builds on **EDP** through allowing apps to emit events and reguster listeners over net. connections.  
Uses Sockets.IO as its transport method, but also compatible with HTTP for failsafe.

- **Server** - Listens to incoming client connections, requests, and manages comms.
- **Client** - Connects to server, sends/receives events.
- **Event(s)** - Messages that comm. between clients and servers.
- **Event Listener(s)** - Functions that execute code when a specific event is received.
- **Broadcasting** - Sending events to multiple connected clients.
- **Automatic reconnection** - After losing connection, Sockets.IO clients can attempt to reconnect.

### Answers.2

1. What does the event handler `io.on()` do?
    - register an event on Sockets.IO server; Listens for `connection` event.
2. Describe some possible proof of life or proof that the code works as expected.
    - console.log / message when connection succeeds.
    - browser(client) establishes connection and content loads.
    - event(s) are received by client and displayed, after being emitted by server.
3. What does `socket.emit()` do?
    - sends a named event to client/other side of connection.

## [Socket.io vs Web Sockets](https://www.educba.com/websocket-vs-socket-io/)

Not interchangeable, both support real-time comms.  
**WebSocket** is the **communication protocol**.  
**Socket.IO** is a **library**; it provides additional features for managing real-time connections.

One does not exist w/o the other(kinda), they compliment one another.  
Sockets.io uses WebSocket (but can also use standard HTTP request) to provide a comm. system.  
WebSocket is the underlying transport

### Answers.3

1. What is the difference between WebSocket and Socket.IO? (think Git and GitHub, or OAuth and Auth0).
    - WebSocket is the protocol used. Sockets.IO is the library that uses WebSockets and adds features (plus an additional protocol).
2. When would you use Socket.IO?
    - messages/chats,
    - collaboration software,
    - multiplayer games,
    - live notifications, etc.
3. When would you use WebSockets?
    - When in need of **direct**, 2-way comms;
      - seensors (temp, movement, humidity, etc.)

## [[Video] - OSI Model Explained](https://www.youtube.com/watch?v=vv4y_uOneC0)

**A**ll  
**P**eople  
**S**eem  
**T**o -  
**N**eed-  
**D**ata -  
**P**rocessing -  
  
**P**lease **D**o **N**ot **T**hrow **S**ausage **P**izza **A**way.  
bits (physical) -> frames (MAC) -> packets (IP) -> segments (TCP/UDP) -> (datagrams +>).  

A framework for understanding how data and info travels across the network. A Model, but TCP/IP (or DoD, 4/5-layer model) the actual in use.

### Answers.4

1. What are a couple of key takeaways from this video?
    - Each alayer is responsible for a different part of transmitting / receiving data.
    - The division of labor makes it it easier to understand and troubleshoot (the method!) when and issue arises.
    - Allows for comms. between different devices and devices on different OS's (no need for IPX, NetBIOS, etc.) due to being a recognized model that follows standardized protocols.
    - Adding to previous points, the division helps clear up where certain protocols reside and do their part.

## [[Video] - TCP Handshakes Explained](https://www.youtube.com/watch?v=xMtP5ZB3wSk)

**SYN, SYN-ACK, ACK**; ***FIN -> 4-way...***  

Transmission Control Protocol.  
The handshake is the method used by two devices to establish a connection before exchanging data.  
The counterpart to its sibling, **UDP*.  

### Answers.5

1. Translate the gist of this video to a non-technical friend.
    - Knock-knock joke. Person knocks, second responds by asking, who's there?"; first answers, then second either opens the door or doesnt.
    - Once both sides acknowledge each other, a connection is established.

## Bookmark and Review

- [Socket.io Documentation](https://socket.io/docs/)
  - official docs; how it works, installation, how to establish comms.
  - conection mgmt, event emission, broadcasting, **rooms**, namespaces, and acks.
  - rooms allow the server to organize clients into groups and send messages to specific groups (~ multicast/anycast vs. broadcast).
- [Socket.io Server API](https://socket.io/docs/server-api)
  - methods available (`.on`, `.emit`, etc.)
- [Socket.io Client API](https://socket.io/docs/client-api)
  - how clients(browsers) connect to Socket.IO server, send events, receive messages, handle connection chnages, etc.
    - udeful in updating a React app's state w/o needing to refresh the state.
- [Socket Testing Tool](https://amritb.github.io/socketio-client-tool/)
  - browser-based tool to help developers test Socket.IO servers e/o bilding a complete frontend.
    - archived Feb.2026; compatability may be limited...

## Thing to Learn More About

- Implementing the use of WebSockets/Sockets.IO
