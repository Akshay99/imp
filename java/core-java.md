# Core Java

## Overview
Core Java focuses on the fundamentals of the language, object-oriented programming, memory handling, and common interview topics that every Java developer should understand deeply.

## Key Concepts
- Object-oriented principles: abstraction, encapsulation, inheritance, polymorphism
- Primitive vs reference types
- Packages, interfaces, and access modifiers
- `final`, `static`, `abstract`, and `this`/`super`
- Strings, immutability, and the Java memory model
- Exceptions and error handling

## Frequently Asked Interview Questions
1. What is the difference between abstraction and encapsulation?
2. What is method overloading vs overriding?
3. What is the difference between `==` and `.equals()`?
4. Why are strings immutable?
5. What is the difference between checked and unchecked exceptions?

## Answers
Abstraction hides implementation details, while encapsulation bundles data and behavior. Overloading creates multiple methods with the same name but different signatures, while overriding changes behavior in a subclass. `==` compares references for objects and values for primitives, whereas `.equals()` compares logical equality. Strings are immutable to improve safety and support sharing. Checked exceptions must be declared or handled explicitly, while unchecked exceptions usually represent runtime problems.

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
```

## Best Practices
- Prefer meaningful names and small methods.
- Use interfaces to define contracts.
- Handle exceptions at the right abstraction level.

## Common Mistakes
- Confusing inheritance with composition.
- Using `==` for object comparisons.
- Catching exceptions too broadly.

## Real-World Scenarios
A service layer often uses core Java concepts to model business entities, enforce validation, and handle edge cases cleanly.
