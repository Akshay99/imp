# High-Level Design

## Overview
High-level design defines the overall structure of a system, including major services, data flow, and deployment choices.

## Key Concepts
- System boundaries and components
- Scalability and reliability
- Security and observability
- Data flow and communication patterns

## Frequently Asked Interview Questions
1. What is the difference between HLD and LLD?
2. How do you choose between a monolith and microservices?
3. How do you ensure scalability?
4. What are the main trade-offs in architecture decisions?

## Answers
HLD describes the big picture of the system, including components, interactions, and deployment strategy. LLD goes deeper into the implementation details. Monoliths are simpler to operate, while microservices can offer better scaling and team autonomy when the system becomes large.

## Code Examples
```text
Client -> Load Balancer -> App Servers -> Database
```

## Best Practices
- Align the architecture with business goals.
- Plan for failures and observability.
- Document assumptions and trade-offs.

## Common Mistakes
- Designing for unrealistic traffic assumptions.
- Overengineering before validating requirements.
- Ignoring operational concerns.

## Real-World Scenarios
A media platform may use cloud storage, load balancers, caching, and queues to support global traffic.
