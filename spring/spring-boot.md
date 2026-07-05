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

## Spring Core Interview Questions

### 1. Spring Container & IoC
- What is Spring Framework?
- What is the Spring Container?
- What is IoC (Inversion of Control)?
- What is Dependency Injection?
- Difference between IoC and DI?
- What are the types of DI?
- Constructor Injection vs Setter Injection
- Why is Constructor Injection preferred?
- What happens if there are multiple constructors?
- What is field injection and why is it discouraged?

Advanced:
- How does Spring create objects?
- How does Spring resolve dependencies?
- How does Spring detect circular dependencies?
- Why does constructor injection fail for circular dependencies?
- How does Spring know which bean to inject?

### 2. Spring Bean Basics
- What is a Bean?
- Difference between Java object and Spring Bean?
- How are beans created?
- What is BeanFactory?
- What is ApplicationContext?
- Difference between BeanFactory and ApplicationContext?
- What are singleton beans?
- What are prototype beans?
- Can you manually create beans?
- Difference between @Bean and @Component?

### 3. Bean Lifecycle ⭐⭐⭐
- Explain Spring Bean Lifecycle.
- Which comes first, constructor or @PostConstruct?
- When is dependency injection performed?
- When is @Autowired executed?
- Difference between constructor and @PostConstruct?
- Difference between @PostConstruct and initMethod?
- Difference between destroy() and @PreDestroy?
- What if initialization fails?
- Can bean lifecycle be customized?
- Which interfaces participate in lifecycle?

### 4. Bean Scopes
- Singleton
- Prototype
- Request
- Session
- Application
- WebSocket

Questions:
- Default bean scope?
- Singleton vs Prototype?
- Can Singleton contain Prototype?
- How to inject Prototype into Singleton?
- Lifecycle difference between Singleton and Prototype?
- Which scopes exist only in web applications?

### 5. Bean Creation
- How does Spring discover beans?
- What is Component Scanning?
- What packages are scanned?
- Can scanning be customized?
- What happens if same bean name exists?
- How does Spring create @Configuration classes?

### 6. Bean Annotations
- @Component
- @Service
- @Repository
- @Controller
- @RestController

Interview:
- Difference among them?
- Are they functionally different?
- Why use @Repository?
- What exception translation happens?

### 7. Dependency Injection
- @Autowired
- @Inject
- @Resource

Difference:
- Constructor
- Setter
- Field

Advanced:
- Required=false
- Optional dependency
- Lazy dependency

### 8. @Qualifier / @Primary
- What happens if two beans have same type?
- How does Spring decide?
- Difference between @Primary and @Qualifier?
- Which has higher priority?
- Can multiple qualifiers exist?
- Custom qualifier?

Example:
```
interface Payment {}
@Component
class Paypal implements Payment {}
@Component
class Stripe implements Payment {}
@Service
class Checkout {
    @Qualifier("stripe")
    private Payment payment;
}
```

### 9. @Bean vs @Component
- Difference?
- Which is preferred?
- When to use @Bean?
- Third-party library registration?
- Can @Bean return interface?
- Can @Bean create multiple instances?

### 10. Bean Initialization
- @PostConstruct
- InitializingBean
- initMethod

Difference:
- Which executes first?
- Can multiple init methods exist?

### 11. Bean Destruction
- @PreDestroy
- DisposableBean
- destroyMethod

Advanced:
- Prototype bean destruction?
- When destroy methods are skipped?

### 12. BeanPostProcessor ⭐⭐⭐
- What is BeanPostProcessor?
- Why is it used?
- Before initialization?
- After initialization?
- Real examples?
- How Spring AOP uses it?
- How proxies are created?

### 13. BeanFactoryPostProcessor
- Difference from BeanPostProcessor?
- When executed?
- Can bean definitions change?
- Why execute before beans?

### 14. Aware Interfaces
- BeanNameAware
- BeanFactoryAware
- ApplicationContextAware
- EnvironmentAware
- ResourceLoaderAware

Interview:
- Why are they called Aware?
- When invoked?

### 15. Lazy Initialization
- What is @Lazy?
- Benefits?
- Drawbacks?
- Lazy singleton?
- Lazy dependency?

### 16. Circular Dependency
- Why does setter injection work?
- Why constructor injection fails?
- How Spring solves it?
- How to avoid circular dependency?

### 17. Singleton Internals
- Are singleton beans thread-safe?
- Can singleton hold state?
- Why avoid mutable fields?
- Difference between singleton bean and singleton design pattern?

### 18. Bean Naming
- Default bean name?
- Custom bean name?
- Duplicate names?
- Bean aliases?

### 19. Configuration
- @Configuration
- @Bean
- proxyBeanMethods
- Full vs Lite configuration
- CGLIB enhancement

### 20. Profiles
- @Profile
- Multiple profiles
- Default profile
- Active profile
- Environment-specific beans

### 21. Conditional Beans
- @Conditional
- @ConditionalOnMissingBean
- @ConditionalOnProperty
- @ConditionalOnClass
- @ConditionalOnBean

### 22. Spring Boot Auto Configuration
- What is Auto Configuration?
- @EnableAutoConfiguration
- @SpringBootApplication
- How does Spring Boot know which beans to create?
- How can auto configuration be disabled?
- Order of auto configuration?

### 23. Factory Beans
- FactoryBean vs BeanFactory
- Why FactoryBean?
- Object creation process
- getObject()

### 24. Proxy Questions
- Why proxies?
- JDK proxy
- CGLIB proxy
- When each is used?
- Does Spring proxy every bean?

### 25. Common Tricky Questions
- Does Spring create all beans at startup?
- Why isn't `@Autowired` needed on a single constructor?
- Can `final` fields be injected?
- Can static fields be injected?
- Can private fields be injected?
- Can interfaces be beans?
- Can abstract classes be beans?
- Why doesn't `@PostConstruct` run on manually created objects (`new MyClass()`)?
- Why doesn't `@Transactional` work when calling a method from the same class?
- What happens if two beans have the same name?
- What is the difference between eager and lazy initialization?
- Can one bean have multiple scopes?
- Is `ApplicationContext` thread-safe?
- Can a bean be reinitialized?
- What happens if a bean throws an exception during startup?

## Real-World Scenarios
A REST API service can start quickly with an embedded server, use profiles for different environments, and expose health and metrics endpoints for monitoring.
