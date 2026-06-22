# Hazelcast

## Overview
Hazelcast provides distributed in-memory computing and caching capabilities for scalable applications.

## Key Concepts
- Distributed maps
- Near caches
- Cluster membership
- Data partitioning
- Distributed locks

## Frequently Asked Interview Questions
1. What is a distributed map?
2. How does Hazelcast improve scalability?
3. What is a near cache?
4. When is Hazelcast useful?

## Answers
A distributed map stores data across cluster members so multiple nodes can access shared state. Hazelcast improves scalability by allowing data to be shared low-latency across instances. A near cache keeps frequently used data closer to the application. It is useful when shared in-memory state matters for performance.

## Code Examples
```text
Client -> Hazelcast Cluster -> Distributed Map
```

## Best Practices
- Plan partitioning and memory usage carefully.
- Use Hazelcast when low-latency shared state is important.
- Monitor eviction and failover behavior.

## Common Mistakes
- Using Hazelcast as a primary durable store.
- Underestimating cluster coordination complexity.
- Ignoring memory pressure and eviction.

## Real-World Scenarios
A high-throughput application may use Hazelcast to share session or lookup data across nodes.
