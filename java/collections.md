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

You can copy this directly into a Java_Collections_Interview_Notes.md file.

Java Collections Interview Notes

Collection Hierarchy

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

---

List Implementations

Feature| ArrayList| LinkedList| Vector
Internal Structure| Dynamic Array| Doubly Linked List| Dynamic Array
Insertion Order| Yes| Yes| Yes
Duplicates Allowed| Yes| Yes| Yes
Null Allowed| Yes| Yes| Yes
Thread Safe| No| No| Yes
Random Access| O(1)| O(n)| O(1)
Add at End| O(1)| O(1)| O(1)
Insert/Delete Middle| O(n)| O(n)| O(n)

---

Common List Syntax

Add

list.add("Java");

Insert At Index

list.add(1, "Spring");

Update

list.set(1, "Kafka");

Get

list.get(0);

Delete By Index

list.remove(0);

Delete By Value

list.remove("Kafka");

Size

list.size();

---

LinkedList Specific Methods

ll.addFirst("Java");
ll.addLast("Spring");

ll.removeFirst();
ll.removeLast();

ll.getFirst();
ll.getLast();

---

Ways To Iterate

Traditional For Loop

for(int i=0;i<list.size();i++){
    System.out.println(list.get(i));
}

Enhanced For Loop

for(String s : list){
    System.out.println(s);
}

Iterator

Iterator<String> itr = list.iterator();

while(itr.hasNext()){
    System.out.println(itr.next());
}

ListIterator

ListIterator<String> itr = list.listIterator();

while(itr.hasNext()){
    System.out.println(itr.next());
}

while(itr.hasPrevious()){
    System.out.println(itr.previous());
}

Java 8 forEach

list.forEach(System.out::println);

Stream API

list.stream()
    .forEach(System.out::println);

---

Iterator vs ListIterator

Feature| Iterator| ListIterator
Forward Traversal| Yes| Yes
Backward Traversal| No| Yes
Add| No| Yes
Update| No| Yes
Remove| Yes| Yes

---

Set Implementations

Feature| HashSet| LinkedHashSet| TreeSet
Duplicates| No| No| No
Insertion Order| No| Yes| No
Sorted| No| No| Yes
Null Allowed| One Null| One Null| No
Thread Safe| No| No| No
Internal Structure| Hash Table| Hash Table + Linked List| Red Black Tree

---

Map Implementations

Feature| HashMap| LinkedHashMap| TreeMap| Hashtable
Insertion Order| No| Yes| No| 
Sorted| No| No| Yes (Key)| 
Null Key| One| One| No| No
Null Value| Yes| Yes| Yes| No
Thread Safe| No| No| No| Yes
Performance| O(1)| O(1)| O(log n)| O(1)

---

Queue Implementations

Collection| Ordering
PriorityQueue| Priority Based
LinkedList| FIFO

Queue Syntax

Queue<String> q = new LinkedList<>();

q.offer("A");
q.offer("B");

q.poll();
q.peek();

---

Stack

Stack<String> stack = new Stack<>();

stack.push("A");
stack.push("B");

stack.pop();
stack.peek();

LIFO (Last In First Out)

---

