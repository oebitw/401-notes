# Event Driven Architecture

## Review, Research, and Discussion

1) What’s the difference between a FIFO and a standard queue?

FIFO queues have essentially the same features as standard queues, but provide the added benefits of supporting ordering and exactly-once processing. FIFO queues provide additional features that help prevent unintentional duplicates from being sent by message producers or from being received by message consumers

2) How can the server be assured a message was properly received?

We Make a queue and when the client connect to internet it will connect to queue and get all massages


3) What classic design pattern is best represented by event driven programming?

Event Notification

4) How do you test an event driven system?

emit an event and check if It's run the code in the event listener.


## Preview
1) Which 3 things had you heard about previously and now have better clarity on?
    * event
    * queue
    * socket

2) Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
    * message queue
    * socket

## Preparation

![](https://miro.medium.com/max/1446/1*DRrTtdyah9NHwR0VCm6MWA.png)

SQS and SNS are important components for scalable, large scale, distributed, cloud-based applications:
SNS is a distributed publish-subscribe service.
SQS is distributed queuing service.

### SNS (Simple Notification Service)

![](https://miro.medium.com/max/1004/1*mdUPKzrfJFuXa4d43KhKUQ.png)

Amazon SNS is a fast, flexible, fully managed push notification service that lets you send individual messages or to bulk messages to large numbers of recipients. Amazon SNS makes it simple and cost effective to send push notifications to mobile device users, email recipients or even send messages to other distributed services.


### SQS (Simple Queue Service)

![](https://miro.medium.com/max/1700/1*7eL3udb6Cto4I9Ly1sN8oA.jpeg)

SQS is distributed queuing system. Messages are not pushed to receivers. Receivers have to poll SQS to receive messages. Messages can’t be received by multiple receivers at the same time. Any one receiver can receive a message, process and delete it. Other receivers do not receive the same message later.
Polling inherently introduces some latency in message delivery in SQS unlike SNS where messages are immediately pushed to subscribers.