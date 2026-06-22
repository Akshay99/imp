# RabbitMQ

## Overview
RabbitMQ is a message broker used for reliable delivery and queue-based communication. It is often discussed in interviews because it shows understanding of routing, acknowledgements, and failure handling.

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
5. Why is idempotency important for consumers?
6. What happens if a consumer crashes after reading a message but before acknowledging it?

## Detailed Answers
### 1) Direct vs topic exchanges
A direct exchange routes by exact key, while a topic exchange routes using pattern matching. Topic exchanges are more flexible for many-to-many routing.

### 2) Acknowledgements
Acknowledgements confirm that a message was processed successfully. If the consumer fails or times out, the message may be re-queued.

### 3) Dead-letter queue
A dead-letter queue stores messages that could not be processed successfully after retries. It helps teams investigate failure patterns.

### 4) RabbitMQ vs Kafka
RabbitMQ is often preferred for task queues, work distribution, and request-response patterns. Kafka excels at high-volume streaming and replayability.

### 5) Idempotency
Consumers should handle duplicate messages safely because network or broker failures may cause retries.

### 6) Consumer crash behavior
If a crash happens before acknowledgement, the message can be redelivered. This is why reliability logic must be handled carefully.

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
An email service may enqueue notifications so the API remains responsive while background workers handle actual delivery.
