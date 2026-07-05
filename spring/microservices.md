# Microservices

## Overview
Microservices are a common interview topic because they represent a major architectural decision. Strong answers should explain both the benefits and the operational complexity involved.

## Key Concepts
- Service boundaries
- API gateway
- Service discovery
- Resilience and circuit breakers
- Distributed tracing
- Data ownership

## Frequently Asked Interview Questions (moved to spring-questions.md)

## Detailed Answers
### 1) Advantages
Microservices allow independent deployment, team ownership, and better scaling of specific components. They make it easier to isolate failures to a smaller part of the system.

### 2) Challenges
They introduce network complexity, distributed debugging, repeated infrastructure concerns, and potential data consistency issues.

### 3) API gateway
An API gateway sits in front of microservices and handles routing, authentication, request aggregation, and rate limiting.

### 4) Eventual consistency
Because services can have separate databases, data may temporarily be inconsistent. The system must tolerate that and reconcile states asynchronously.

### 5) Observability
In distributed systems, logs, metrics, and traces are essential for detecting failures and understanding request flow.

### 6) Sync vs async communication
Synchronous calls are simple but can create coupling and delays. Asynchronous communication improves resilience but requires careful handling of retries and message ordering.

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
A retail platform may split order, payment, inventory, and notification flows into separate services that communicate through APIs and events.
