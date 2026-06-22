# Spring Data JPA

## Overview
Spring Data JPA simplifies database access by reducing boilerplate code and providing repository abstractions.

## Key Concepts
- Entities and repositories
- Derived query methods
- Transactions
- Lazy vs eager loading
- JPQL and native queries

## Frequently Asked Interview Questions
1. What is the difference between JPA and Hibernate?
2. What is the difference between `findById` and `getReference`?
3. What is lazy loading?
4. Why is transaction management important?

## Answers
JPA is the specification, while Hibernate is a common implementation. `findById` loads the entity immediately or returns null, while `getReference` may return a proxy. Lazy loading postpones loading related data until needed. Transactions ensure that multiple database operations are committed or rolled back together.

## Code Examples
```java
public interface UserRepository extends JpaRepository<User, Long> {
    List<User> findByEmail(String email);
}
```

## Best Practices
- Keep transaction boundaries at the service level.
- Be careful about N+1 query problems.
- Use repositories for persistence logic.

## Common Mistakes
- Fetching too much data unnecessarily.
- Forgetting to handle transactions correctly.
- Using entity objects directly in API responses.

## Real-World Scenarios
An e-commerce system may use repositories to manage orders, products, and customers while controlling query performance.
