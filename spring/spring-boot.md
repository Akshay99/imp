# Spring Boot

## Overview
Spring Boot accelerates application development by providing sensible defaults, embedded servers, and auto-configuration.

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

## Answers
Spring Boot reduces setup code and allows applications to run with minimal configuration. Auto-configuration detects dependencies and wires beans automatically. Profiles let you run different configurations for development, testing, and production. `application.properties` or YAML files define environment-specific behavior.

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
- Externalize secrets and configuration.
- Use health checks and metrics in production.

## Common Mistakes
- Confusing default configuration with correct configuration.
- Forgetting to monitor startup logs.
- Overriding defaults without understanding them.

## Real-World Scenarios
A REST API can start quickly with embedded Tomcat, use profiles for environment-specific settings, and expose health endpoints for monitoring.
