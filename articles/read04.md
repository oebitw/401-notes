# Data Modeling
![](https://cdn.mindmajix.com/courses/data-modeling-training.png)

## Review, Research, and Discussion

### Name 3 advantages to Test Driven Development

* Reduction in defect rates
* Better program design and higher code quality
* overheads are more than offset by reduction in effort of projects' final phases


### In what case would you need to use beforeEach() or afterEach() in a test suite?

when a method should run before a test and another method should run after it.

### What is one downside of Test Driven Development

not running tests frequently enough or writing too many tests at once.


### What’s the primary difference between ES6 Classes and Constructor/Prototype Classes?

Inheritance is much more efficient and simple for ES6 classes.


### Why REST?

* Can be used well where network bandwidth is a constraint.

* Don't need to maintain a state of information from one request to another.

* Good for caching a lot of requests.

* Much easier to code/implement for web services than SOAP.


## Terms:

### Functional programming:

* Software is composed using pure functions (avoid shared state, mutable data, side-effects).

* If functions are interrelated, changing one function could break everything else.

### object-oriented programming (OOP)

Object-oriented programming is a programming paradigm based on the concept of "objects", which can contain data and code: data in the form of fields, and code, in the form of procedures. A feature of objects is that an object's own procedures can access and often modify the data fields of itself.

### Class

Templates for creating objects. The constructor() method is used for creating and initializing an object created with a class. Can only be one constructor() per class.

### `super`

this is used to call the constructor of the super (parent) class

### `this`

`this` refers to the current object being instantiated.

### Test Driven Development (TDD)

is a software development process relying on software requirements being converted to test cases before software is fully developed, and tracking all software development by repeatedly testing the software against all test cases.

### Jest

is a JavaScript testing framework designed to ensure correctness of any JavaScript codebase.

### Continuous Integration (CI)

consistent merging from multiple places into one multiple times a day.

### REST

Representational State Transfer. Uses HTTP requests to retrieve/use data.

### Data Model	

a model that describes the data and their relations.

## Preparation Materials

### NoSQL vs SQL

#### NoSQL
* primarily called non-relational database.

* document based, key-value pairs, graph databases, or wide-column stores.

* dynamic schema for unstructured data.

* horizontally scalable

* queries are focused on collection of documents, sometimes called unstructured query language (UnQL)

#### SQL
* primarily called relational databases
* table databases
* predefined schema
* vertically scalable
* use structured query language

#### Mongoose
It is an Object Data Modeling (ODM) library for MongoDB and Node. js.


#### NoSQL Modeling Techniques

* Often compared by various non-functional criteria, such as scalability, performance, and consistency.

* Often starts from the application-specific queries as opposed to relational modeling.

* Data duplication and de normalization are first class citizens

* Often requires a deeper understanding of data structures and algorithms than relational database modeling does.

















