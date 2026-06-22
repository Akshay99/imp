# Transactions

## Overview
Transactions ensure that related database operations succeed or fail together. A good understanding of transaction semantics is critical for interview discussions about data integrity.

## Key Concepts
- ACID properties
- Commit and rollback
- Isolation levels
- Savepoints
- Deadlocks

## Frequently Asked Interview Questions
1. What does ACID stand for?
2. What is the difference between commit and rollback?
3. What is an isolation level?
4. What is a deadlock?

## Answers
ACID stands for Atomicity, Consistency, Isolation, and Durability. Commit saves changes permanently, while rollback undoes them. Isolation levels control how transactions interact with concurrent changes. A deadlock occurs when multiple transactions wait on each other indefinitely.

## Code Examples
```sql
BEGIN;
UPDATE accounts SET balance = balance - 100 WHERE id = 1;
UPDATE accounts SET balance = balance + 100 WHERE id = 2;
COMMIT;
```

## Best Practices
- Keep transaction scope short.
- Handle exceptions carefully.
- Use a suitable isolation level for the workload.

## Common Mistakes
- Holding locks for long-running business logic.
- Forgetting to rollback on failure.
- Mixing unrelated operations in one transaction.

## Real-World Scenarios
A payment system must ensure that debit and credit steps are performed atomically.
