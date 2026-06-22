# MongoDB

## Overview
MongoDB is a document-oriented database that is widely used when schema flexibility and rapid iteration matter. Interview answers should cover both strengths and limitations.

## Key Concepts
- Documents and collections
- Embedded vs referenced data
- Indexes and aggregation
- Sharding and replication
- Query patterns

## Frequently Asked Interview Questions
1. When would you choose MongoDB over SQL?
2. What is an embedded document?
3. What is aggregation in MongoDB?
4. What is sharding?
5. Why is schema design important in MongoDB?
6. What is the difference between a document and a row?

## Detailed Answers
### 1) MongoDB vs SQL
MongoDB is often preferred when the schema changes frequently or the data is naturally document-shaped. SQL is still better when strong consistency and complex joins are important.

### 2) Embedded document
An embedded document stores related data inside the same document. This can reduce joins but may increase document size and complexity.

### 3) Aggregation
Aggregation pipelines allow you to group, filter, transform, sort, and summarize data in a flexible way.

### 4) Sharding
Sharding distributes data across multiple machines so a single node does not become the bottleneck.

### 5) Schema design
Good schema design in MongoDB depends on how the data is read and written. A poor design can lead to repeated updates or large documents.

### 6) Document vs row
A document is a JSON-like structure that can contain nested data. A row is a flat tuple in a relational table.

## Code Examples
```javascript
db.users.find({ status: "active" }).limit(10);
```

## Best Practices
- Model data around access patterns.
- Use indexes for frequent queries.
- Understand consistency trade-offs.

## Common Mistakes
- Using oversized documents.
- Ignoring indexing.
- Assuming MongoDB is always the best choice.

## Real-World Scenarios
A content platform may store flexible profiles and activity logs in MongoDB while keeping analytics data in a separate system.
