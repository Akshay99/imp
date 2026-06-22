# Design Patterns

## Overview
Design patterns are reusable ideas for solving common design challenges. In interviews, the best answers explain the problem, the pattern, the trade-offs, and where the pattern fits.

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
5. Why is the open-closed principle important?
6. What is the difference between adapter and facade?

## Detailed Answers
### 1) Factory vs builder
A factory hides object creation logic and usually returns a concrete object based on inputs. A builder is used when object construction requires many optional parameters or step-by-step setup.

### 2) Singleton
A singleton ensures one instance exists. It can be useful for configuration or shared resources, but it can also introduce global state and testing difficulty. Interviewers often look for caution when using it.

### 3) Dependency injection
Dependency injection passes dependencies into a class rather than letting it create them internally. This improves flexibility, testability, and separation of concerns.

### 4) Strategy vs template method
Strategy changes the algorithm at runtime by selecting a different implementation. Template method defines the structure of an algorithm but allows some steps to vary through inheritance.

### 5) Open-closed principle
The open-closed principle says software should be open for extension but closed for modification. This is important because it helps teams add behavior without breaking existing code.

### 6) Adapter vs facade
An adapter makes two incompatible interfaces work together. A facade provides a simpler, unified interface over a more complex system.

## Code Examples
```java
interface PaymentStrategy {
    void pay(int amount);
}

class CreditCardPayment implements PaymentStrategy {
    public void pay(int amount) {
        System.out.println("Paying " + amount + " via credit card");
    }
}
```

## Best Practices
- Use patterns only when they solve a real problem.
- Keep designs simple and understandable.
- Prefer composition and dependency injection over hidden global state.

## Common Mistakes
- Using patterns unnecessarily.
- Ignoring trade-offs.
- Overengineering small problems.

## Real-World Scenarios
A payment service may use the strategy pattern when different payment gateways need to be supported without rewriting business logic.
