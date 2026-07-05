# Consolidated Spring Interview Questions

## Spring Core

1. What is dependency injection?
2. What is the difference between `@Component`, `@Service`, and `@Repository`?
3. What are bean scopes in Spring?
4. What is constructor injection?
5. What is the difference between BeanFactory and ApplicationContext?
6. Why is Spring considered loosely coupled?

### Expanded Spring Core Questions
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
- How does Spring create objects?
- How does Spring resolve dependencies?
- How does Spring detect circular dependencies?
- Why does constructor injection fail for circular dependencies?
- How does Spring know which bean to inject?
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
- Default bean scope?
- Singleton vs Prototype?
- Can Singleton contain Prototype?
- How to inject Prototype into Singleton?
- Lifecycle difference between Singleton and Prototype?
- Which scopes exist only in web applications?
- How does Spring discover beans?
- What is Component Scanning?
- What packages are scanned?
- Can scanning be customized?
- What happens if same bean name exists?
- How does Spring create @Configuration classes?
- @Component, @Service, @Repository, @Controller, @RestController — differences?
- Are they functionally different?
- Why use @Repository?
- What exception translation happens?
- @Autowired, @Inject, @Resource — differences?
- Required=false and optional dependency handling?
- Lazy dependency?
- What happens if two beans have same type?
- How does Spring decide which bean to inject?
- Difference between @Primary and @Qualifier?
- Which has higher priority?
- Can multiple qualifiers exist?
- Custom qualifier?
- @Bean vs @Component — when to use which?
- Which is preferred?
- Can @Bean return interface?
- Can @Bean create multiple instances?
- @PostConstruct, InitializingBean, initMethod — which runs first?
- @PreDestroy, DisposableBean, destroyMethod — lifecycle questions
- Prototype bean destruction — who is responsible?
- What is BeanPostProcessor and why is it used?
- Before initialization vs after initialization behavior?
- How Spring AOP uses BeanPostProcessor?
- BeanFactoryPostProcessor — difference from BeanPostProcessor?
- Aware interfaces: BeanNameAware, BeanFactoryAware, ApplicationContextAware, EnvironmentAware, ResourceLoaderAware — why and when invoked?
- What is @Lazy and when to use it?
- Circular Dependency: why setter injection works and constructor injection fails?
- Are singleton beans thread-safe?
- Can singleton hold state?
- Why avoid mutable fields in singleton beans?
- Default bean naming and aliases?
- @Configuration, @Bean, proxyBeanMethods, Full vs Lite configuration, CGLIB enhancement
- @Profile and profile-related questions
- @Conditional and conditional-on-* annotations
- Auto-configuration and @EnableAutoConfiguration
- FactoryBean vs BeanFactory
- Proxy questions: JDK proxy vs CGLIB proxy
- Tricky questions: @Transactional self-invocation, @Autowired on single constructor, final/static/private field injection, etc.

## Spring Boot

1. What is the advantage of Spring Boot over traditional Spring?
2. What is auto-configuration?
3. How do profiles help in deployment?
4. What is the role of `application.properties`?
5. Why is Spring Boot useful for microservices?
6. What is the difference between `@SpringBootTest` and unit tests?

## Spring MVC

1. What is the role of `@Controller`?
2. How does request mapping work?
3. What is the difference between `@RequestBody` and `@ModelAttribute`?
4. How do you validate user input?
5. Why should controllers stay thin?
6. What is the difference between `@RestController` and `@Controller`?

## Spring Data JPA

1. What is the difference between JPA and Hibernate?
2. What is the difference between `findById` and `getReference`?
3. What is lazy loading?
4. Why is transaction management important?
5. What is the N+1 problem?
6. How do you avoid fetching too much data?

## Spring Security

1. What is the difference between authentication and authorization?
2. How does JWT work?
3. What is CSRF?
4. How do you secure REST APIs?
5. Why should passwords be hashed?
6. What is the difference between roles and permissions?

## Microservices (related)

1. What are the advantages of microservices?
2. What are the challenges of microservices?
3. What is an API gateway?
4. How do you handle eventual consistency?
5. Why is observability important in microservices?
6. What is the difference between synchronous and asynchronous communication?

---

File generated by consolidation script.

## Other Topics

### Git
1. What is the difference between `git merge` and `git rebase`?
2. What is a pull request?
3. How do you resolve merge conflicts?
4. What is `git stash` used for?
5. Why is commit history important?
6. What is the difference between `git fetch` and `git pull`?

### RabbitMQ
1. What is the difference between direct and topic exchanges?
2. How do acknowledgements work?
3. What is a dead-letter queue?
4. When would you choose RabbitMQ over Kafka?
5. Why is idempotency important for consumers?
6. What happens if a consumer crashes after reading a message but before acknowledging it?

### Kafka
1. What is a partition in Kafka?
2. How do consumer groups work?
3. What is the difference between Kafka and RabbitMQ?
4. What is idempotence?
5. Why is ordering guaranteed only within a partition?
6. What is the role of offsets?

### Caching (Hazelcast)
1. What is a distributed map?
2. How does Hazelcast improve scalability?
3. What is a near cache?
4. When is Hazelcast useful?
5. Why is partitioning important?
6. How does Hazelcast handle cluster failures?

