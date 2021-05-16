# Express

## What’s the difference between PUT and PATCH?

When designing API endpoints, there’s always the need to specify what http method to use for CRUD (Create, Read/Retrieve, Update, Delete) operations. Commonly, this is nailed down as:
* Create — POST
* Read/Retrieve — GET
* Update — PUT/PATCH
* Delete — DELETE

In this section of our article we will focus on the differences between PUT and PATCH.

We might think that PUT and PATCH do the same thing and are simply aliases but we couldn’t be further from the truth. It’s true that both methods update the resource at a location, but they do so differently.

### PUT: 

PUT is a method of modifying resource where the client sends data that updates the entire resource. It is used to set an entity’s information completely. PUT is similar to POST in that it can create resources, but it does so when there is a defined URI. PUT overwrites the entire entity if it already exists, and creates a new resource if it doesn’t exist.

For example, when you want to change the first name of a person in a database, you need to send the entire resource when making a PUT request.

```
{“first": "John", "last": "Stone”}

```
To make a PUT request, you need to send the two parameters; the first and the last name.


### PATCH:

Unlike PUT, PATCH applies a partial update to the resource.

This means that you are only required to send the data that you want to update, and it won’t affect or change anything else. So if you want to update the first name on a database, you will only be required to send the first parameter; the first name.

## Three tools for mocking HTTP requests
1) Postman
2) Nock
3) Stoplight

##  Swagger VS APIDoc.js

While developing node services, we might need to expose our Api documents based on requirement.

In that case we think of picking right documentation tool because there are many 3rd parties tools available for it. I have created sample POC by using 2 popular documentation tools:

a. Swagger

b. Apidocjs

Here is my finding regarding both:


1) Popularity: By comparing stats,  swagger-ui is more popular then apidocjs.
Consistency: If we already using swagger for our Dotnetcore service, then implementing swagger tool will consist more from Info and UI prospective.

2) Implementation complexity: apidocjs and swagger both required documentation content on implemented method as customize comment data. In addition they allow to write documentation data in separate resource file as .js and .json. If we already have swagger.json created by DotnetCore we can reuse more than 80% specification.

3) Maintenance: For apidocjs will have to modify documentation for each affected method/endpoints if service changed. In swagger we can limit changes. But by implementing apidocjs we can isolate the layer.

4) Other benefits: Because swagger use plain .json that could be parsed through programing language, thus we can get advantage of various other 3rd parties in order to create http client and more. 

5) Future: Due to popularity of swagger, apidocjs provide information about apidoc-swagger converter so we can switch apidoc to swagger anytime.


## SOAP VS REST

REST operates through a solitary, consistent interface to access named resources. It’s most commonly used when you’re exposing a public API over the Internet. SOAP, on the other hand, exposes components of application logic as services rather than data. Additionally, it operates through different interfaces. To put it simply, REST accesses data while SOAP performs operations through a more standardized set of messaging patterns. Still, in most cases, either REST or SOAP could be used to achieve the same outcome (and both are infinitely scalable), with some differences in how you’d configure it.

SOAP was originally created by Microsoft, and it’s been around a lot longer than REST. This gives it the advantage of being an established, legacy protocol. But REST has been around for a good time now as well. Plus, it entered the scene as a way to access web services in a much simpler way than possible with SOAP by using HTTP.

## Definitions

1) Web Server :
A web server is a computer that runs websites. It's a computer program that distributes web pages as they are requisitioned. The basic objective of the web server is to store, process and deliver web pages to the users. This intercommunication is done using Hypertext Transfer Protocol (HTTP).

2) Express: It's a web framework that let's you structure a web application to handle multiple different http requests at a specific url. Express is a minimal, open source and flexible Node. js web app framework designed to make developing websites, web apps, & API's much easier.

3) Routing: is the process of selecting a path for traffic in a network or between or across multiple networks.

4) WRRC: It's a blueprint describes the way that a backend server deals with different http requests/responses and where it redirects each request and response.

## TDD
Test-driven development (TDD) is a development technique where you must first write a test that fails before you write new functional code. TDD is being quickly adopted by agile software developers for development of application source code and is even being adopted by Agile DBAs for database development.

## CI/CD

CI/CD is a method to frequently deliver apps to customers by introducing automation into the stages of app development. The main concepts attributed to CI/CD are continuous integration, continuous delivery, and continuous deployment.

