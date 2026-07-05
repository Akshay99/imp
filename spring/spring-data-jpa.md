# Spring Data JPA

## Overview
Spring Data JPA simplifies database access and is a common interview topic because it combines repository abstraction, transaction handling, and object mapping.

## Key Concepts
- Entities and repositories
- Derived query methods
- Transactions
- Lazy vs eager loading
- JPQL and native queries

## Frequently Asked Interview Questions (moved to spring-questions.md)

## Detailed Answers
### 1) JPA vs Hibernate
JPA is the specification; Hibernate is a popular implementation. JPA defines the contract, while Hibernate provides the actual behavior.

### 2) `findById` vs `getReference`
`findById` immediately loads the entity or returns null. `getReference` may return a proxy and delay the database hit until the entity is actually used.

### 3) Lazy loading
Lazy loading delays loading related data until needed. It can improve performance but may cause extra queries if not managed carefully.

### 4) Transaction management
Transactions ensure that multiple operations either succeed together or fail together. This is essential for consistency in financial or inventory flows.

### 5) N+1 problem
The N+1 problem happens when loading a parent collection causes one extra query for each child. This is common when lazy loading is used incorrectly.

### 6) Avoiding too much data
Use projections, pagination, and selective fetching to control exactly what data is read. This reduces memory use and improves throughput.

## Code Examples
```java
public interface UserRepository extends JpaRepository<User, Long> {
    List<User> findByEmail(String email);
}
```

## Best Practices
- Keep transaction boundaries at the service layer.
- Use projections or DTOs when needed.
- Watch out for N+1 queries.

## Common Mistakes
- Fetching too much data unnecessarily.
- Forgetting transaction boundaries.
- Using entity objects directly in API responses.

## Real-World Scenarios
An e-commerce service may use repositories to manage products, orders, and customers while controlling the amount of data fetched during checkout.
