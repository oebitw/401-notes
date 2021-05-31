# Message Queues

## Review, Research, and Discussion

1. **What does it mean that web sockets are bidirectional? Why is this useful?**

Data flows both ways (full-duplex), a web socket can both send and receive which is useful because it allows data to be sent and received on the same channel.

2. **Does socket.io use HTTP? Why?**

Yes, it can. Socket.io will try to establish a WebSocket () if possible but if it cannot it will fall back on HTTP.

3. **What happens when a client emits an event?**

The event will be sent to the server, which will be listening for the event if already connected

4. **What happens when a server emits an event?**

Whatever client is listening for the event (maybe all, or maybe one specific client) will respond

5. **What happens if a client “misses” an event?**

Unhandled messages are ignored, behaves as if there is no event listener for the event

6. **How can we mitigate this?**

Can avoid missing an event by always having handlers installed and then deciding in the handlers whether to do anything with the message or not.


## Vocabulary Terms

**Socket**: Sockets allow communication between two different processes on the same or different machines.

**Web Socket**: WebSocket is a computer communications protocol, providing full-duplex communication channels over a single TCP connection.

**Socket.io**:is a library that enables real-time, bidirectional and event-based communication between the browser and the server.

**Client**: client is a piece of computer hardware or software that accesses a service made available by a server as part of the client–server model of computer networks.

**Server**: server is a piece of computer hardware or software that provides functionality for other programs or devices.

**OSI Model**: The Open Systems Interconnection model is a conceptual model that characterizes and standardizes the communication functions of a telecommunication or computing system without regard to its underlying internal structure and technology.

**TCP Model**: The Internet protocol suite is the conceptual model and set of communications protocols used in the Internet and similar computer networks.

**TCP**: The Transmission Control Protocol (TCP) is one of the main protocols of the Internet protocol suite.

**UDP**: User Datagram Protocol (UDP) – a communications protocol that facilitates the exchange of messages between computing devices in a network.

**Packets**:  a packet is a small segment of a larger message. Data sent over computer networks*, such as the Internet, is divided into packets.


## Socket.io Chat example

- Sockets have traditionally been the solution around which most real-time chat systems are architected, providing a bi-directional communication channel between a client and a server
- The server can push messages to clients
- Whenever you write a chat message, the idea is that the server will get it and push it to all other connected clients
- Setup steps [here](https://socket.io/get-started/chat/)

## Rooms and Namespaces

- Room is an arbitrary channel that sockets can join and leave, it can be used to broadcast events to a subset of clients
- Rooms are a server-only concept (client does not have access to the list of rooms it has joined)
- Can join to subscribe the socket to a given channel ```socket.join()```
- Each socket in Socket.io is identified by a random unique identifier (Socket#id), each socket automatically joins a room identified by its own id
- Upon disconnection, sockets leave all the channels they were part of automatically.