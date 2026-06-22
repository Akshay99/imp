# Design Patterns

## Overview
Design patterns provide reusable approaches to recurring software design challenges. They help teams communicate decisions clearly and build more maintainable systems.

## Key Concepts
- Creational patterns: Factory, Builder, Singleton
- Structural patterns: Adapter, Decorator, Facade
- Behavioral patterns: Observer, Strategy, Template Method
- SOLID principles

## Frequently Asked Interview Questions
1. What is the difference between a factory and a builder?
2. When should you use a singleton?
3. What is dependency injection?
4. How do you decide between strategy and template method?

## Answers
A factory encapsulates object creation, while a builder helps construct complex objects step by step. A singleton can ensure one instance, but it should be used carefully because it can hide dependencies. Dependency injection helps decouple classes from their concrete dependencies. Strategy selects algorithms dynamically, while template method defines the skeleton of an algorithm.

## Code Examples
```java
interface PaymentStrategy {
    void pay(int amount);
}
```

## Best Practices
- Use patterns only when they solve a real problem.
- Keep designs simple and understandable.
- Prefer composition over excessive inheritance.

## Common Mistakes
- Applying patterns without understanding the trade-offs.
- Introducing complexity too early.
- Hiding dependencies through global state.

## Real-World Scenarios
A payment module may use the strategy pattern to support multiple payment gateways without changing the calling code.
