# RabbitMQ

## Overview
RabbitMQ is a message broker that supports reliable delivery, routing, and queueing for distributed systems.

## Key Concepts
- Exchanges, queues, and bindings
- Publish/subscribe patterns
- Routing keys
- Acknowledgements and dead-letter queues

## Frequently Asked Interview Questions
1. What is the difference between direct and topic exchanges?
2. How do acknowledgements work?
3. What is a dead-letter queue?
4. When would you choose RabbitMQ over Kafka?

## Answers
Direct exchanges route to a queue based on an exact key, while topic exchanges match patterns. Acknowledgements confirm that a consumer processed a message successfully. A dead-letter queue stores failed messages for inspection. RabbitMQ is often used for task queues, while Kafka is stronger for event streaming.

## Code Examples
```text
Publisher -> Exchange -> Queue -> Consumer
```

## Best Practices
- Prefer idempotent consumers.
- Plan retries and DLQ handling.
- Monitor queue depth and consumer health.

## Common Mistakes
- Failing to ack or nack messages properly.
- Overloading a single queue.
- Ignoring failure handling.

## Real-World Scenarios
An email or reporting system may enqueue background work so the user-facing API remains fast.
