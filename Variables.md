# Variables in Postman

Postman allows you to save values as variables to reuse them and easily hide sensitive information like API Keys.

Once a variable is defined, you can access its value using double curly brace syntax like this: <b>{{variableName}} </b>

## Where are my variables?

You can find Collections variables in your collections

Click on your collections, then the <b>Variables</b> tab. Here you can view and edit your variables.

Note that there are two different columns:

<b>Initial Value</b> - the value initially set when someone forks or imports your collections.

<b>Current Value</b> - Postman always resolves the variable to this value. This is local to your Postman account and not public. It is good to keep secrets like API keys ONLY in this colunm and not include them in the Initial Value column.

## Query parameters syntax

Query parameters are added to the end of the path. They start with a question mark `?`, followed by the key-value pairs in the fomat: `<key>=<value>`. For example, this request might fetch all photos that have landscape orientation

`Get https://some-api.com/photo?orientiation=landscape`

If there are multiple query parameters, each is seperated by an ampersand `&`. Below two query parameters to specify the orientation and size of the photos to be returned.

`GET https://some-api.com/photo?orientation=&size=500x400`

#### Searching Google - with query parameters

`https://www.google.com/search?q=postman`

This request adds a search term as a query parameter `q=postman` ("q" refers to "query" here) to the `GET /search` path on Google's server.

Because this parameter is in our request, the server returns an HTML document that is a search results page with hits for "Postman".

You can change your search directly from the URL by changing the value of th query parameter `q=<something else!>`

### When to use query parameters?

Always use the query parameter.

Sometimes, query parameters are optional and allow you to add filters or extra data to your responses. Sometimes, they are required in order for the server to process your request. APIs are implemented differently to fulfill different needs.

The Postman Library API v2 allows you to add optional query parameters on requests to `GET/books` filter the books that come back in response.

### Path Variables

Another way of passing request data to an API is via <b>path variables</b>. (a.k.a path parameters). A path variable is a dynamic section of a patph and is oftwn used for IDs and entity names such as usernames.

#### Path Variables Syntax

The path variables comes immediately after a slash in the path. For exampls, the `Github API` allows you to search for Github users by providing a username in the path in place of `{username}` below

`GET https://api.github.com/users/{username}`

Making this API call with a value for `{username}` will fetch data about that user:

`GET https://api.github.com/users/postmanlabs`

#### Path vs. query parameters

| Path Variable                                                                             | Query Parameter                                                             |
| ----------------------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| ex: `/books/abc123`                                                                       | ex.`/books?search=borges&checkedOut=false`                                  |
| located <b>directly after a slash </b> in the path. I can <b> be anywhere on the path</b> | Located only at the <b> end of a path </b>, right after a question mark `?` |
| Accepts <b> dynamic values </b>                                                           | Accepts <b> defined query keys with potentially dynamic values</b>          |
| \* Often used for IDs or entity names                                                     | \* Often used for options and filters                                       |
|                                                                                           |                                                                             |

- These are just conventions ! Some APIs might ask you to pass an ID or username in a query parameter like this `/users?username=getpostman`

### When to use path variable?

<b>Always reas the API documentation</b> If a path parameter is required, the documentation will mention this.

Note that some API documentation uses <b>colon syntax</b> to represent a wildcard in the path lik `/users/:username`, while some user curly braces like `/users/{username}`. They both mean the same thing: that part of the path is dynamic.
