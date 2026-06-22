# Multithreading

## Overview
Multithreading is a key interview topic because most modern systems must handle concurrency. You should be able to explain thread safety, synchronization, and how to avoid common pitfalls.

## Key Concepts
- Thread lifecycle
- `Runnable` vs `Callable`
- Synchronization and locks
- `ExecutorService`
- `CompletableFuture`
- Thread safety

## Frequently Asked Interview Questions
1. What is the difference between `Runnable` and `Callable`?
2. What is a deadlock?
3. What is the difference between `wait()` and `sleep()`?
4. How does `ExecutorService` help with concurrency?
5. What are race conditions?
6. Why are immutable objects useful in multithreaded code?

## Detailed Answers
### 1) `Runnable` vs `Callable`
`Runnable` represents a task that does not return a result. `Callable` can return a value or throw a checked exception. In practice, `Callable` is useful when you need a result from an asynchronous operation.

### 2) Deadlock
A deadlock happens when two or more threads are waiting on each other and none can proceed. A common example is thread A holding lock X and waiting for lock Y while thread B holds lock Y and waits for X.

### 3) `wait()` vs `sleep()`
`wait()` releases the monitor and is used for inter-thread communication. `sleep()` pauses execution without releasing the lock. This difference is often asked in interviews because it shows understanding of synchronization behavior.

### 4) `ExecutorService`
`ExecutorService` manages a pool of threads and handles task submission, reuse, and shutdown. It is preferred over manually creating new threads because it reduces resource overhead and improves control.

### 5) Race conditions
A race condition occurs when multiple threads access shared data without proper synchronization, causing unpredictable results. The fix usually involves locking, atomic operations, or immutable design.

### 6) Immutable objects
Immutable objects are safe to share across threads because their state cannot change after construction. This reduces the chance of accidental data corruption.

## Code Examples
```java
ExecutorService executor = Executors.newFixedThreadPool(4);
Future<String> future = executor.submit(() -> "done");

try {
    System.out.println(future.get());
} catch (Exception e) {
    e.printStackTrace();
} finally {
    executor.shutdown();
}
```

## Best Practices
- Prefer thread pools over manual thread creation.
- Keep synchronized sections small.
- Use immutable objects where possible.

## Common Mistakes
- Sharing mutable state without synchronization.
- Ignoring exceptions in async tasks.
- Creating too many threads.

## Real-World Scenarios
A high-traffic backend may use a thread pool to process report generation asynchronously so that the API response remains fast.
