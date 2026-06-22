# Low-Level Design

## Overview
Low-level design focuses on classes, interfaces, and detailed implementation decisions for a specific module or feature.

## Key Concepts
- Classes, responsibilities, and interactions
- Data structures and algorithms
- API contracts and error handling
- Design patterns and extensibility

## Frequently Asked Interview Questions
1. What is the difference between HLD and LLD?
2. How do you design a cache for a system?
3. How do you structure service classes?
4. How do you handle extensibility?

## Answers
HLD looks at the architecture and major components, while LLD dives into concrete implementation details. A good low-level design specifies responsibilities, interfaces, data flow, and edge cases. It also considers testability, maintainability, and operational concerns.

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
A notification system may be designed with sender, template, retry policy, and audit components.
