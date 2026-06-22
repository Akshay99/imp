# Low-Level Design

## Overview
Low-level design focuses on the detailed implementation decisions behind a specific feature or module. It is a common interview topic for senior engineering roles because it tests how well you can translate requirements into a practical design.

## Key Concepts
- Class responsibilities
- Object interactions
- Data structures and algorithms
- API contracts and error handling
- Design patterns and extensibility

## Frequently Asked Interview Questions
1. What is the difference between HLD and LLD?
2. How do you design a cache for a system?
3. How do you structure service classes?
4. How do you handle extensibility?
5. Why are interfaces useful in LLD?
6. How do you approach edge cases in design?

## Detailed Answers
### 1) HLD vs LLD
HLD describes the system architecture and components. LLD explains classes, interfaces, methods, data structures, and technical decisions for a specific feature.

### 2) Designing a cache
A good cache design considers eviction policy, invalidation strategy, size limits, and consistency with the source of truth.

### 3) Structuring service classes
Service classes should coordinate workflows, hide implementation details, and delegate persistence or external calls appropriately.

### 4) Extensibility
Use interfaces, abstraction boundaries, and configuration to support future changes without rewriting everything.

### 5) Interfaces in LLD
Interfaces help define contracts between components, improving testability and reducing coupling.

### 6) Edge cases
A strong LLD always considers validation failures, retries, partial failures, concurrency, and data consistency edge cases.

## Code Examples
```text
OrderService -> PaymentGateway -> InventoryService
```

## Best Practices
- Keep modules cohesive.
- Document assumptions and trade-offs.
- Consider failure scenarios in the design.

## Common Mistakes
- Designing without understanding the requirements.
- Overengineering simple use cases.
- Missing edge cases.

## Real-World Scenarios
A notification system may be designed with sender, template, retry policy, and audit components so failures are visible and recoverable.
