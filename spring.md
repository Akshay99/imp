# Spring

## Overview
Spring is a comprehensive framework for building Java applications. It provides IoC/DI, a modular architecture, and integrations for web, data access, security, and more. The consolidated notes below combine the key concepts, examples, best practices, and detailed answers from the original Spring topic files.

---

## Spring Core

### Overview
Spring Core is the foundation of the Spring ecosystem. It manages object creation, dependency wiring, and lifecycle.

### Key Concepts
- Inversion of control
- Dependency injection
- Bean lifecycle
- ApplicationContext and BeanFactory
- Bean scopes
- Autowiring

### Detailed Notes
- Dependency injection: Spring provides dependencies instead of objects constructing them, reducing coupling and improving testability.
- Stereotypes: `@Component` is generic; `@Service` and `@Repository` indicate intent and can influence tooling and exception translation.
- Bean scopes: `singleton` (default), `prototype`, and web scopes like `request` and `session`.
- Constructor injection preferred for explicit dependencies and final fields; avoids hidden mutability.
- `BeanFactory` is the basic container; `ApplicationContext` adds resource loading, events, and integration features.
- Bean lifecycle: constructor -> dependency injection -> `@PostConstruct` -> initialized -> `@PreDestroy` on shutdown.

### Best Practices
- Prefer constructor injection.
- Keep configuration explicit.
- Avoid field injection and circular dependencies.

---

## Spring Boot

### Overview
Spring Boot reduces setup overhead with auto-configuration, starters, and embedded servers.

### Key Concepts
- Auto-configuration
- Starter dependencies
- Embedded server
- Profiles
- Actuator
- Externalized configuration

### Notes
- Auto-configuration inspects classpath and config to create beans automatically.
- `application.properties`/`application.yml` centralizes runtime configuration.
- Profiles (`dev`, `test`, `prod`) let you switch environment-specific settings.
- `@SpringBootTest` loads the full context for integration tests; unit tests are faster and scope-limited.

### Best Practices
- Use the right starters.
- Externalize secrets and configs.
- Monitor startup and health with Actuator.

---

## Spring MVC

### Overview
Spring MVC handles web request mapping, validation, and response rendering for web apps and REST APIs.

### Key Concepts
- Controllers and request mapping
- Request parameters and path variables
- Models and views
- Validation and exception handling
- `@RequestBody` and `@ResponseBody`

### Notes
- Use `@RestController` for JSON APIs (combines `@Controller` + `@ResponseBody`).
- Use DTOs and `@Valid` for validation; keep controllers thin and delegate business logic to services.

---

## Spring Data JPA

### Overview
Simplifies database access via repository abstractions, query derivation, and transaction management.

### Key Concepts
- Entities and repositories
- Derived query methods
- Transactions
- Lazy vs eager loading
- JPQL and native queries

### Notes
- JPA is a spec; Hibernate is a common implementation.
- `findById` loads eagerly; `getReference` may return a proxy (lazy access).
- Watch N+1 problems; use projections, joins, and DTOs to control data fetched.

---

## Spring Security

### Overview
Framework for authentication, authorization, and request-level security controls.

### Key Concepts
- Authentication and authorization
- Filters and security chain
- Roles and permissions
- JWT and OAuth2 basics
- CSRF protection

### Notes
- Prefer stateless JWT for APIs; always use HTTPS and proper token validation.
- Hash passwords (BCrypt/PBKDF2) and limit exposure of sensitive endpoints.

---

## Spring & Microservices

### Overview
Spring Boot pairs well with microservices due to lightweight startups, integrations, and cloud-ready tooling.

### Key Concepts
- Service boundaries
- API gateway
- Service discovery
- Resilience and circuit breakers
- Distributed tracing

### Notes
- Design services for autonomy, observability, and eventual consistency; use message-driven approaches when appropriate.

---

## Code Examples (collected)

```java
@Component
public class GreetingService {
    public String greet() { return "Hello"; }
}

@SpringBootApplication
public class App {
    public static void main(String[] args) {
        SpringApplication.run(App.class, args);
    }
}

@RestController
public class UserController {
    @GetMapping("/users/{id}")
    public User getUser(@PathVariable Long id) { return new User(id, "Alice"); }
}
```

---

## Best Practices (summary)
- Prefer constructor injection and explicit configuration.
- Keep controllers thin and services responsible for business logic.
- Externalize configuration and use profiles for environment differences.
- Monitor health and metrics in production.

