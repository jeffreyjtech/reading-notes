# Read 13 - Message Queues

## [Socket.io Chat Example](https://socket.io/get-started/chat/)

The chat application created in this example using a simple HTML page to display the message received by the socket.io-client packaged on the client side.

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Socket.IO chat</title>
    <style>
      body { margin: 0; padding-bottom: 3rem; font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif; }

      #form { background: rgba(0, 0, 0, 0.15); padding: 0.25rem; position: fixed; bottom: 0; left: 0; right: 0; display: flex; height: 3rem; box-sizing: border-box; backdrop-filter: blur(10px); }
      #input { border: none; padding: 0 1rem; flex-grow: 1; border-radius: 2rem; margin: 0.25rem; }
      #input:focus { outline: none; }
      #form > button { background: #333; border: none; padding: 0 1rem; margin: 0.25rem; border-radius: 3px; outline: none; color: #fff; }

      #messages { list-style-type: none; margin: 0; padding: 0; }
      #messages > li { padding: 0.5rem 1rem; }
      #messages > li:nth-child(odd) { background: #efefef; }
    </style>
  </head>
  <body>
    <ul id="messages"></ul>
    <form id="form" action="">
      <input id="input" autocomplete="off" /><button>Send</button>
    </form>
  </body>
</html>
```

Socket.io is composed of two parts: a server which works in a NodeJS environment, and a client which works on the browser or also in a NodeJS environment

The server side is installed with `npm install socket.io`

The server code for this example application looks this:

```js
const express = require('express');
const app = express();
const http = require('http');
const server = http.createServer(app);
const { Server } = require("socket.io");
const io = new Server(server);

app.get('/', (req, res) => {
  res.sendFile(__dirname + '/index.html');
});

io.on('connection', (socket) => {
  console.log('a user connected');
});

server.listen(3000, () => {
  console.log('listening on *:3000');
});
```

The client side can send messages to the server using the `socket.emit()` method. Using the following code, the input to a form is captured and emitted.

```html
<script src="/socket.io/socket.io.js"></script>
<script>
  var socket = io();

  var form = document.getElementById('form');
  var input = document.getElementById('input');

  form.addEventListener('submit', function(e) {
    e.preventDefault();
    if (input.value) {
      socket.emit('chat message', input.value);
      input.value = '';
    }
  });
</script>
```

The chat app can transmit messages to all other clients with the addition of some client side code:

```html
<script>
  /* 
  code from the previous example goes here
  */

  socket.on('chat message', function(msg) {
    var item = document.createElement('li');
    item.textContent = msg;
    messages.appendChild(item);
    window.scrollTo(0, document.body.scrollHeight);
  });
</script>
```

And some server side code which uses `socket.broadcast.emit()` to emit messages to all connected sockets

```js
io.on('connection', (socket) => {
  socket.broadcast.emit('hi');
});
```

## [Rooms and Namespaces](https://socket.io/docs/rooms-and-namespaces/)

### Rooms

Rooms are an arbitrary channel for grouping sockets together. Sockets can be added and removed at-will. In fact, every socket is in a room by default, which is named after it's socket id and contains only that socket.

Here's a "glossary" of functions/methods important for using rooms:

- `socket.join(<room name>)` Adds the given socket to a room.
- `.to(<room name>)` Emits an event to the sockets in `my room`
  - Example: `io.to('my room').emit('some event')`
  - A socket can broadcast to a room, like so `socket.to()`. 
    - Keep in mind it will not receive it's own event when `.to()` is used in this way.
  - Multiple `.to()`'s can be chained to emit to multiple rooms. `io.to('room1').to('room2').to('room3')`
- `socket.leave(<room name>)` Removes the given socket from the room.

### Namespaces

Namespaces are communication channels which allow you to split the logic of an app over a single connection.

- Namespaces are created and used by assigning the return of `io.of('/my-namespace)`, then using new object like the `io` object.
- It's possible ot create dynamic namespaces with regex or a function.
- Namespaces operate very much like independent socket.io instances
  - They have their own event handlers
  - They have their own rooms
  - They have their own middlewares

## [Socket.io Emit Cheatsheet](https://socket.io/docs/emit-cheatsheet/)

This cheatsheet is a nice, concise reference for `.emit()` usage. Here's some code snippets I want to remember:

- `emitter.emit(/*payload*/)` Emits to all clients
- `emitter.to(/*room name*/).emit(/*payload*/)` Emits to a room
- `emitter.socketsJoin(/*room name*/)` Makes **all** sockets join the given room.
- `emitter.of("/admin").in("room1").socketsJoin("room2")` Makes all Socket instances of the "admin" namespace in the "room1" room join the "room2" room
- `emitter.socketsLeave(/*room name*/)` Makes **all** sockets leave the given room.
  - This can be passed an array of room names to execute this on multiple rooms
- `emitter.disconnectSockets()` Disconnects all sockets
