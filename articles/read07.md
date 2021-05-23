# Bearer Authorization


## Review, Research, and Discussion

### Write the following steps in the correct order
1) Register your application to get a client_id and client_secret

2) Ask the client if they want to sign in via a third party

3) Redirect to a third party authentication endpoint

4) Make a request to the third-party API endpoint

5) Receive authorization code

6) Make a request to the access token endpoint

7) Receive access token

### What can you do with an authorization code?

The authorization code is a temporary code that the client will exchange for an access token. The code itself is obtained from the authorization server where the user gets a chance to see what information the client is requesting, and approve or deny the request.

### What can you do with an access token?
Access tokens are the thing that applications use to make API requests on behalf of a user. The access token represents the authorization of a specific application to access specific parts of a user’s data.

### What's a benefit of using OAuth instead of your own basic authentication?
Better security, token management provides you with a means of tracking each connected device that uses your API.

## Vocabulary Terms

* Client ID: a public identifier for apps

* Client Secret: secret known only to the application and the authorization server

* Authentication endpoint: where the user is sent to input credentials to become authorized
Access Token Endpoint: where apps make a request to get an access token for a user

* API Endpoint: can include a URL of a server or service, each endpoint is the location from which APIs can access the resources they need to carry out their function

* Authorization Code: temporary code that the client will exchange for an access token


* Access token:
is an object encapsulating the security identity of a process or thread. A token is used to make security decisions and to store tamper-proof information about some system entity.


## Preview

Which 3 things had you heard about previously and now have better clarity on?

* linked list
* basic auth
* mongodb

Which 3 things are you hoping to learn more about in the upcoming lecture/demo?

* basic auth
* mongodb
* data structure

What are you most excited about trying to implement or see how it works?

basic auth

## Preparation Materials

## JWTs 

*`A JSON Web Token (JWT)` is a JSON object encoded as a long string. We use 
them to identify users. It’s similar to a passport or driver’s license. It includes a few public properties about a user in its payload. These properties cannot be 
tampered because doing so requires re-generating the digital signature.*


* When the user logs in, we generate a JWT on the server and return it to the 
client. We store this token on the client and send it to the server every time we 
need to call an API endpoint that is only accessible to authenticated users.

* To generate JSON Web Tokens in an Express app use jsonwebtoken package. 

**Generating a JWT**


`const jwt = require(‘jsonwebtoken’);`

`const token = jwt.sign({ _id: user._id}, ‘privateKey’);`


* Never store private keys and other secrets in your codebase. Store them in 
environment variables. Use the config package to read application settings 
stored in environment variables. 

