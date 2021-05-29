# Event Driven Applications

![](https://www.bbconsult.co.uk/wp-content/uploads/2018/09/event-driven-apps.jpg)

## Review, Research, and Discussion

**1) Why is access control important?**

Access controls limit access to information and information processing systems. When implemented effectively, they mitigate the risk of information being accessed without the appropriate authorization, unlawfully and the risk of a data breach.

**2)Describe an application that would need access control.** 

* Social media applications

**3) What is a role used for?**

A role is used to specify the user authorization in an app For example:
* Administrators can: (read, write, update and delete), while a default user can only have read capabilities.

**4) Why is role based access control more scalable than discretionary or mandatory access control?**

The assignment of access rights in RBAC is very systematic and repeatable, easier to audit user rights (users are in only one of a few categories), and easier to correct any issues that are identified. There is no case by case assignment of roles, users fall into one of already pre-assigned roles/capabilities.

## Terms

**1) Authorization**
process of giving the user permission to access a specific resource or function (access control or client privilege), in secure environments authorization must follow authentication

**2) Role Based Access Control**

is a method of restricting network access based on the roles of individual users within an enterprise.

**3) Capabilities**
the access that a user has in an app (read, create, update, or delete for example)


## Preview

**Which 3 things had you heard about previously and now have better clarity on?**

1) middlewares
2) o-auth
3) basic sign-in

**Which 3 things are you hoping to learn more about in the upcoming lecture/demo?**

1) Event driven applications
2) Stack and Queues


**What are you most excited about trying to implement or see how it works?**
Event driven applications

## Preparation Materials

**What is Event-Driven Programming?**

Event-Driven Programming is a logical pattern that we can choose to confine our programming within to avoid issues of complexity and collision.


**Overview**

* Every time you interact with a webpage through it’s user interface, an event is happening.

* Event-Driven Programming makes use of the following concepts:

  1) An Event Handler is a callback function that will be called when an event is triggered.
  2) A Main Loop listens for event triggers and calls the associated event handler for that event.


**EventEmitter**

- EventEmitter: Node.js nativey provides this module, allows us to get started incorporating event driven programming into projects right away
- Access the EventEmitter class through the `events` module, one imported you need to create a new object from the class to start using it

```js
const EventEmitter = require('events').EventEmitter;
const myEventEmitter = new EventEmitter();
```

- Use EventEmitters `on` method to set the listener
- Use the `emit` method to trigger the event
- Removing listeners with `removeListener` or `removeAllListeners`
- Must pass reference to the exact function you wish to remove when using the `removeListener` method, which means wherever you want to remove the event you need to make sure the function is able to be referenced from that place in your code (often best to name the event handling function and declare them before you register the event listener as opposed to leaving them anonymous)


**Object Oriented Programming + Event-Driven Programming**

The Object Oriented approach promotes the idea that all behavior of an individual unit (or object) be handled from code within that unit. Using this approach, applications are built with many different units that all speak to and interact with each other.



**Node docs:**

- All objects that emit events are instances of the `EventEmitter` class.

- These objects expose an `eventEmitter.on()` function that allows one or more functions to be attached to named events emitted by the object.

- When the `EventEmitter` object emits an event, all of the functions attached to that specific event are called synchronously, any values returned by the called listeners are ignored and discarded.

- `eventEmitter.on()` is used to register listeners.

- `eventEmitter.emit())` is used to trigger the event.

- The `eventEmitter.emit()` method allows an arbitrary set of arguments to be passed to the listener functions.

