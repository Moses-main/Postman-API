# Variables and scripting

Remember, Postman allows you to save values as variables so that you can

1. Reuse values to keep your work DRY (don't repeat yourself)
2. Hide sensitive values like API keys from being shared publicly.

## Variable scope

Variable can be set to live in various scopes. Postman will resolve to the value at the nearest and narrowest scope.

From broadest to narrowest, these scopes are <b>global, collection, environment, data and local</b>

If a variable with the same name is declared in two different scopes, the value stored in the variable with the narrowest scope will be used. For example, if there is a global variable with the named <b>username</b> and a local variable named <b>username</b>, the local variable will be used when the request runs.

## Setting variables programmatically.

### Scripting in Postman

Postman allows you to add automation and dynamic behaviors to your collections with scripting.

Postman will automatically execute any provided scripts during two events in the request flow.

1. Immediately before a request is sent: pre-request script (<b>Pre-request Script</b> tab of request).

2. Immediately after a response comes back: test script (<b>Tests</b> tab of request).

### The `pm` object

The `pm` object is a helper object that gives access to data about your postman environment, request, response, variables and testing utilities.

For example, you can access the JSON response body from an API with:

`pm.response.json()`.

You can also programmatically get collection variables like the value of `baseUrl` with `pm.collectionVariables.get("baseUrl")`

In addition to getting variables, you can also set them with `pm.collectionVariables.set("variableName","variableValue")` like this:

`pm.collectionVariables.set("myVar","foo")`
