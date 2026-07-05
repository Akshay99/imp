# High-Level Design

## Overview
High-level design focuses on the overall architecture of a system. Interviewers often want to see how you think about components, data flow, scalability, reliability, and trade-offs.

## Key Concepts
- System boundaries and components
- Scalability and reliability
- Security and observability
- Data flow and communication patterns

## Frequently Asked Interview Questions (moved to spring-questions.md)

## Detailed Answers
### 1) HLD vs LLD
HLD looks at the big picture and main components. LLD focuses on the internals of a specific module or feature.

### 2) Monolith vs microservices
A monolith is simpler to build and operate early on. Microservices help with team independence and scaling when the system becomes complex.

### 3) Ensuring scalability
Use load balancers, caching, database optimization, queueing, and stateless services where possible.

### 4) Architecture trade-offs
Every design decision has trade-offs in complexity, cost, latency, consistency, and operational overhead.

### 5) Observability
Logs, metrics, dashboards, and tracing make it easier to diagnose production issues quickly.

### 6) Failure handling
Assume parts of the system will fail, and design for retries, timeouts, circuit breakers, and graceful degradation.

## Code Examples
```text
Client -> Load Balancer -> App Servers -> Database
```

## Best Practices
- Align architecture with business goals.
- Plan for failures and observability.
- Document assumptions and trade-offs.

## Common Mistakes
- Designing for unrealistic traffic assumptions.
- Overengineering before validating requirements.
- Ignoring operational concerns.

## Real-World Scenarios
A media platform may use CDN, load balancers, object storage, caching, and message queues to support global traffic.
