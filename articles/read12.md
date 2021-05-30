# Socket.io

![](https://ik.imagekit.io/ably/ghost/prod/2021/03/socket-io-logo.jpeg?tr=w-1520)


## Review, Research, and Discussion

**1) What is the benefit of transforming data into packets?**


Allows for data to be transferred fast and efficiently over the network and minimizes the transmission latency.



**2) UDP is often refereed to as a connectionless protocol. Why is this?**

UDP is a connectionless protocol. It is known as a datagram protocol because it is analogous to sending a letter where you don't acknowledge receipt. Examples of applications that use connectionless transport services are broadcasting and tftp .



**3) Can a socket server application have multiple socket connections?**

A server socket listens on a single port, but it is able to share the same server-side IP/Port pair as long as they are associated with different client-side IP/Port pairs


**4) Can a socket connection application be connected to multiple socket servers?**

Yes, it can handle up to 65535.



**5) Can an application be both a socket server and a socket connection?**

Yes


## Term

**1) Observer Pattern**

The observer pattern is a software design pattern in which an object, named the subject, maintains a list of its dependents, called observers, and notifies them automatically of any state changes, usually by calling one of their methods.

**2) Listener**

An event listener is a procedure or function in a computer program that waits for an event to occur

**3) Event Handler**

a function that runs when a specific event fires

**4) Event Driven Programming**

programming paradigm in which the flow of the program is determined by events such as user actions, message passing

**5) Event Loop**

In computer science, the event loop is a programming construct or design pattern that waits for and dispatches events or messages in a program.

**6) Event Queue**

is to synchronize the different servers when a change has occurred in the Sitecore Back Office.

**7) Call Stack**

a mechanism for an interpreter to keep track of its place in a script that calls multiple functions - what function is currently being run and what functions are called from within that function

**8) Emit/Raise/Trigger**

in event-driven programming, emit sends a message to trigger a response and raise an event

**9) Subscribe**

waiting for a published event to take place

**10) database**

an organized collection of data, generally stored and accessed electronically from a computer system


## Preview

**1) Which 3 things had you heard about previously and now have better clarity on?**

  * Middleware
  * Basic Auth
  * Express



**2) Which 3 things are you hoping to learn more about in the upcoming lecture/demo?**

  * event driven applications
  * Sockets


**3) What are you most excited about trying to implement or see how it works?**

  * event driven applications

## Preparation Materials

* WebSocket is a computer communications protocol, providing full-duplex communication channels over a single TCP connection. The WebSocket protocol was standardized by the IETF as RFC 6455 in 2011, and the WebSocket API in Web IDL is being standardized by the W3C.

* Socket.IO enables real-time bidirectional event-based communication. It works on every platform, browser or device, focusing equally on reliability and speed. Socket.IO is built on top of the WebSockets API (Client side) and Node.js. It is one of the most depended upon library on npm (Node Package Manager).

* WebSocket :

  * It is the protocol that is established over the TCP connection.

  * It provides full-duplex communication on TCP connections.

  * Proxy and load balancer is not supported in WebSocket.

  * It doesn’t support broadcasting.

  * It doesn’t have a fallback option.

- Socket.io :
    - It is the library to work with WebSocket
    - Provides the event-based communication between browser and server.
    - A connection can be established in the presence of proxies and load balancers.
    - It supports broadcasting.
    - It supports fallback options.

