---
description: Reference for the API endpoints related to the drivers.
---

# Drivers

{% api-method method="post" host="https://journal-de-bord-api.app" path="/api/drivers" %}
{% api-method-summary %}
Create a driver
{% endapi-method-summary %}

{% api-method-description %}
Create a new driver. You need to create a new driver to create a new journal.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Content-Type" type="string" required=false %}
application/json
{% endapi-method-parameter %}

{% api-method-parameter name="Authentication" type="string" required=true %}
Authentication token \(J.W.T.\): the authenticated user will be set as the owner of the driver resource.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="identifier" type="string" required=false %}
This is a unique string. This should be the user identifier provided by the authorization server.
{% endapi-method-parameter %}

{% api-method-parameter name="objective" type="number" required=true %}
This is the number of kilometres the drivers wants to reach at the end of his training.
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=201 %}
{% api-method-response-example-description %}
The driver was successfully created.
{% endapi-method-response-example-description %}

```
Empty body.
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
The request body was not valid or the authentication header was omitted.
{% endapi-method-response-example-description %}

```
{
    "timestamp": "2021-03-27T08:31:39.150+00:00",
    "status": 400,
    "error": "Bad Request",
    "message": "",
    "path": "/api/drivers"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=409 %}
{% api-method-response-example-description %}
Could not create a new driver because the authenticated user was already created.
{% endapi-method-response-example-description %}

```
{
    "timestamp": "2021-03-27T08:31:02.417+00:00",
    "status": 409,
    "error": "Conflict",
    "message": "",
    "path": "/api/drivers"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=422 %}
{% api-method-response-example-description %}
The identifier was specified in the request body but the logged user identifier does not match. This makes sure that the user can only create a driver for itself.
{% endapi-method-response-example-description %}

```
{
    "timestamp": "2021-03-27T08:32:04.883+00:00",
    "status": 422,
    "error": "Unprocessable Entity",
    "message": "",
    "path": "/api/drivers"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="" path="" %}
{% api-method-summary %}
Get a driver
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="" type="string" required=false %}

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

