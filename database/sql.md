# SQL

## Overview
SQL is one of the most important interview topics for backend roles because it shows whether you understand data modeling, retrieval, and performance trade-offs.

## Key Concepts
- `SELECT`, `INSERT`, `UPDATE`, `DELETE`
- Joins and subqueries
- Grouping and aggregation
- Constraints and keys
- Normalization

## Frequently Asked Interview Questions
1. What is the difference between `INNER JOIN` and `LEFT JOIN`?
2. What is normalization?
3. What is the difference between `WHERE` and `HAVING`?
4. How can you find duplicate rows?
5. Why is indexing important for joins?
6. What is the difference between `DELETE` and `TRUNCATE`?

## Detailed Answers
### 1) `INNER JOIN` vs `LEFT JOIN`
`INNER JOIN` returns only matching rows from both tables. `LEFT JOIN` returns all rows from the left table and matching rows from the right table, filling nulls where there is no match.

### 2) Normalization
Normalization reduces redundancy and improves consistency by organizing data into related tables. It is important for avoiding duplicate and conflicting information.

### 3) `WHERE` vs `HAVING`
`WHERE` filters rows before aggregation. `HAVING` filters grouped results after aggregation.

### 4) Finding duplicates
You can use `GROUP BY` with `COUNT(*) > 1` to identify duplicate values.

### 5) Indexing and joins
Indexes can make join operations much faster by reducing the number of rows that must be scanned. Without proper indexes, joins may become slow on large datasets.

### 6) `DELETE` vs `TRUNCATE`
`DELETE` removes rows one by one and can be rolled back in a transaction. `TRUNCATE` removes all rows faster but may have stricter behavior and is often less flexible.

## Code Examples
```sql
SELECT u.name, o.amount
FROM users u
JOIN orders o ON u.id = o.user_id
WHERE o.status = 'PAID';
```

## Best Practices
- Use indexes appropriately.
- Avoid `SELECT *` when you only need a few columns.
- Keep queries readable and deterministic.

## Common Mistakes
- Missing join conditions.
- Using functions on indexed columns without understanding impact.
- Ignoring constraints.

## Real-World Scenarios
A reporting dashboard may use SQL queries to calculate revenue by customer segment, daily order volume, or product performance.
