# Collections Framework

## Overview
The Java Collections Framework is heavily used in interviews because every application handles collections of data. The key is to understand not just syntax, but when to use one structure over another.

## Key Concepts
- List, Set, Map, Queue, and Deque
- `ArrayList`, `LinkedList`, `Vector`
- `HashSet`, `LinkedHashSet`, `TreeSet`
- `HashMap`, `LinkedHashMap`, `TreeMap`
- Iteration, sorting, and comparison strategies

## Frequently Asked Interview Questions
1. What is the difference between `ArrayList` and `LinkedList`?
2. When should you use `HashMap` instead of `TreeMap`?
3. What is the difference between `HashSet` and `TreeSet`?
4. How does `ConcurrentHashMap` work?
5. What is the difference between `Comparable` and `Comparator`?
6. Why should you avoid modifying a collection while iterating?

## Detailed Answers
### 1) `ArrayList` vs `LinkedList`
`ArrayList` is backed by a dynamic array and is efficient for indexed access. `LinkedList` stores nodes and is efficient for frequent insertions and deletions in the middle of the list. In interviews, a good answer is that `ArrayList` wins for random access, while `LinkedList` is better for certain linked operations.

### 2) `HashMap` vs `TreeMap`
`HashMap` gives average O(1) lookup time and does not guarantee order. `TreeMap` keeps keys sorted and provides O(log n) operations. Use `HashMap` for fast lookups and `TreeMap` when sorted ordering matters.

### 3) `HashSet` vs `TreeSet`
`HashSet` uses hashing and does not preserve insertion order. `TreeSet` stores elements in sorted order. If the interview asks about uniqueness and ordering, explain that both enforce uniqueness, but only `TreeSet` guarantees sorting.

### 4) `ConcurrentHashMap`
`ConcurrentHashMap` allows multiple threads to read and update the map safely by splitting the map into segments or buckets. It reduces contention compared to synchronizing the whole map, which is important in highly concurrent systems.

### 5) `Comparable` vs `Comparator`
`Comparable` is implemented by the class itself and defines the natural ordering. `Comparator` is external and can define multiple sorting strategies without changing the class. This is especially useful when you want different sort orders for the same object.

### 6) Modifying collections during iteration
If you modify a collection while iterating, you may get a `ConcurrentModificationException` or unpredictable results. Use iterator removal or collect results into a new list instead.

## Code Examples
```java
Map<String, Integer> scores = new HashMap<>();
scores.put("Alice", 95);
scores.put("Bob", 88);

List<String> names = new ArrayList<>();
names.add("Bob");
names.add("Alice");

Set<String> uniqueNames = new HashSet<>(names);
```

## Best Practices
- Prefer interfaces like `List`, `Set`, and `Map` in method signatures.
- Avoid raw types.
- Use iterators or streams carefully when mutating data.

## Common Mistakes
- Assuming `HashMap` preserves insertion order.
- Using `==` instead of `.equals()` for object comparisons.
- Modifying a collection while looping.

## Real-World Scenarios
In a reporting service, a `Map<String, List<Order>>` can group orders by customer, while a `Set` can remove duplicate products before generating analytics.
