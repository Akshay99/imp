# Kafka

## Overview
Kafka is a distributed event streaming platform used for real-time data movement. Interview answers should focus on throughput, partitions, consumers, and trade-offs with other messaging systems.

## Key Concepts
- Topics, partitions, and brokers
- Producers and consumers
- Consumer groups and offsets
- Idempotence and retries
- Kafka Streams

## Frequently Asked Interview Questions
1. What is a partition in Kafka?
2. How do consumer groups work?
3. What is the difference between Kafka and RabbitMQ?
4. What is idempotence?
5. Why is ordering guaranteed only within a partition?
6. What is the role of offsets?

## Detailed Answers
### 1) Partition
A partition is a unit of parallelism inside a topic. Messages are distributed across partitions, allowing Kafka to scale horizontally.

### 2) Consumer groups
Consumer groups let multiple consumers share a topic so that each message is processed once per group. This is how Kafka handles parallelism.

### 3) Kafka vs RabbitMQ
Kafka is designed for streaming and high throughput, while RabbitMQ is often used for traditional queueing and task distribution.

### 4) Idempotence
Idempotence ensures the same message can be retried without causing duplicate side effects. This is important for reliability in real systems.

### 5) Ordering guarantees
Kafka guarantees order only within a partition, not across the entire topic. This is because messages may be routed to different partitions.

### 6) Offsets
Offsets track how far a consumer has progressed in a partition. They are critical for resume behavior after a restart or failure.

## Code Examples
```text
Producer -> Kafka Topic -> Consumer Group
```

## Best Practices
- Use versioned schemas.
- Design for retries and dead-letter flows.
- Monitor lag and throughput.

## Common Mistakes
- Ignoring partition ordering guarantees.
- Using Kafka for synchronous request-response flows.
- Forgetting to monitor lag.

## Real-World Scenarios
A payment or analytics pipeline may publish events to Kafka for downstream processing, notifications, and reporting.