---

---

## Interview Questions (Spring & Java)

### Spring - Core
1. What is dependency injection?
2. What is IoC (Inversion of Control) and how does it differ from DI?
3. What are the types of dependency injection (constructor, setter, field)?
4. Why prefer constructor injection over field injection?
5. How does Spring detect and resolve circular dependencies?
6. What is the difference between `@Bean` and `@Component`?
7. What are common bean scopes in Spring (singleton, prototype, request, session)?
8. Explain the Spring bean lifecycle (constructor, injection, `@PostConstruct`, init, `@PreDestroy`).
9. What is `@Qualifier` vs `@Primary` and when to use them?
10. What is `@Lazy` and lazy initialization?

### Spring Boot
1. What is the advantage of Spring Boot over traditional Spring?
2. What is auto-configuration and how does it work?
3. What are starter dependencies?
4. How do profiles (`dev`, `test`, `prod`) help in deployment?
5. What is the role of `application.properties` / `application.yml`?
6. What is `@SpringBootTest` and how is it different from unit tests?

### Spring MVC
1. What is the role of `@Controller`?
2. What is `@RestController` and how does it differ from `@Controller`?
3. How do `@GetMapping`, `@PostMapping` and request mappings work?
4. What is the difference between `@RequestBody` and `@ModelAttribute`?
5. How do you validate user input with `@Valid` and DTOs?
6. Why should controllers remain thin and delegate business logic?

### Spring Data JPA
1. What is the difference between JPA and Hibernate?
2. What is the difference between `findById` and `getReference`?
3. What is lazy loading and how can it cause the N+1 problem?
4. How do you avoid fetching too much data (projections, DTOs, joins)?
5. How does transaction management work in Spring?
6. When to use JPQL vs native queries?

### Spring Security
1. What is the difference between authentication and authorization?
2. How does JWT-based authentication work?
3. What is CSRF and how is it mitigated?
4. How do you secure REST APIs (HTTPS, tokens, scopes)?
5. Why should passwords be hashed (BCrypt, PBKDF2)?
6. Difference between roles and permissions?

### Spring & Microservices
1. What are the advantages of microservices and why use Spring Boot for them?
2. What are common challenges of microservices (operational complexity, data consistency)?
3. What is an API gateway and when to use one?
4. How do you handle eventual consistency between services?
5. Why is observability (logs, metrics, tracing) important?
6. When to choose synchronous vs asynchronous communication?

---

### Core Java
1. What is the difference between abstraction and encapsulation?
2. What is method overloading vs method overriding?
3. What is the difference between `==` and `.equals()` for objects?
4. Why are strings immutable in Java?
5. What is the difference between checked and unchecked exceptions?
6. Why is composition often preferred over inheritance?

### Collections
1. What is the difference between `ArrayList` and `LinkedList`?
2. When should you use `HashMap` instead of `TreeMap`?
3. What is the difference between `HashSet` and `TreeSet`?
4. How does `ConcurrentHashMap` achieve thread-safety and scalability?
5. What is the difference between `Comparable` and `Comparator`?
6. Why should you avoid modifying a collection while iterating?

### Multithreading
1. What is the difference between `Runnable` and `Callable`?
2. What is a deadlock and how can it be prevented?
3. What is the difference between `wait()` and `sleep()`?
4. How does `ExecutorService` help manage concurrency?
5. What are race conditions and how to avoid them?
6. Why are immutable objects useful in multithreaded code?

### JVM Internals
1. What is the difference between heap and stack memory?
2. What is garbage collection and how does it work?
3. What are common GC algorithms/collectors (Serial, Parallel, CMS, G1)?
4. Why is the JVM platform-independent?
5. What is the role of the JIT compiler?
6. What are trade-offs of `new` vs object pooling?

### Java 8
1. What is a lambda expression and when to use it?
2. What is the difference between a stream and a collection?
3. Why is `Optional` used and how to use it properly?
4. When would you use `flatMap` vs `map`?
5. Why are streams lazy and what are the implications?
6. What are best practices when using parallel streams?

### Design Patterns
1. What is the difference between a factory and a builder?
2. When is a singleton appropriate and what are its drawbacks?
3. How does dependency injection relate to design patterns?
4. When to use strategy vs template method?
5. What is the open-closed principle and why it matters?
6. Difference between adapter and facade?

---

File merged and consolidated into this single `spring.md` file at repository root.
