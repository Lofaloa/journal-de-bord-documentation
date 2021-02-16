---
description: This page covers the development process of the Journal de bord REST API.
---

# Development

## Configuration

```yaml
spring:
  security:
    oauth2:
      resourceserver:
        jwt:
          issuer-uri: <authorization-server-host>
          jwk-set-uri: <authorization-server-public-keys-endpoint>
  datasource:
    url: jdbc:h2:mem:<name>
    driverClassName: org.h2.Driver
    username: <username>
    password: <password>
  jpa:
    database-platform: org.hibernate.dialect.H2Dialect
  h2:
    console:
      enabled: true
```

## Security

The application can be tested using the [Postman](https://www.postman.com/) application.

{% embed url="https://www.baeldung.com/postman-keycloak-endpoints" caption="This tutorial is great to both review the the usage of Postman with the Authorization code flow. " %}

{% embed url="https://learning.postman.com/docs/sending-requests/authorization/\#authorization-code" %}

{% embed url="https://github.com/postmanlabs/postman-app-support/issues/7700" %}



## In-memory database

The application uses a H2 in-memory database. You can access using the admin console at the &lt;host&gt;/h2-console endpoint.







