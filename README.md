# Service Discovery (Eureka Server)

This module provides a centralized **Eureka Service Registry**, enabling dynamic service discovery and registration for all microservices in the system. It is the core of service communication in this Spring Cloud-based microservices architecture.

## Features

- Centralized service registry using **Eureka**
- Enables dynamic service discovery for microservices
- Supports horizontal scaling of services
- Provides a web dashboard to monitor registered instances
- Simple and lightweight

---

## Technologies

- **Java 17+**
- **Spring Boot 3**
- **Spring Cloud Netflix Eureka Server**

---

## Configuration Overview

### `application.yml`

```yaml
server:
  port: 8761

spring:
  application:
    name: service-discovery

eureka:
  client:
    register-with-eureka: false
    fetch-registry: false
```

- register-with-eureka: false: The Eureka server does not register itself.

- fetch-registry: false: The Eureka server does not fetch other instances (it's the source of truth).

