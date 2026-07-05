# Indexing

## Overview
Indexing is crucial for performance because it helps the database locate rows faster. In interviews, the best answers show both the benefits and the trade-offs.

## Key Concepts
- B-tree indexes
- Composite indexes
- Clustered vs non-clustered indexes
- Selectivity and query planning
- Covering indexes

## Frequently Asked Interview Questions (moved to spring-questions.md)

## Detailed Answers
### 1) What is an index?
An index is a data structure that speeds up lookup operations by reducing the amount of data the database must scan.

### 2) Too many indexes
Each index must be updated during inserts, updates, and deletes. Too many indexes can slow down writes and increase storage usage.

### 3) Composite index
A composite index uses multiple columns together, which is helpful when queries filter by several columns in a specific order.

### 4) Covering index
A covering index includes all columns a query needs so the database can answer the query without reading the actual table rows.

### 5) Knowing if an index is useful
You can check query plans, execution times, and row scans. A useful index usually lowers the number of rows scanned significantly.

### 6) Avoiding indexes
If a column is rarely used in filters or if the table is very small, an index may not provide enough benefit to justify the cost.

## Code Examples
```sql
CREATE INDEX idx_orders_user_created ON orders(user_id, created_at);
```

## Best Practices
- Index columns used heavily in filters and joins.
- Review query plans regularly.
- Balance read performance with write overhead.

## Common Mistakes
- Indexing every column.
- Ignoring query plans.
- Using low-selectivity indexes unnecessarily.

## Real-World Scenarios
A search endpoint may use composite indexes on status, category, and timestamp to make filtering faster for large datasets.
