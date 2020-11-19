---
description: >-
  The server issuing access tokens to the client after successfully
  authenticating the resource owner and obtaining authorization.
---

# Authorization Server \(Keycloak\)

## **Keycloak**

Keycloak is an open-source Identity and Access Management solution administered by RedHat, and developed in Java by JBoss. More documentation about Keycloak can be found [here](https://www.keycloak.org/). A code sample of an embedded server \(Spring Boot\) can be found [here](https://github.com/Baeldung/spring-security-oauth/tree/master/oauth-rest/oauth-authorization-server).

**Note:** the server could be running on a VM or something in a standalone mode and configured using the Admin Console. This process is described [here](https://www.keycloak.org/docs/latest/server_admin/). I chose de deploy it in a Spring Boot embedded application to make the deployment process easier.

## **Configuration in the Admin Console**

Some core concepts need to be understood to configure the server properly. They are explained [here](https://www.keycloak.org/docs/latest/server_admin/#core-concepts-and-terms).

The embedded server is created using a realm import file. The file is in the project repository and can be found in resources/journal-de-bord-realm.json file.

### **Identity Providers**

I would like to enable login with Google. [Here](https://www.keycloak.org/docs/6.0/server_admin/#google) are the steps to follow.

It is possible to add a Google button, resources are provided by Google [here](https://developers.google.com/identity/branding-guidelines).

https://developers.google.com/identity/sign-in/web/build-button

### **Theme customization**

It is possible to customize the look and feel of the Keycloak GUI. Here are two key tutorials:

* [https://www.baeldung.com/spring-keycloak-custom-themes](https://www.baeldung.com/spring-keycloak-custom-themes) \(explains how theme are added in an embedded server\)
* [https://www.baeldung.com/keycloak-custom-login-page](https://www.baeldung.com/keycloak-custom-login-page) \(customize the login page\)

Pour modifier la page il suffit de copier le style de base \(que l’on trouve [ici](https://github.com/keycloak/keycloak/tree/master/themes/src/main/resources/theme/base)\), la documentation officielle sur les themes est [ici](https://github.com/keycloak/keycloak-documentation/blob/master/server_development/topics/themes.adoc).

https://developers.google.com/identity/sign-in/web/build-button

## **Deployment**

[**https://elements.heroku.com/buttons/mieckert/keycloak-heroku**](https://elements.heroku.com/buttons/mieckert/keycloak-heroku)

### Environment variables

The server configuration is the following…

![](https://lh6.googleusercontent.com/tCjJYtWHv7LoZZTf9cN16ENI8Z25R8h6JTxGbUmR2SPEGmyIvTSoGRwBFpD-zPswRkyE07pxCTW9MjQ5crzATvsw7qt8iZJOVDAJaa0HMkIGH1dWWRpHtbB5nvp4dhnST0m90lx_)

