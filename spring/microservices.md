# Microservices

## Overview
Microservices break a large system into smaller, independently deployable services that communicate through APIs or events.

## Key Concepts
- Service boundaries
- API gateways
- Service discovery
- Resilience and circuit breakers
- Distributed tracing
- Data ownership

## Frequently Asked Interview Questions
1. What are the advantages of microservices?
2. What are the challenges of microservices?
3. What is an API gateway?
4. How do you handle eventual consistency?

## Answers
Microservices allow teams to deploy independently and scale different parts of the system separately. They add complexity in network calls, monitoring, deployment, and data consistency. An API gateway centralizes routing and authentication. Eventual consistency is common, so systems should tolerate temporary data divergence.

## Code Examples
```text
Client -> API Gateway -> Order Service -> Inventory Service
```

## Best Practices
- Define clear service boundaries.
- Prefer asynchronous communication when possible.
- Centralize observability and security.

## Common Mistakes
- Creating microservices too early.
- Ignoring operational complexity.
- Missing monitoring and tracing.

## Real-World Scenarios
A retailer may split order, payment, inventory, and notification processing into services that work together asynchronously.
