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
# Java Collections Interview Notes

## Collection Hierarchy

```text
Iterable
  |
Collection
  |
  +-- List
  |     +-- ArrayList
  |     +-- LinkedList
  |     +-- Vector
  |            |
  |          Stack
  |
  +-- Set
  |     +-- HashSet
  |     +-- LinkedHashSet
  |     +-- TreeSet
  |
  +-- Queue
        +-- PriorityQueue
        +-- LinkedList

Map (Separate Hierarchy)
  |
  +-- HashMap
  +-- LinkedHashMap
  +-- Hashtable
  +-- TreeMap
```

---

# List Implementations

| Feature              | ArrayList     | LinkedList         | Vector        |
| -------------------- | ------------- | ------------------ | ------------- |
| Internal Structure   | Dynamic Array | Doubly Linked List | Dynamic Array |
| Insertion Order      | Yes           | Yes                | Yes           |
| Duplicates Allowed   | Yes           | Yes                | Yes           |
| Null Allowed         | Yes           | Yes                | Yes           |
| Thread Safe          | No            | No                 | Yes           |
| Random Access        | O(1)          | O(n)               | O(1)          |
| Add at End           | O(1)          | O(1)               | O(1)          |
| Insert/Delete Middle | O(n)          | O(n)               | O(n)          |

---

# Common List Syntax

## Add

```java
list.add("Java");
```

## Insert At Index

```java
list.add(1, "Spring");
```

## Update

```java
list.set(1, "Kafka");
```

## Get

```java
list.get(0);
```

## Delete By Index

```java
list.remove(0);
```

## Delete By Value

```java
list.remove("Kafka");
```

## Size

```java
list.size();
```

---

# LinkedList Specific Methods

```java
ll.addFirst("Java");
ll.addLast("Spring");

ll.removeFirst();
ll.removeLast();

ll.getFirst();
ll.getLast();
```

---

# Ways To Iterate

## Traditional For Loop

```java
for(int i=0;i<list.size();i++){
    System.out.println(list.get(i));
}
```

## Enhanced For Loop

```java
for(String s : list){
    System.out.println(s);
}
```

## Iterator

```java
Iterator<String> itr = list.iterator();

while(itr.hasNext()){
    System.out.println(itr.next());
}
```

## ListIterator

```java
ListIterator<String> itr = list.listIterator();

while(itr.hasNext()){
    System.out.println(itr.next());
}

while(itr.hasPrevious()){
    System.out.println(itr.previous());
}
```

## Java 8 forEach

```java
list.forEach(System.out::println);
```

## Stream API

```java
list.stream()
    .forEach(System.out::println);
```

---

# Iterator vs ListIterator

| Feature            | Iterator | ListIterator |
| ------------------ | -------- | ------------ |
| Forward Traversal  | Yes      | Yes          |
| Backward Traversal | No       | Yes          |
| Add                | No       | Yes          |
| Update             | No       | Yes          |
| Remove             | Yes      | Yes          |

---

# Set Implementations

| Feature            | HashSet    | LinkedHashSet            | TreeSet        |
| ------------------ | ---------- | ------------------------ | -------------- |
| Duplicates         | No         | No                       | No             |
| Insertion Order    | No         | Yes                      | No             |
| Sorted             | No         | No                       | Yes            |
| Null Allowed       | One Null   | One Null                 | No             |
| Thread Safe        | No         | No                       | No             |
| Internal Structure | Hash Table | Hash Table + Linked List | Red Black Tree |

---

# Map Implementations

| Feature         | HashMap | LinkedHashMap | TreeMap   | Hashtable |
| --------------- | ------- | ------------- | --------- | --------- |
| Insertion Order | No      | Yes           | No        |           |
| Sorted          | No      | No            | Yes (Key) |           |
| Null Key        | One     | One           | No        | No        |
| Null Value      | Yes     | Yes           | Yes       | No        |
| Thread Safe     | No      | No            | No        | Yes       |
| Performance     | O(1)    | O(1)          | O(log n)  | O(1)      |

---

# Queue Implementations

| Collection    | Ordering       |
| ------------- | -------------- |
| PriorityQueue | Priority Based |
| LinkedList    | FIFO           |

## Queue Syntax

```java
Queue<String> q = new LinkedList<>();

q.offer("A");
q.offer("B");

q.poll();
q.peek();
```

---

# Stack

```java
Stack<String> stack = new Stack<>();

stack.push("A");
stack.push("B");

stack.pop();
stack.peek();
```

LIFO (Last In First Out)

---

# Time Complexity

| Collection | Add      | Search   | Delete   |
| ---------- | -------- | -------- | -------- |
| ArrayList  | O(1)     | O(n)     | O(n)     |
| LinkedList | O(1)     | O(n)     | O(n)     |
| HashSet    | O(1)     | O(1)     | O(1)     |
| TreeSet    | O(log n) | O(log n) | O(log n) |
| HashMap    | O(1)     | O(1)     | O(1)     |
| TreeMap    | O(log n) | O(log n) | O(log n) |

---

# Thread Safe Collections

| Collection | Thread Safe |
| ---------- | ----------- |
| Vector     | Yes         |
| Stack      | Yes         |
| Hashtable  | Yes         |
| ArrayList  | No          |
| LinkedList | No          |
| HashMap    | No          |
| HashSet    | No          |

---

# Modern Thread Safe Alternatives

## Synchronized List

```java
List<String> list =
    Collections.synchronizedList(new ArrayList<>());
```

## CopyOnWriteArrayList

```java
CopyOnWriteArrayList<String> list =
    new CopyOnWriteArrayList<>();
```

## ConcurrentHashMap

```java
ConcurrentHashMap<String,String> map =
    new ConcurrentHashMap<>();
```