### Caching (Redis)
1. What is a cache hit vs cache miss?
2. How does Redis support pub/sub?
3. What is TTL?
4. When should Redis be used for locking?
5. Why is cache invalidation difficult?
6. What is the difference between persistence and durability?

### System Design (HLD)
1. What is the difference between HLD and LLD?
2. How do you choose between a monolith and microservices?
3. How do you ensure scalability?
4. What are the main trade-offs in architecture decisions?
5. Why is observability necessary?
6. How do you handle failure in distributed systems?

### System Design (LLD)
1. What is the difference between HLD and LLD?
2. How do you design a cache for a system?
3. How do you structure service classes?
4. How do you handle extensibility?
5. Why are interfaces useful in LLD?
6. How do you approach edge cases in design?

### Cloud (AWS)
1. What is the difference between EC2 and Lambda?
2. What is IAM?
3. How does S3 differ from EBS?
4. What is the role of a load balancer?
5. Why is least-privilege access important?
6. What is the difference between vertical and horizontal scaling?

### Docker
1. What is the difference between a container and a virtual machine?
2. What is a Dockerfile?
3. How do volumes help?
4. Why are multi-stage builds useful?
5. What is the difference between `COPY` and `ADD`?
6. Why is immutability important for containers?

### Kubernetes
1. What is the difference between a pod and a container?
2. What is a deployment?
3. What is the purpose of a service?
4. How do rolling updates work?
5. What is the difference between ConfigMap and Secret?
6. Why are readiness and liveness probes important?

### REST APIs
1. What is the difference between `PUT` and `PATCH`?
2. What are common HTTP status codes?
3. What is idempotency?
4. How do you version an API?
5. Why should APIs return consistent error structures?
6. What is pagination and why is it needed?

### Node.js
1. What is the event loop?
2. Why is Node.js non-blocking?
3. What is the difference between synchronous and asynchronous code?
4. How do you handle errors in Node.js?
5. Why is Node.js good for I/O-heavy applications?
6. What are streams used for?

### Core Java
1. What is the difference between abstraction and encapsulation?
2. What is method overloading vs overriding?
3. What is the difference between `==` and `.equals()`?
4. Why are strings immutable?
5. What is the difference between checked and unchecked exceptions?
6. Why is composition often preferred over inheritance?

### Design Patterns
1. What is the difference between a factory and a builder?
2. When should you use a singleton?
3. What is dependency injection?
4. How do you decide between strategy and template method?
5. Why is the open-closed principle important?
6. What is the difference between adapter and facade?

### JVM Internals
1. What is the difference between heap and stack memory?
2. What is garbage collection?
3. What are the major garbage collectors?
4. Why is the JVM platform-independent?
5. What is the role of the JIT compiler?
6. What is the difference between `new` object creation and object pooling?

### Multithreading
1. What is the difference between `Runnable` and `Callable`?
2. What is a deadlock?
3. What is the difference between `wait()` and `sleep()`?
4. How does `ExecutorService` help with concurrency?
5. What are race conditions?
6. Why are immutable objects useful in multithreaded code?

### Collections
1. What is the difference between `ArrayList` and `LinkedList`?
2. When should you use `HashMap` instead of `TreeMap`?
3. What is the difference between `HashSet` and `TreeSet`?
4. How does `ConcurrentHashMap` work?
5. What is the difference between `Comparable` and `Comparator`?
6. Why should you avoid modifying a collection while iterating?

### Frontend (TypeScript)
1. What is the difference between `interface` and `type`?
2. What are generics?
3. What is the benefit of type inference?
4. How does `unknown` differ from `any`?
5. What is a union type?
6. Why is TypeScript useful in large applications?

### Frontend (React)
1. What is the difference between props and state?
2. What are React hooks?
3. What is reconciliation?
4. How do you optimize React performance?
5. Why are keys important in lists?
6. What is the difference between controlled and uncontrolled components?

### Frontend (JavaScript)
1. What is a closure?
2. What is the difference between `var`, `let`, and `const`?
3. How does the event loop work?
4. What is the difference between promises and callbacks?
5. What is hoisting?
6. What is the difference between shallow copy and deep copy?

### MongoDB
1. When would you choose MongoDB over SQL?
2. What is an embedded document?
3. What is aggregation in MongoDB?
4. What is sharding?
5. Why is schema design important in MongoDB?
6. What is the difference between a document and a row?

### Transactions
1. What does ACID stand for?
2. What is the difference between commit and rollback?
3. What is an isolation level?
4. What is a deadlock?
5. Why should transactions be short?
6. What is the difference between optimistic and pessimistic locking?

### SQL
1. What is the difference between `INNER JOIN` and `LEFT JOIN`?
2. What is normalization?
3. What is the difference between `WHERE` and `HAVING`?
4. How can you find duplicate rows?
5. Why is indexing important for joins?
6. What is the difference between `DELETE` and `TRUNCATE`?

### Indexing
1. What is an index?
2. Why can too many indexes hurt performance?
3. What is a composite index?
4. What is a covering index?
5. How do you know if an index is useful?
6. When should you avoid an index?
