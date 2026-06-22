# Spring Boot

## Overview
Spring Boot reduces setup overhead and helps teams ship applications faster. Interviewers often ask about auto-configuration, starter dependencies, profiles, and production readiness.

## Key Concepts
- Auto-configuration
- Starter dependencies
- Embedded server
- Profiles
- Actuator
- Externalized configuration

## Frequently Asked Interview Questions
1. What is the advantage of Spring Boot over traditional Spring?
2. What is auto-configuration?
3. How do profiles help in deployment?
4. What is the role of `application.properties`?
5. Why is Spring Boot useful for microservices?
6. What is the difference between `@SpringBootTest` and unit tests?

## Detailed Answers
### 1) Advantage over traditional Spring
Spring Boot removes much of the repetitive setup work and provides sensible defaults. This lets developers focus on business logic instead of wiring components manually.

### 2) Auto-configuration
Auto-configuration looks at the dependencies on the classpath and creates appropriate beans automatically. It is one of the main reasons Spring Boot reduces configuration complexity.

### 3) Profiles
Profiles allow different configuration values for different environments such as dev, test, and prod. This keeps secrets and environment-specific settings organized.

### 4) `application.properties`
This file stores configuration values such as server port, database settings, and feature toggles. It is a central place for runtime configuration.

### 5) Spring Boot and microservices
Spring Boot is ideal for microservices because it is lightweight, starts quickly, and integrates well with tools like Docker, Kubernetes, and Spring Cloud.

### 6) `@SpringBootTest` vs unit tests
Unit tests focus on a small piece of logic. `@SpringBootTest` loads the application context and validates how components interact together.

## Code Examples
```java
@SpringBootApplication
public class App {
    public static void main(String[] args) {
        SpringApplication.run(App.class, args);
    }
}
```

## Best Practices
- Use the correct starter dependencies.
- Externalize configuration and secrets.
- Use health checks and metrics in production.

## Common Mistakes
- Confusing default configuration with correct configuration.
- Forgetting to monitor startup logs.
- Overriding defaults without understanding them.

## Real-World Scenarios
A REST API service can start quickly with an embedded server, use profiles for different environments, and expose health and metrics endpoints for monitoring.
