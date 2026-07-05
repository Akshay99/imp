# JVM Internals

## Overview
The JVM is important because it determines how Java code executes, how memory is managed, and how performance issues are diagnosed. Interviewers often test your understanding of memory areas, garbage collection, and runtime behavior.

## Key Concepts
- Class loading
- Heap and stack memory
- Garbage collection
- JIT compilation
- Method area and metaspace
- Bytecode execution

## Frequently Asked Interview Questions (moved to spring-questions.md)

## Detailed Answers
### 1) Heap vs stack
Heap memory stores objects created at runtime. Stack memory stores local variables and method call frames. A large object or shared data usually lives on the heap, while method-local values typically live on the stack.

### 2) Garbage collection
Garbage collection removes unreachable objects so memory can be reused. It helps reduce memory leaks but does not completely eliminate object lifecycle issues in application design.

### 3) Garbage collectors
The JVM offers different collectors such as Serial, Parallel, CMS, and G1. The right choice depends on workload, latency requirements, and throughput goals.

### 4) Platform independence
Java source is compiled into bytecode, and the JVM interprets or compiles that bytecode for the target platform. This is why the same bytecode can run on different operating systems.

### 5) JIT compiler
The Just-In-Time compiler optimizes frequently executed bytecode at runtime, improving speed while keeping the startup model flexible.

### 6) Object pooling
Object pooling reuses objects instead of creating new ones, but it is not always the best approach because it increases complexity and may introduce lifecycle bugs. In most modern applications, object creation is cheap enough unless profiling shows otherwise.

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
- Tune memory based on real workloads.
- Avoid unnecessary allocations in hot paths.

## Common Mistakes
- Assuming memory leaks are always the same as in C/C++.
- Ignoring GC tuning until a production issue appears.
- Over-tuning without evidence.

## Real-World Scenarios
A high-throughput trading or analytics system may need careful GC tuning to avoid latency spikes during peak requests.
