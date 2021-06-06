#  AWS: S3 and Lambda

## Review, Research, and Discussion

### 1) Describe “The Cloud”

servers that are accessed over the Internet, and the software and databases that run on those servers. ... By using cloud computing, users and companies don't have to manage physical servers themselves or run software applications on their own machines.


### 2) What is a container (as it relates to computers and servers)?

is a standard unit of software that packages up code and all its dependencies so the application runs quickly and reliably from one computing environment to another. 
Available for both Linux and Windows-based applications, containerized software will always run the same, regardless of the infrastructure.


### 3)  What is auto-scaling?

AWS Auto Scaling lets you build scaling plans that automate how groups of different resources respond to changes in demand. You can optimize availability, costs, or a balance of both. AWS Auto Scaling automatically creates all of the scaling policies and sets targets for you based on your preference.


### 4) What is bandwidth?

bandwidth is the maximum rate of data transfer across a given path. Bandwidth may be characterized as network bandwidth, data bandwidth, or digital bandwidth.


## 5)How do cloud providers compute service costs?
When setting price, cloud providers determine the expense to maintaining the network. They start by calculating costs for network hardware, network infrastructure maintenance, and labor. These expenses are added together and then divided by the number of rack units a business will need for its IaaS cloud.


## Vocabulary Terms

1) server instance:

is a collection of SQL Server databases which are run by a solitary SQL Server service or instance. The details of each server instance can be viewed on the service console which can be web-based or command-line based.

2) Containers: A container is a standard unit of software that packages up code and all its dependencies so the application runs quickly and reliably from one computing environment to another.


3) Cloud Services: a wide range of services delivered on demand to companies and customers over the internet, these services are designed to provide easy, affordable access to applications and resources without the need for internal infrastructure or hardware

4) Cloud Architecture: the way technology components combine to build a cloud, in which resources are pooled through virtualization technology and shared across a network
* Components of cloud architecture include:
    - front-end platform (client or device used to access the cloud)
    - back-end platform (servers and storage)
    - cloud-based delivery model
    - network

5) AWS: Amazon Web Services, a subsidiary of Amazon providing on-demand cloud computing platforms and APIs to individuals, companies, and governments on a metered pay-as-you-go basis.

6) EC2/Beanstalk vs Heroku: EC2/Beanstalk is an Infrastructure as a Service product (IaaS), while Heroku is a Platform as a Service (PaaS) product.

### Preview

1) Which 3 things had you heard about previously and now have better clarity on?

- Node.js
- Express.js

2) Which 3 things are you hoping to learn more about in the upcoming lecture/demo?

- AWS
- Trees
- LL

3) What are you most excited about trying to implement or see how it works?

AWS Deployment


## Preparation Materials


### AWS S3

- Cloud object storage service that offers scalability, data availability, security and performance
- Capability to scale your storage resources up and down to meet fluctuating demands
- Stores data across the S3 storage classes which support different data access levels at corresponding rates
- Store your data in Amazon S3 and secure it from unauthorized access with encryption features and access management tools
- S3 is the only object storage service that allows you to block public access to all of your objects at the bucket or the account level
- S3 Access Points make it easy to manage data access with specific permissions for your applications using a shared data set
- Use cases: backup and restore, disaster recovery, archive, data lakes and big data analytics, hybrid cloud storage, cloud-native applications


### AWS Lambda

- AWS Lambda is a serverless computing service provided by Amazon Web Services (AWS)
- The Lambda functions can perform any kind of computing task, from serving web pages and processing streams of data to calling APIs and integrating with other AWS services
- Each Lambda function runs in its own container
- When a function is created, Lambda packages it into a new container and then executes that container on a multi-tenant cluster of machines managed by AWS
- Before the functions start running, each function’s container is allocated its necessary RAM and CPU capacity
- Once the functions finish running, the RAM allocated at the beginning is multiplied by the amount of time the function spent running
- The customers then get charged based on the allocated memory and the amount of run time the function took to complete
- One of the distinctive architectural properties of AWS Lambda is that many instances of the same function, or of different functions from the same AWS account, can be executed concurrently
- Common use cases for Lambda: scalable APIs, data processing, task automation


### CDN

- Content Delivery Network (CDN) is a geographically distributed group of servers that work together to provide fast delivery of Internet content.

- A CDN allows for the fast transfer of data needed for loading Internet content including HTML pages, JavaScript files, stylesheets, images, and videos.

- CDNs work through servers nearest to the website visitor respond to the request.

- The content delivery network copies the pages of a website to a network of servers that are spread out at geographically different locations, caching the contents of the page
- When a user requests a webpage that is part of a content delivery network, the CDN will redirect the request from the originating site’s server to a server in the CDN that is closest to the user and deliver the cached content
- CDNs will also communicate with the originating server to deliver any content that has not been previously cached
- Speed is improved by distributing content closer to the website visitors by using a nearby CDN server, causing visitors to experience faster page loading times






