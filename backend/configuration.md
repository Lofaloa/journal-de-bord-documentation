# Configuration

## Security

The Spring Boot application resources are secured using the Keycloak management system. This section summarizes the steps described in this tutorial: [setup the resource server](https://www.baeldung.com/spring-boot-keycloak).

### Keycloak server configuration

1. Create a client
2. Create a new role

### Dependency

The [keycloak-spring-boot-started](https://mvnrepository.com/artifact/org.keycloak/keycloak-spring-boot-starter) is a required dependency and should be added to the project pom.xml file.

```text
<dependencies>
    ...
    <dependency>
        <groupId>org.keycloak</groupId>
        <artifactId>keycloak-spring-boot-starter</artifactId>
        <version>11.0.2</version>
    </dependency>
</dependencies>
<dependencyManagement>
    <dependencies>
        <dependency>
            <groupId>org.keycloak.bom</groupId>
            <artifactId>keycloak-adapter-bom</artifactId>
            <version>11.0.2</version>
            <type>pom</type>
            <scope>import</scope>
        </dependency>
    </dependencies>
</dependencyManagement>
```

### Project properties



