# AWS: API, Dynamo and Lambda

## Review, Research, and Discussion


### 1) What are serverless functions?

A serverless function is a programmatic function written by a software developer for a single purpose. It's then hosted and maintained on infrastructure by cloud computing companies. These companies take care of code maintenance and execution so that developers can deploy new code faster and easier.

### 2) If you were to create a system that emulated Lambda functions, how would you do it?

1) Open the Functions page on the Lambda console.

2) Choose Create function.

3) Under Basic information, do the following:

     a) For Function name, enter my-function.

    b) For Runtime, confirm that Node.js 14.x is selected. Note that Lambda provides runtimes for .NET (PowerShell,C#) Go, Java, Node.js, Python, and Ruby.

4) Choose Create function.

Lambda creates a Node.js function and an execution role that grants the function permission to upload logs. The Lambda function assumes the execution role when you invoke your function, and uses the execution role to create credentials for the AWS SDK and to read data from event sources.

### 3) Describe how a CDN works?

To minimize the distance between the visitors and your website's server, a CDN stores a cached version of its content in multiple geographical locations.In essence, CDN puts your content in many places at once, providing superior coverage to your users.



## Vocabulary Terms

1)  serverless function:

is a programmatic function written by a software developer for a single purpose. It's then hosted and maintained on infrastructure by cloud computing companies. These companies take care of code maintenance and execution so that developers can deploy new code faster and easier.

2) Cloud storage : 

allows you to save data and files in an off-site location that you access either through the public internet or a dedicated private network connection. Data that you transfer off-site for storage becomes the responsibility of a third-party cloud provider.


3) content delivery network:

or content distribution network, is a geographically distributed network of proxy servers and their data centers. The goal is to provide high availability and performance by distributing the service spatially relative to end users.

## Preview


1) Which 3 things had you heard about previously and now have better clarity on?

    - Tree Data Structure
    - Basic Auth
    - O Auth

2) Which 3 things are you hoping to learn more about in the upcoming lecture/demo? 

   - Socket.io
   - AWS


3) What are you most excited about trying to implement or see how it works?

AWS


## Amazon API Gateway

### What is Amazon API Gateway?

Amazon API Gateway is a managed service that allows developers to define the HTTP endpoints of a REST API or a WebSocket API and connect those endpoints with the corresponding backend business logic. It also handles authentication, access control, monitoring, and tracing of API requests.


### How does API Gateway work?

API Gateway sits between the backend services of your API and your API’s users, handling the HTTP requests to your API endpoints and routing them to the correct backends. It provides a set of tools that help you manage your API definitions and the mappings between endpoints and their respective backend services. It can also generate API references from your definitions and make them available to your users as API documentation.

### Why is API Gateway an essential part of the Serverless ecosystem?

Within the Serverless ecosystem, API Gateway is the piece that ties together Serverless functions and API definitions. Being able to trigger the execution of a Serverless function directly in response to an HTTP request is the key reason why API Gateway is so valuable in Serverless setups: it enables a truly serverless architecture for web applications. When using API Gateway together with other AWS services, it’s possible to build a fully functional customer-facing web application without maintaining a single server yourself.

API Gateway integrates with many other AWS services like AWS Lambda, AWS SNS, AWS IAM, and Cognito Identity Pools. These integrations allow for fully managed authentication and authorization layers, as well as detailed metrics and tracing for API requests.


## Amazon DynamoDB

Amazon DynamoDB is a key-value and document database that delivers single-digit millisecond performance at any scale. It's a fully managed, multi-region, multi-active, durable database with built-in security, backup and restore, and in-memory caching for internet-scale applications. DynamoDB can handle more than 10 trillion requests per day and can support peaks of more than 20 million requests per second.

In other words it is a hosted NoSQL database offered by Amazon Web Services (AWS). It offers:

1) reliable performance even as it scales;

2) a managed experience, so you won't be SSH-ing into servers to upgrade the crypto libraries;

3) a small, simple API allowing for simple key-value access as well as more advanced query patterns.

### Benefits
- Performance at scale
- No servers to manage
- Enterprise ready


## Dynamoose

Dynamoose is a modeling tool for Amazon's DynamoDB. Dynamoose is heavily inspired by Mongoose, which means if you are coming from Mongoose the syntax will be very familar.

### Key Features

- Type safety
- High level API
- Easy to use syntax
- Ability to transform data before saving or retrieving documents
- Strict data modeling (validation, required attributes, and more)
- Support for DynamoDB Transactions
- Powerful Conditional/Filtering Support
- Callback & Promise support


