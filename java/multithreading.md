# Multithreading

## Overview
Multithreading is essential for building responsive and scalable applications. It allows multiple tasks to run concurrently, but it also introduces risks such as race conditions and deadlocks.

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

## Answers
`Runnable` cannot return a result, whereas `Callable` can. A deadlock happens when threads wait on each other forever. `wait()` releases the monitor, while `sleep()` pauses execution without releasing locks. `ExecutorService` manages thread pools and simplifies task execution.

## Code Examples
```java
ExecutorService executor = Executors.newFixedThreadPool(4);
Future<String> future = executor.submit(() -> "done");
```

## Best Practices
- Prefer thread pools over manually creating threads.
- Keep synchronized blocks as small as possible.
- Use immutable objects where possible.

## Common Mistakes
- Sharing mutable state without proper synchronization.
- Ignoring exceptions in asynchronous tasks.
- Creating excessive thread counts.

## Real-World Scenarios
A backend system may process billing jobs asynchronously using a fixed thread pool so the API remains responsive.
