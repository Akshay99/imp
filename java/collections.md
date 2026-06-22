# Collections Framework

## Overview
The Java Collections Framework provides reusable data structures for storing and processing groups of objects. Strong understanding of collections is essential for efficient and correct code.

## Key Concepts
- List, Set, Map, Queue, and Deque
- `ArrayList`, `LinkedList`, `Vector`
- `HashSet`, `LinkedHashSet`, `TreeSet`
- `HashMap`, `LinkedHashMap`, `TreeMap`
- Iterators, comparison, and sorting

## Frequently Asked Interview Questions
1. What is the difference between `ArrayList` and `LinkedList`?
2. When should you use `HashMap` over `TreeMap`?
3. What is the difference between `HashSet` and `TreeSet`?
4. How does `ConcurrentHashMap` work?

## Answers
`ArrayList` is better for indexed access, while `LinkedList` performs better for frequent insertions and deletions. `HashMap` gives average O(1) lookup time but does not guarantee order, while `TreeMap` keeps keys sorted. `HashSet` uses hashing, while `TreeSet` uses a sorted structure. `ConcurrentHashMap` supports concurrent access without locking the entire collection.

## Code Examples
```java
Map<String, Integer> scores = new HashMap<>();
scores.put("Alice", 95);

List<String> names = new ArrayList<>();
names.add("Bob");
```

## Best Practices
- Favor interfaces such as `List` and `Map` in API signatures.
- Avoid modifying a collection while iterating.
- Choose the right collection based on access pattern.

## Common Mistakes
- Assuming `HashMap` preserves insertion order.
- Using raw types.
- Exposing mutable internal collections.

## Real-World Scenarios
A dashboard service may use `HashMap` for lookup tables and `ArrayList` for ordered result rendering.
