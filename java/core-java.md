# Core Java

## Overview
Core Java is the foundation of almost every backend and full-stack interview. It is important because many advanced topics—Spring, JPA, concurrency, and design patterns—depend on strong Java basics.

## Key Concepts
- OOP principles: abstraction, encapsulation, inheritance, polymorphism
- Primitive vs reference types
- Packages, interfaces, and access modifiers
- `final`, `static`, `abstract`, `this`, and `super`
- Strings, immutability, and memory model basics
- Exception handling and error propagation

## Frequently Asked Interview Questions (moved to spring-questions.md)

## Detailed Answers
### 1) Abstraction vs encapsulation
Abstraction focuses on hiding implementation details and exposing only what is needed. Encapsulation focuses on keeping data and behavior together and restricting direct access. A real-world example is a car: abstraction lets you use the `drive()` method without knowing the internal engine mechanics, while encapsulation ensures the engine internals are not exposed directly.

### 2) Overloading vs overriding
Method overloading happens in the same class when methods share the same name but differ in parameters. Method overriding happens in a subclass when the child provides a specific implementation of a parent method. Overloading is compile-time polymorphism; overriding is runtime polymorphism.

### 3) `==` vs `.equals()`
`==` compares references for objects and values for primitives. `.equals()` is logic-based and can be overridden by the class to compare meaningful data. For example, two different `String` objects may contain the same text, and `==` may return false while `.equals()` returns true.

### 4) Why strings are immutable
Strings are immutable because it improves memory safety, allows caching, and makes sharing predictable. If strings were mutable, many parts of the application could accidentally change the same value at once.

### 5) Checked vs unchecked exceptions
Checked exceptions must be declared or handled explicitly, usually for recoverable situations such as file I/O. Unchecked exceptions usually represent programming mistakes or runtime problems such as null references or invalid casts.

### 6) Composition vs inheritance
Inheritance creates an “is-a” relationship and can lead to tight coupling. Composition creates a “has-a” relationship and is usually easier to change over time. For example, a `Car` has an `Engine`, but a `Car` is not necessarily an `Engine`.

## Code Examples
```java
class Person {
    private String name;

    public Person(String name) {
        this.name = name;
    }

    public String getName() {
        return name;
    }
}

class Employee extends Person {
    private String role;

    public Employee(String name, String role) {
        super(name);
        this.role = role;
    }
}
```

## Best Practices
- Prefer composition over inheritance when appropriate.
- Keep classes focused on one responsibility.
- Use exceptions to signal real error conditions, not control flow.
- Write code that is easy to read and maintain.

## Common Mistakes
- Confusing inheritance with composition.
- Using `==` for object comparison.
- Catching exceptions too broadly.
- Forgetting to close resources.

## Real-World Scenarios
A service layer may use core Java concepts such as encapsulation, interfaces, and exceptions to keep business logic clean and predictable. In a payment system, a `PaymentService` should not expose raw internal state but instead provide safe methods to perform operations.
