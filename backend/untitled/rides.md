---
description: Reference for the API endpoints related to the rides.
---

# Rides

{% api-method method="get" host="https://journal-de-bord-api.app" path="/api/drivers/rides" %}
{% api-method-summary %}
Get Cakes
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="page" type="number" required=false %}
The index of the page to get.
{% endapi-method-parameter %}

{% api-method-parameter name="size" type="string" %}
The number of rides that are in the page.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {Access token \(J.W.T.\)}
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```
{
    "rides": [...],
    "totalPages": <number of available pages>,
    "isLastPage": <true is the page is last>
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=403 %}
{% api-method-response-example-description %}
The logged user cannot access the specified driver.
{% endapi-method-response-example-description %}

```
{
    "timestamp": "2021-03-27T08:47:41.332+00:00",
    "status": 403,
    "error": "Forbidden",
    "message": "",
    "path": "/api/drivers/differentDriverIdentifier/rides"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Could not find a driver with the given identifier.
{% endapi-method-response-example-description %}

```
{
    "timestamp": "2021-03-27T22:37:02.071+00:00",
    "status": 404,
    "error": "Not Found",
    "message": "Unknown driver with id: dfgdfgd.",
    "path": "/api/drivers/dfgdfgd/rides"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



