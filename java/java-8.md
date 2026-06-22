# Java 8 Features

## Overview
Java 8 introduced functional programming features that changed how developers write readable, expressive, and maintainable code.

## Key Concepts
- Lambda expressions
- Functional interfaces
- Streams API
- `Optional`
- Default methods
- New Date and Time API

## Frequently Asked Interview Questions
1. What is a lambda expression?
2. What is the difference between a stream and a collection?
3. Why is `Optional` used?
4. When would you use `flatMap`?

## Answers
A lambda is an anonymous function used to pass behavior as a parameter. A stream is a pipeline for processing data, not a data store. `Optional` helps represent the absence of a value explicitly. `flatMap` is useful when each item maps to multiple values or nested collections.

## Code Examples
```java
List<String> names = List.of("A", "B", "C");
names.stream()
     .filter(n -> n.length() > 1)
     .map(String::toUpperCase)
     .forEach(System.out::println);
```

## Best Practices
- Use streams for readable transformations.
- Avoid side effects inside stream pipelines.
- Use `Optional` to reduce null handling complexity.

## Common Mistakes
- Using streams for very simple loops.
- Modifying shared state inside parallel streams.
- Forgetting to handle `Optional.empty()`.

## Real-World Scenarios
A service may stream API results, filter invalid records, and convert them into DTOs for response generation.
