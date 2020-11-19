# OAuth 2.0

## Introduction

I have found two tutorials explaining how to implement OAuth 2.0 authentication with Spring Boot. Here is the tutorial provided by [spring official documentation](https://spring.io/guides/tutorials/spring-boot-oauth2/) and here is one provided by [OAuth documentation](https://auth0.com/blog/securing-spring-boot-apis-and-spas-with-oauth2/).

Different flows exist for an OAuth authentication. The official documentation advises to use the Authorization Code Flow with Proof Key for Code Exchange \([source](https://auth0.com/docs/authorization/which-oauth-2-0-flow-should-i-use#is-the-client-a-single-page-app-)\). The documentation describes the flow [here](https://auth0.com/docs/flows/authorization-code-flow-with-proof-key-for-code-exchange-pkce) \(it presents some links to the Auth0 SDK\) and the reference is [here](https://tools.ietf.org/html/rfc7636).

I will be using the [authorization code flow](https://oauth.net/2/grant-types/authorization-code/). The implementation follows these [tutorials and code samples](https://www.baeldung.com/rest-api-spring-oauth2-angular).

## **Useful resources**

{% embed url="https://www.youtube.com/watch?v=996OiexHze0" %}

\*\*\*\*

* [**OAuth 2.0 in Spring Boot**](https://spring.io/guides/tutorials/spring-boot-oauth2/)
* [**OAuth 2.0 reference**](https://tools.ietf.org/html/rfc6749#section-4)
* [**OpenID Connect \| Google Identity Platform**](https://developers.google.com/identity/protocols/oauth2/openid-connect)
* [**Using Postman to access OAuth 2.0 Google APIs**](https://stackoverflow.com/questions/32076503/using-postman-to-access-oauth-2-0-google-apis)
* [**REST API Security Essentials - REST API Tutorial**](https://restfulapi.net/security-essentials/)



 ****[**reference**](https://tools.ietf.org/html/rfc6749)

