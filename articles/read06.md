# Authentication
![](https://www.loginradius.com/blog/start-with-identity/static/c49123200495a3bc193612dc9923645d/a3513/Authentication-vs.-Authorization.png)

## Review, Research, and Discussion

### 1) Explain what a “Singleton” is (in Computer Science terms)

“Singleton” is a class that allows only a single instance of itself to be created and gives access to that created instance. It contains static variables that can accommodate unique and private instances of itself. It is used in scenarios when a user wants to restrict instantiation of a class to only one object.

### Explain how the Singleton pattern can be used with Node modules, specifically with classes:

Singleton design pattern restricts the instantiation of a class to a single instance

```
// car.js file
class Car {
    constructor(make, model,year) {
        this.make = make;
        this.model = model;
        this.year=year
    }
}
module.exports = Car;

// toyota.js file
const Car = require('car.js');
const camry = new Car('toyota', 'camry', 2021);
```

### 3) If you were tasked with building a middleware system like Express uses, what approach might you take to construct/operate it?

* Create a function that takes three arguments :
  * req
  * res
  * next

* The req will indicate the received data.

* The res will indicate the data sent from the server after handling the data.

* next will go to the next middleware.

```
const express = require('express')
const app = express()

const middleWare = (request, response, next) => {... next()}

app.use(middleWare);

app.get('/route', (request, response) => {...})

app.listen(PORT)
```

## Vocabulary Terms

* Router Middleware: works in the same way as application-level middleware, except it is bound to an instance of express.Router()

* Dynamic Module Loading: the mechanism by which a computer program can, at run time, load a library (or other binary) into memory, retrieve the addresses of functions and variables contained in the library, execute those functions or access those variables, and unload the library from memory.

* singleton pattern : is a software design pattern that restricts the instantiation of a class to one "single" instance. This is useful when exactly one object is needed to coordinate actions across the system. The term comes from the mathematical concept of a singleton.

* CRUD -> REST Method Matches :
  
  * Create => post
  * Read => get
  * Update => put
  * Delete => delete


* Mock testing:

it is an approach to unit testing that lets you make assertions about how the code under test is interacting with other system modules. In mock testing, the dependencies are replaced with objects that simulate the behavior of the real ones.


## Preview

### Which 3 things had you heard about previously and now have better clarity on?

* Model view control (MVC)

* Binary search

* middle wares

### Which 3 things are you hoping to learn more about in the upcoming lecture/demo?

* Linked List

* Authentication

* Data structure and algorithm.

## Preparation Materials

### 1) Securing Passwords

Hashing is the greatest way for protecting passwords and considered to be pretty safe for ensuring the integrity of data or passwords.

**PROBLEMS WITH CRYPTOGRAPHIC HASH ALGORITHM**

There are some weaknesses in cryptographic hash algorithm that allows an attacker to calculate the original value of hashed password: 
* Brute Force attack

* Hash Collision attack


### 2) Basic Auth

is a simple authentication scheme built into the HTTP protocol. The client sends HTTP requests with the Authorization header that contains the word Basic word followed by a space and a base64-encoded string username:password .

### 3) OWASP Cheat Sheet

* Authentication: is the process of verifying that an individual, entity or website is whom it claims to be.

* Session management: is a process by which a server maintains the state of an entity interacting with it. This is required for a server to remember how to react to subsequent requests throughout a transaction.


* Passwords: minimum length of 8 characters, common maximum length is 64 characters.

* Transmit passwords only over TLS (transport layer protection) or other strong transport.


* Account lockout: prevent any more login attempts after a series of failed logins.

### 4) bcrypt docs

* it is a library to help us in hashing passwords.
* `npm i bcrypt`









