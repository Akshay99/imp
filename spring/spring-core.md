# Spring Core

## Overview
Spring Core is the foundation of the Spring ecosystem. In interviews, a strong answer should explain how Spring manages object creation, dependency wiring, and lifecycle.

## Key Concepts
- Inversion of control
- Dependency injection
- Bean lifecycle
- ApplicationContext and BeanFactory
- Bean scopes
- Autowiring

## Frequently Asked Interview Questions (moved to spring-questions.md)

## Detailed Answers
### 1) Dependency injection
Dependency injection means Spring provides dependencies instead of the object constructing them itself. This reduces tight coupling and makes code easier to test.

### 2) Stereotypes
`@Component` is generic, while `@Service` and `@Repository` communicate intent. They are often used to make code easier to understand and to allow targeting of specific beans in configuration.

### 3) Bean scopes
Bean scopes define how long a bean lives. Singleton is the default and creates one instance per container; prototype creates a new instance each time one is requested.

### 4) Constructor injection
Constructor injection is preferred because dependencies are explicit and final fields can be safely set once. It also improves readability and testability.

### 5) BeanFactory vs ApplicationContext
`BeanFactory` is the basic container, while `ApplicationContext` is a richer container with features like internationalization, resource loading, event propagation, and easier integration.

### 6) Loosely coupled design
Spring reduces coupling by letting components depend on abstractions rather than concrete implementations. This makes changes safer and testing simpler.

## Code Examples
```java
@Component
public class GreetingService {
    public String greet() {
        return "Hello";
    }
}
```

## Best Practices
- Prefer constructor injection.
- Keep configuration explicit.
- Avoid unnecessary circular dependencies.

## Common Mistakes
- Overusing field injection.
- Not understanding bean lifecycle behavior.
- Creating tightly coupled components.

## Real-World Scenarios
A Spring application may wire controllers, services, repositories, and external clients together while keeping each piece testable and independently changeable.
