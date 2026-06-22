# Transactions

## Overview
Transactions are central to reliability in data systems. Interviewers want to know whether you understand atomicity, consistency, isolation, and the practical implications of concurrency.

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
5. Why should transactions be short?
6. What is the difference between optimistic and pessimistic locking?

## Detailed Answers
### 1) ACID
ACID stands for Atomicity, Consistency, Isolation, and Durability. It describes the guarantees a database should provide for reliable transaction processing.

### 2) Commit vs rollback
Commit permanently saves changes, while rollback undoes them. The choice depends on whether the application considers the operation successful.

### 3) Isolation levels
Isolation levels define how concurrent transactions interact. Higher isolation reduces anomalies but may increase locking and reduce throughput.

### 4) Deadlock
A deadlock happens when transactions wait on each other forever. It is often resolved by the database, but applications should design around it.

### 5) Short transactions
Short transactions reduce lock time, lower contention, and improve throughput. Long transactions can cause delays and dependence problems.

### 6) Optimistic vs pessimistic locking
Optimistic locking checks for conflicts at update time; pessimistic locking takes locks early to prevent conflicts. The first is often better for low contention, while the second is useful for high-conflict scenarios.

## Code Examples
```sql
BEGIN;
UPDATE accounts SET balance = balance - 100 WHERE id = 1;
UPDATE accounts SET balance = balance + 100 WHERE id = 2;
COMMIT;
```

## Best Practices
- Keep transactions short.
- Handle exceptions carefully.
- Use a suitable isolation level.

## Common Mistakes
- Holding locks for long operations.
- Forgetting rollback on failure.
- Mixing unrelated operations into one transaction.

## Real-World Scenarios
A payment workflow must ensure that debit and credit operations are committed atomically so money is not lost or duplicated.
