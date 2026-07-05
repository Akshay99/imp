# Hazelcast

## Overview
Hazelcast is a distributed in-memory platform used for caching, clustering, and low-latency shared state. It is especially relevant when multiple application nodes need near-real-time access to the same data.

## Key Concepts
- Distributed maps
- Near caches
- Cluster membership
- Data partitioning
- Distributed locks

## Frequently Asked Interview Questions (moved to spring-questions.md)

## Detailed Answers
### 1) Distributed map
A distributed map stores data across nodes so that the cluster behaves like one shared memory layer.

### 2) Scalability
Hazelcast reduces bottlenecks by distributing data and computation across nodes, making it easier to scale horizontally.

### 3) Near cache
A near cache keeps frequently accessed data closer to the application node, reducing latency.

### 4) When Hazelcast is useful
It is useful when applications need low-latency shared state, distributed locks, or coordinated caching across multiple instances.

### 5) Partitioning
Partitioning distributes data across cluster members so that the system can scale and balance load.

### 6) Handling failures
Hazelcast supports cluster membership and failover behavior, which is important for resilience in production.

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
A high-traffic application may use Hazelcast to share session or lookup data across nodes while keeping latency low.
