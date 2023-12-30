# Sending data with POST

## But what is the <b>Body</b>

Adding or updating structured data needs to be sent using body data

The <b>Body</b> tab in Postman enables you to specify the data you need to send with a request. You can send different data to suit you API.

Anything that can be sent as text can be sent using raw body data which can include different format like (<b>Text, Javascript, JSON, HTML, or XML</b>), and Postman will enable syntax-highlighting and appending the relevant headers to your request.

## Make a POST request

### Authorization

This is the way of granting permission to a request being sent to an endpoint.

There are multiple methods for authorizing a request. Some examples are <b>Basic Auth</b> (username and password), <b>OAuth</b> (Delegated authorzation) and <b>API Keys</b> (secret strings registered to a developer from an API portal)/

### Getting an API Key

APIs that use API key auth usually allow developers to sign up in a developer portal, where they will recieve a random API key that can be used to authorize their requests to the API. The API key allows the API to track who is making calls and how often.

The Postman Library API v2 uses very light protection and does not require you to register for an API Key. You simply have to know it:

Header name: `api-key`<br />
Header value: `postmanrulz`

The Postman Library API v2 requires adding this <b>header</b> to any requests for adding, updating and deleting books, since these operations change data in the database instead of simply reading them.

### Headers

Headers are how we can add <b>metadata</b> about our requests, such as authorization information or specify the data type we want to recieve in a response. This is different fromt the actual payload data we send inthe body of a request, such as our new book information.
