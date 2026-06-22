# SQL

## Overview
SQL is the standard language for querying and managing relational data. Strong SQL skills are essential for interviews involving database design and query performance.

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

## Answers
An `INNER JOIN` returns only matching rows, while a `LEFT JOIN` returns all rows from the left table and matching rows from the right table. Normalization reduces redundancy and improves data consistency. `WHERE` filters rows before grouping, and `HAVING` filters grouped data after aggregation.

## Code Examples
```sql
SELECT u.name, o.amount
FROM users u
JOIN orders o ON u.id = o.user_id
WHERE o.status = 'PAID';
```

## Best Practices
- Use indexes appropriately.
- Avoid `SELECT *` when only a few columns are needed.
- Keep queries readable and deterministic.

## Common Mistakes
- Missing join conditions.
- Using functions on indexed columns without understanding impact.
- Ignoring data constraints.

## Real-World Scenarios
A reporting dashboard may use SQL aggregations to calculate revenue, order volume, and customer trends.
