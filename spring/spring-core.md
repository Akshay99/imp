# Spring Core

## Overview
Spring Core is the foundation of the Spring ecosystem. It provides dependency injection, inversion of control, and bean management for enterprise applications.

## Key Concepts
- Inversion of control
- Dependency injection
- Bean lifecycle
- ApplicationContext and BeanFactory
- Bean scopes
- Autowiring

## Frequently Asked Interview Questions
1. What is dependency injection?
2. What is the difference between `@Component`, `@Service`, and `@Repository`?
3. What are bean scopes in Spring?
4. What is constructor injection?

## Answers
Dependency injection allows objects to receive their dependencies from the container rather than creating them themselves. `@Component` is a generic stereotype, while `@Service` and `@Repository` communicate intent. Bean scopes include singleton, prototype, request, session, and application. Constructor injection is preferred because it makes dependencies explicit and immutable.

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
- Keep configuration explicit and readable.
- Avoid unnecessary circular dependencies.

## Common Mistakes
- Overusing field injection.
- Not understanding bean lifecycle behavior.
- Creating tightly coupled components.

## Real-World Scenarios
A Spring application can wire controllers, services, and repositories together while keeping each layer loosely coupled.
