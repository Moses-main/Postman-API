# Request Methods

<p>When making an HTTP call to a server, we specifu a <b>request method</b> that indicates the type of operation we are about to perfom. These are also called <b>HTTP verbs</b></p>

---

| <b> Method Name | Operation |</b>

|`GET` | Retrieve data (Read) |

|`POST` | Send data (Create) |

|`PUT/PATCH` | \* `PUT` Usually replaces an entire resources, whereas `PATCH` usually is for partial updates |

|`DELETE` |
Delete data (Delete) |

## Request URL

<p>In addition to a request method, a request must inclyde a <b>request URL</b> that indicates <i>where</i> to make the API call. A request URL has three parts: a <b>protocol</b>  (such as <code>http://</code> or <code>https://</code> ), <b>host</b> (location of the server)m and <b>path</b> (route on the server). In REST APIs, the path often points to a reference entity, like "books" </p>

---

| Protocol | Host | Path |

|`https://` | `library-api.postmanlabs.com` | `	/books` |

## Reponses status codes

Status codes have conventions. For example, any status code starting with a "2xx" (a "200-level reponse") represents a successful call.

| Code range | Meaning      | Example                        |
| ---------- | ------------ | ------------------------------ |
| `2xx`      | success      | `200` - OK                     |
|            |              | `201` - Created                |
|            |              | `204` - No content (silent OK) |
|            |
|            |
| `3xx`      | Redirection  | `301` - Moved (path changed)   |
| `4xx`      | Client Error | `400` - Bad request            |
|            |              | `401` - Unauthorized           |
|            |              | `403` - Not Permitted          |
|            |              | `404` - Not Found              |
| `5xx`      | server error | `500` - Internal Server Error  |
|            |              | `502` - Bad Gateway            |
|            |              | `504` - Gateway timeout        |

## Request-Response Pattern

Request-Response patterns are representations that shows how computers communicate over a newtwork. An API is the interface that lets us know what kind of response to expext when we make certain calls to the server.

In API calls there are 3 bodies involved.

1. <b>CLIENT</b> : The <b>client</b> is the agent making a request. A client could be a browser or an application you have coded, for example. In our case Postman is the client because that's how we sent the request.

2. The <b>request</b> is sent over a <b>NETWORK</b> to some <b>server</b> . In our case, we made a request over the public internet to a server located at the address `https://library-api.postmanlabs.com`

3. <b>THE SERVER</b> interprets the request (`GET/books`) and sent the appropriate <b>response over the newtwork back to the Postman client: a list of books</b>
