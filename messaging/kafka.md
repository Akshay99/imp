# Kafka

## Overview
Apache Kafka is a distributed event streaming platform used for real-time data movement and event-driven architectures.

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

## Answers
A partition is a unit of parallelism within a topic. Consumer groups allow multiple consumers to share load for a topic. Kafka is optimized for high-throughput streaming, while RabbitMQ is commonly used for task queues and request-response patterns. Idempotence ensures that duplicate messages do not cause duplicate side effects.

## Code Examples
```text
Producer -> Kafka Topic -> Consumer Group
```

## Best Practices
- Use versioned schemas.
- Design for retries and dead-letter flows.
- Monitor throughput, lag, and retention policies.

## Common Mistakes
- Ignoring partition ordering guarantees.
- Using Kafka for synchronous request-response use cases.
- Forgetting to monitor consumer lag.

## Real-World Scenarios
A payment or analytics pipeline may publish events to Kafka for downstream processing and reporting.
