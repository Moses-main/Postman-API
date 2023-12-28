# MY LEARNING PROCESS (API)

## What are APIs

<p> API simply stands for Application Programming Interface. APIs functions as the middle men between a computer server and the client making request to the servers</p>

## Types of APIs

- `Hardware APIs`: Interfaces for software to talk to hardware. **_example: How phone
  's camera talks to the operating system_**

- `Software Library APIS`: Interface for directly consuming code from another code base. **_example: Using methods from a library you import into your application_**

- `Web APIs`: Interface for communicating across code bases over a network. **_example: Fetching current stock prices from a finance API over the internet_**

## Architectures

- REST (Respresentational State Transfer)
- GraphQL
- WebSockets
- Webhooks
- SOAP (Simple Object Access Protocol)
- gRPC (Google Remote Procdure Call)
- MQTT (MQ Telemetry Transport)

## <b>REST APIs</b>

<p>Some traits of REST APIs include <ol>
<li>Not Storing session state betweeen requests.</li>
<li>The ability to cache</li>
<li>The ability to send and recieve various data types.</li>
</ol></p>

## Access

<p>APIs also vay in the scope of who can access them.</p>

- <b> Public APIs (aka OPen APIs)</b>
<p>Consumed by anyone who discovers the API</p>

- <b>Private APIs (aka OPen APIs)</b>
<p>Consumed only within organization and not made public</p>

- <b>Partner APIs (aka OPen APIs)</b>
<p>Consumed between one or more organizations that have an established relationship</p>

## Working with APIs then and now:cURL vs. Postman

#### <b>API calls with `curl`</b>

<p>Before Postman, it was common practice to poke at APIs with a command line tool for making HTTP requests called cURL.</p>

**_example curl https://api.github.com/users/postmanlabs_**

#### <b>API calls with Postman</b>

<p>Here is the same call done with Postman. Postman shows the response with clean indents and olors and allows you to save, organize and share your requests. All the components of the request and response are broken down into tabs and other helpful details like the response time and status code.</p>
