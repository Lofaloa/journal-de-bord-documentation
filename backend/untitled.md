# REST API map

{% embed url="https://cheatsheetseries.owasp.org/cheatsheets/REST\_Security\_Cheat\_Sheet.html" %}

[**How to design a REST API**](https://restfulapi.net/rest-api-design-tutorial-with-example/)

{% api-method method="post" host="http://example.backend.com" path="/api/drivers/{pseudonym}/rides" %}
{% api-method-summary %}
Create a new ride
{% endapi-method-summary %}

{% api-method-description %}
This endpoint can be used to start a new ride without knowing a thing about the arrival. For instance, a web client could have the following flow: \(1\) the user start a new ride; \(2\) the user quits the app and drives; \(3\) the user opens the app and finishes the track.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="odometerValue" type="number" required=true %}
This is the value shown by the odometer of the vehicle at start. 
{% endapi-method-parameter %}

{% api-method-parameter name="" type="number" required=true %}
This is the identifier of the start location.
{% endapi-method-parameter %}

{% api-method-parameter name="moment" type="string" required=true %}
It is date represented by a string using the ISO 8601 standard. This is the start moment of the newly created ride. 
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=201 %}
{% api-method-response-example-description %}
The start has been created successfully. A new entry is created in the database. The new entity has no information concerning the arrival and is ready to be finished.
{% endapi-method-response-example-description %}

```java

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

## **Resources**

* Drivers
  * Pseudonym
  * Password
  * Objective \(number of kilometers\)
* Rides
  * Departure \(stop id\)
  * Arrival \(stop id\)
  * Condition de circulation \(integer\)
  * Difficultés \(string\)
* Stops
  * Date and time \(timestamp\)
  * Location \(location identifier\)
  * Odometer value
* Locations
  * Name
  * Latitude
  * Longitude

## **Rides**

* Start a new ride and initialize it with a departure stop
  * Method: POST
  * URI: /api/drivers/{pseudonym}/rides
  * Argument: none.
  * Body \(JSON\): moment \(iso 8601\), location \(id\), odometerValue
  * Response:
    * 201: the ride has been started successfully
    * 422: a ride has already been started and the new ride cannot be started
    * 400: bad request
    * 404: the driver does not exist
* Get a driver rides
  * Method: GET
  * URI: /api/drivers/{pseudonym}/rides
  * Arguments: last \(boolean, optional\)
  * Body: empty.
  * Response:
    * 200: the server found the expected results
    * 400: bad request
    * 404: the driver does not exist
* Update a ride data
  * Method: PUT
  * URI: /api/drivers/{pseudonym}/rides/{identifier}
  * Arguments: none.
  * Body \(JSON\): arrival, departure, comment, trafficCondition, driverPseudonym.
  * Response:
    * 204: success
    * 400: bad request
    * 404: when the ride or the driver cannot be found
    * 422: if the new ride data isn’t valid.
* Delete a ride
  * Method: DELETE
  * URI: /api/drivers/{pseudonym}/rides/{identifier}
  * Arguments: none.
  * Body: empty.
  * Response:
    * 204: success
    * 400: bad request
    * 404: when the ride or the driver cannot be found

## **Security**

* **The frontend should be able to access on the behalf of the current user \(OAuth or J.W.T\).** 
* **The current user cannot access other users rides.**
* **The current user can access all its ride.**

[**Getting Started \| Securing a Web Application**](https://spring.io/guides/gs/securing-web/)

[**Protect REST APIs with Spring Security and JWT**](https://medium.com/@hantsy/protect-rest-apis-with-spring-security-and-jwt-5fbc90305cc5)

[**https://cheatsheetseries.owasp.org/cheatsheets/REST\_Security\_Cheat\_Sheet.html**](https://cheatsheetseries.owasp.org/cheatsheets/REST_Security_Cheat_Sheet.html)  


\*\*\*\*

