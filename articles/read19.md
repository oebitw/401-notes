#  AWS: Events

## Review, Research, and Discussion

### 1) Describe the similarities between AWS API Gateway + Lambda functions and an ExpressJS Server

Express is commonly used for both web applications as well as REST APIs. While the primary API Gateway function is to deliver APIs, it can certainly be used for delivering web apps/sites (HTML) as well.

### 2) List the AWS Database offerings and talk about the pros and cons of each

* Amazon Relational Database Service :

 Amazon Relational Database Service (Amazon RDS) makes it easy to set up, operate, and scale a relational database in the cloud. It provides cost-efficient and resizable capacity while automating time-consuming administration tasks such as hardware provisioning, database setup, patching and backups.


* Amazon DynamoDB

Amazon DynamoDB is a key-value and document database that delivers single-digit millisecond performance at any scale. It's a fully managed, multi-region, multi-active, durable database with built-in security, backup and restore, and in-memory caching for internet-scale applications. DynamoDB can handle more than 10 trillion requests per day and can support peaks of more than 20 million requests per second.

* Amazon Redshift

No other data warehouse makes it as easy to gain new insights from all your data. With Redshift, you can query and combine exabytes of structured and semi-structured data across your data warehouse, operational database, and data lake using standard SQL. Redshift lets you easily save the results of your queries back to your S3 data lake using open formats, like Apache Parquet, so that you can do additional analytics from other analytics services like Amazon EMR, Amazon Athena, and Amazon SageMaker.


### 3) What’s the difference between a FIFO and a standard queue?

FIFO queues have essentially the same features as standard queues, but provide the added benefits of supporting ordering and exactly-once processing. FIFO queues provide additional features that help prevent unintentional duplicates from being sent by message producers or from being received by message consumers.


### 4) How can the server be assured a message was properly received?

A Message Authentication Code (MAC) is a tag attached to a message to ensure the integrity and authenticity of the message. It is derived by applying a MAC algorithm to a message in combination with a secret key.


## Vocabulary Terms

* Serverless API

a cloud computing execution model where the cloud provider dynamically manages the allocation and provisioning of servers

* Triggers

an AWS Lambda resource or resource in another service that you configure to invoke your function in response to lifecycle events, external requests or on a schedule, a function can have multiple triggers

* Dynamo vs Mongo

a visual programming tool used to define relationships and create algorithms that then can be used to generate geometry in 3D space and to process data. MongoDB is a source-available cross-platform document-oriented database program. Classified as a NoSQL database program, MongoDB uses JSON-like documents with optional schemas.

* Dynamoose vs Mongoose

Dynamoose is a DynamoDB API structured like Mongoose, lets us provide a schema and perform CRUD operations against a DynamoDB table, installed via node and configured based on role.


## Preview

1) Which 3 things had you heard about previously and now have better clarity on?

- middle ware
- Mongoose
- Linked List

2) Which 3 things are you hoping to learn more about in the upcoming lecture/demo?

- AWS Dynamo
- AWS lamda


3) What are you most excited about trying to implement or see how it works?

Socket.io

## Preparation Materials

### AWS — Difference between SQS and SNS


SQS and SNS are important components for scalable, large scale, distributed, cloud-based applications:
SNS is a distributed publish-subscribe service.
SQS is distributed queuing service.


![](https://miro.medium.com/max/1004/1*mdUPKzrfJFuXa4d43KhKUQ.png)
 

**Amazon SNS** is a fast, flexible, fully managed push notification service that lets you send individual messages or to bulk messages to large numbers of recipients. Amazon SNS makes it simple and cost effective to send push notifications to mobile device users, email recipients or even send messages to other distributed services.


![](https://miro.medium.com/max/1700/1*7eL3udb6Cto4I9Ly1sN8oA.jpeg)

**SQS** is distributed queuing system. Messages are not pushed to receivers. Receivers have to poll SQS to receive messages. Messages can’t be received by multiple receivers at the same time. Any one receiver can receive a message, process and delete it. Other receivers do not receive the same message later.
Polling inherently introduces some latency in message delivery in SQS unlike SNS where messages are immediately pushed to subscribers.