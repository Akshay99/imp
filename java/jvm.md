# JVM Internals

## Overview
The Java Virtual Machine executes bytecode and manages memory, thread execution, and runtime optimization. Knowledge of JVM internals is important for performance tuning and troubleshooting.

## Key Concepts
- Class loading
- Heap and stack memory
- Garbage collection
- JIT compilation
- Method area and metaspace
- Bytecode execution

## Frequently Asked Interview Questions
1. What is the difference between heap and stack memory?
2. What is garbage collection?
3. What are the common garbage collectors?
4. Why is the JVM platform-independent?

## Answers
Heap memory stores objects, while stack memory stores method frames and local variables. Garbage collection reclaims unreachable objects so the application can reuse memory. Common collectors include Serial, Parallel, CMS, and G1. The JVM makes Java portable because it runs bytecode on a platform-specific runtime.

## Code Examples
```java
public class Demo {
    public static void main(String[] args) {
        String text = "Hello";
        System.out.println(text);
    }
}
```

## Best Practices
- Monitor heap usage and GC behavior.
- Tune memory based on actual workloads.
- Avoid unnecessary object creation in performance-sensitive code.

## Common Mistakes
- Assuming all memory leaks are equally easy to detect.
- Ignoring performance profiling until production issues appear.
- Over-tuning without collecting evidence.

## Real-World Scenarios
A large enterprise application may need careful GC tuning to avoid latency spikes during peak traffic.
