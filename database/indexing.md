# Indexing

## Overview
Indexes improve query speed by allowing the database to find relevant rows faster. Interviewers often ask about when indexes help and when they can hurt performance.

## Key Concepts
- B-tree indexes
- Composite indexes
- Clustered vs non-clustered indexes
- Selectivity and query planning
- Covering indexes

## Frequently Asked Interview Questions
1. What is an index?
2. Why can too many indexes hurt performance?
3. What is a composite index?
4. What is a covering index?

## Answers
An index is a data structure that helps the database locate rows faster. Too many indexes increase write overhead because every insert or update may require multiple index updates. A composite index uses multiple columns together to support specific query patterns. A covering index contains all required columns so the database can avoid extra table lookups.

## Code Examples
```sql
CREATE INDEX idx_orders_user_created ON orders(user_id, created_at);
```

## Best Practices
- Index columns used frequently in filters and joins.
- Review query plans regularly.
- Balance read performance with write overhead.

## Common Mistakes
- Indexing every column unnecessarily.
- Ignoring the actual query pattern.
- Forgetting to monitor index usage.

## Real-World Scenarios
A search endpoint may benefit from indexes on status, category, and timestamp fields.
