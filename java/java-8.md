# Java 8 Features

## Overview
Java 8 introduced features that changed how Java developers write code. Lambdas, streams, `Optional`, and the new date API make code more expressive and easier to reason about.

## Key Concepts
- Lambda expressions
- Functional interfaces
- Streams API
- `Optional`
- Default methods
- Date and Time API

## Frequently Asked Interview Questions
1. What is a lambda expression?
2. What is the difference between a stream and a collection?
3. Why is `Optional` used?
4. When would you use `flatMap`?
5. What is the difference between `map` and `flatMap`?
6. Why are streams considered lazy?

## Detailed Answers
### 1) Lambda expression
A lambda is a concise way to pass behavior as a parameter. It avoids verbose anonymous classes and improves readability when the logic is small and focused.

### 2) Stream vs collection
A collection is a data structure that stores elements. A stream is a sequence of operations that processes data without necessarily storing all elements. Streams can be lazy, sequential, or parallel.

### 3) `Optional`
`Optional` is used to represent possible absence of a value more clearly than returning null. It helps avoid null-related bugs, but it should not be used as a replacement for all validation logic.

### 4) `flatMap`
`flatMap` is used when each input element maps to multiple outputs or a stream of values. Example: a user may have multiple roles, and you want to flatten them into one stream.

### 5) `map` vs `flatMap`
`map` transforms each element one-to-one. `flatMap` transforms each element into multiple elements or nested structures and flattens them into one stream.

### 6) Laziness of streams
Streams are lazy because intermediate operations are not executed until a terminal operation is called. This allows the pipeline to optimize and avoid unnecessary work.

## Code Examples
```java
List<String> names = List.of("Alice", "Bob", "Charlie");

names.stream()
     .filter(name -> name.startsWith("A"))
     .map(String::toUpperCase)
     .forEach(System.out::println);

Optional<String> maybeName = Optional.ofNullable(null);
String result = maybeName.orElse("Unknown");
```

## Best Practices
- Use streams for readable transformations.
- Avoid side effects inside stream pipelines.
- Use `Optional` carefully; do not overuse it.

## Common Mistakes
- Using streams for trivial loops.
- Modifying shared state in parallel streams.
- Forgetting to handle `Optional.empty()`.

## Real-World Scenarios
A service may use streams to filter orders, map them to DTOs, and compute totals while keeping code readable and declarative.
