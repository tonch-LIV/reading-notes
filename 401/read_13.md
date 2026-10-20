# 401_Read_13 - Rooms & Namespaces

## [Socket.io Chat](https://socket.io/get-started/chat/)

The socket.io chat example demonstrates how a basic real-time messaging app would work.  
It is a simple web page built using node.js and express that adds socket.io to establish a connections between browser and server.  

A user would submit a message -> the browser sends the event to the server -> the server receives that event and broadcasts the message to the connected clients.  

- The browser establishes a connection with the node.js server; **clinet-server comms.**
- the server listens for events; `connection` and `chat.message`; **event listeners**,
- clients send messages using **`socket.emit()`**,
- server distributes messages uusing `io.emit()`; **broadcasting**,
- ways to handle missed messages should the connection be temporarily be disrupted; **connection recovery**

### Answers.1

1. Explain to a non-technical recruiter what the Chat Example does.
    - Chat is exemplified through the use of an instant messaging app that allows multiple users to connect and communicate concurrently w/o the need to refresh their browser to see/receive updated messages.  
2. What proof of life are we getting on the backend from the above app?
    - throught the use of `console.log` messages printed on the terminal / browser dev tools.  
3. Socket.IO gives us the _____ method to send an event to everyone.
    - `io.emit()`; broadcasts an event to all connected clients in the namespace, incuding originating client from whence the message came.  
4. What flag would you use if you want to send a message to everyone except for a certain emitting socket?
    - `broadcast`; `socket.broadcast.emit()` sends an event to ***other*** connected clients in that ***same namespace***, except to the originator.

## [Rooms](https://socket.io/docs/v4/rooms)

Rooms allow for organization of connected clients from a namespace into groups. Rather than broadcasting, where every client connected is made aware of every event occuring; the server sends events only to clients belonging to the designated room.  

A Socket can join multiple rooms at the same time; rooms are managed by the server, not directly by the client.  

### Answers.2

1. What is a room and how might a room be useful?
    - think subnet/vlan; a server-side group of clients.
2. How do you join a room? how do you leave a room?
    - `socket.join()` and `socket.leave()`

## [Namespaces](https://socket.io/docs/v4/namespaces/)

Allow for apps to separate different type of comms into independent channels while still sharing the same underlying connection.  

Rooms group users for targeted messaging;  
namespaces organize different sections/functionalities of an app.  
(i.e. separation of general user  and administrative functions for a website.)  

namespaces can;

- handle its own connections and events through **separate communication channels**,  
- listen for different, **independent event handlers**,
- contain their own **separate rooms**,
- apply their own authen/authoriz **middleware** checks,
- share one underlying (**multiplexed**) connection.

### Answers.3

1. What is a Namespace and what does it allow you to do?
    - a separate comm. channel within a socket.io app that allows devs to organize parts of said app per events, as well as control which clients can access specific functionality.
2. Each namespace potentially has its own what? (hint: 3 things)
    - **event handlers** - fucntions that respond to events.
    - **rooms** - group(s) of connected clients.
    - **middleware** - functions that authorize/validate connections before allowing access.
3. Discuss a possible use case for separate `namespaces`.
    - separation of responsibilities / permissions between regular users and those with admin rights.

## Bookmark and Review

- [Socket.io Emit Cheatsheet](https://socket.io/docs/v4/emit-cheatsheet/)
  - quick reference for seding events to different recipients; individual, broadcasting, exclude sender, rooms / namespaces, acks(callbacks & promises), timeouts, and chaining.  

## Things to Learn More About

- when to use `.broadcast.emit()` vs just `io.emit()`.
- use of rooms, and namespaces for bigger scope.  
- practice creating events -> sending events through net -> control who receives