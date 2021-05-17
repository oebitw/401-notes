# Express REST API

![](https://bs-uploads.toptal.io/blackfish-uploads/blog/post/seo/og_image_file/og_image/15921/secure-rest-api-in-nodejs-18f43b3033c239da5d2525cfd9fdc98f.png)

## Review, Research, and Discussion:


### Name 3 real world use cases where you’d want to change the request with custom middleware**

* Error handling
* Data management
* Authentication

### True or false: The route handler is middleware?

False, a route handler is the piece of code that makes an HTTP request, such as `GET`, `POST`, `PUT`, and `DELETE`.

### At what point in the request lifecycle can you “inject” middleware?

After the request is made and before the response is sent, or it could be listed after the route being requested, but before the callback. Example below:

```
app.get('/', logger, (req, res) => {
  res.status(200).send('HELLO WORLD');
})
```

### What can cause express to error with “Request headers sent twice, cannot start a second response”

The problematic middleware sets the response header without calling response.end() and calls next(), which confuses connects server.


## TERMS

1. **Middleware** Any functionality that sits in between request/response, but does not send out response itself.
2. **Request Object** Represents the information in the HTTP request from the client to the server.
3. **Response Object** Information in the HTTP response from the server to the client.
4. **Application Middleware** an application that uses middleware.

5. **Routing Middleware** 
Middleware that plays a role in path routing.

6. **Test-driven development** is a process of modifying the code in order to pass a test designed previously. In Software Engineering, It is sometimes known as "Test First Development.

7. **Behavioral Testing** Testing of the external behavior of the program.

## Preparation Materials

### ES6 Classes

Classes are a template for creating objects. They encapsulate data with code to work on that data. Classes in JS are built on prototypes but also have some syntax and semantics that are not shared with ES5 class-like semantics.


### Express Routing

* Routing refers to how an application’s endpoints (URIs) respond to client requests.
* Define routing using methods of the Express app object that correspond to HTTP methods
* Routing methods specify a callback function (sometimes called "handler functions") called when the application receives a request to the specified route (endpoint) and HTTP method
* Routing methods can have more than one callback function as arguments