---

# Frequently Asked Interview Questions

### ArrayList vs LinkedList

* ArrayList uses Dynamic Array
* LinkedList uses Doubly Linked List
* ArrayList random access O(1)
* LinkedList random access O(n)

### ArrayList vs Vector

* ArrayList is not thread-safe
* Vector is thread-safe
* ArrayList is faster

### HashMap vs Hashtable

* HashMap allows one null key
* Hashtable does not allow null key/value
* Hashtable is thread-safe

### HashMap vs LinkedHashMap

* HashMap does not maintain insertion order
* LinkedHashMap maintains insertion order

### HashMap vs TreeMap

* HashMap O(1)
* TreeMap O(log n)
* TreeMap stores keys in sorted order

### HashSet vs TreeSet

* HashSet unordered
* TreeSet sorted

### Iterator vs ListIterator

* Iterator forward only
* ListIterator forward and backward

### Which Collection Is Most Used?

* ArrayList
* HashMap
* HashSet
* ConcurrentHashMap

# Java Collections Interview Questions

## Basic Questions

1. What is the Collection Framework?
2. Difference between Collection and Collections?
3. Difference between List, Set, Map, and Queue?
4. Why is Map not part of the Collection hierarchy?
5. What is the root interface of the Collection Framework?

---

## ArrayList

6. How does ArrayList work internally?
7. What is the default capacity of ArrayList?
8. How does ArrayList grow when capacity is full?
9. Difference between ArrayList and Array?
10. Difference between ArrayList and Vector?
11. Why is ArrayList not thread-safe?
12. What is RandomAccess interface?
13. Why is ArrayList faster than LinkedList for retrieval?

---

## LinkedList

14. How does LinkedList work internally?
15. Difference between ArrayList and LinkedList?
16. When would you prefer LinkedList over ArrayList?
17. What is a Doubly Linked List?
18. Why is get(index) slower in LinkedList?
19. Difference between addFirst() and add()?

---

## Vector & Stack

20. What is Vector?
21. Why is Vector considered a legacy class?
22. Difference between Vector and ArrayList?
23. Is Vector thread-safe?
24. How does Stack work internally?
25. Why does Stack extend Vector?

---

## HashSet

26. How does HashSet work internally?
27. Can HashSet store duplicate values?
28. How does HashSet identify duplicates?
29. Can HashSet store null values?
30. Difference between HashSet and LinkedHashSet?
31. Difference between HashSet and TreeSet?

---

## HashMap

32. How does HashMap work internally?
33. What are Bucket and Hashing?
34. What is hashCode()?
35. What is equals()?
36. Why should equals() and hashCode() be overridden together?
37. Can HashMap have duplicate keys?
38. Can HashMap have duplicate values?
39. Can HashMap store null keys and values?
40. Difference between HashMap and Hashtable?
41. Difference between HashMap and ConcurrentHashMap?
42. What is a collision in HashMap?
43. How does HashMap handle collisions?
44. What is the load factor?
45. What is rehashing?
46. What is the default capacity of HashMap?
47. What is the default load factor of HashMap?
48. Why are immutable keys recommended in HashMap?

---

## LinkedHashMap

49. Difference between HashMap and LinkedHashMap?
50. How does LinkedHashMap maintain insertion order?
51. How is LinkedHashMap used for LRU Cache?

---

## TreeMap & TreeSet

52. How does TreeMap work internally?
53. Difference between TreeMap and HashMap?
54. Difference between TreeSet and HashSet?
55. What is Red-Black Tree?
56. Can TreeMap store null keys?
57. How does sorting happen in TreeMap?
58. Comparable vs Comparator?

---

## Queue & PriorityQueue

59. Difference between Queue and Stack?
60. What is FIFO?
61. What is PriorityQueue?
62. How does PriorityQueue sort elements?
63. Difference between add() and offer()?
64. Difference between remove() and poll()?
65. Difference between element() and peek()?

---

## Iterator

66. What is Iterator?
67. Difference between Iterator and Enumeration?
68. Difference between Iterator and ListIterator?
69. Can Iterator traverse backward?
70. How do you remove elements using Iterator?

---

## Fail-Fast & Fail-Safe

71. What is ConcurrentModificationException?
72. What is Fail-Fast Iterator?
73. What is Fail-Safe Iterator?
74. Examples of Fail-Fast Collections?
75. Examples of Fail-Safe Collections?

---

## Thread Safety

76. Which Collections are thread-safe?
77. Difference between Hashtable and ConcurrentHashMap?
78. What is CopyOnWriteArrayList?
79. What is Collections.synchronizedList()?
80. Why is ConcurrentHashMap faster than Hashtable?

---

## Comparable & Comparator

81. What is Comparable?
82. What is Comparator?
83. Difference between Comparable and Comparator?
84. When would you use Comparator?

---

## Advanced Questions

85. How does ConcurrentHashMap work internally?
86. What is Segmentation in ConcurrentHashMap?
87. Difference between synchronizedMap() and ConcurrentHashMap?
88. What is CopyOnWriteArrayList and when should it be used?
89. What is BlockingQueue?
90. What is Deque?
91. Difference between Queue and Deque?
92. What is ArrayDeque?
93. Why is ArrayDeque preferred over Stack?

---

## Frequently Asked Coding Questions

94. Remove duplicates from a List.
95. Sort a List of Employees by salary.
96. Find duplicate elements in a List.
97. Count occurrences of elements using Map.
98. Sort a HashMap by value.
99. Convert List to Set.
100. Convert Set to List.
101. Iterate HashMap in different ways.
102. Find top N frequent elements.
103. Find first non-repeated character.
104. Implement LRU Cache using LinkedHashMap.
105. Explain internal working of HashMap with an example.
