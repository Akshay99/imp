# MongoDB

## Overview
MongoDB is a document-oriented database that provides flexibility for evolving schemas and high-speed development.

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

## Answers
MongoDB is a good fit when schema flexibility and rapid iteration matter. Embedded documents store related data together, which can simplify reads. Aggregation pipelines transform and summarize data. Sharding distributes data across nodes to improve scale.

## Code Examples
```javascript
db.users.find({ status: "active" }).limit(10);
```

## Best Practices
- Model data around access patterns.
- Use indexes for frequent queries.
- Understand consistency trade-offs.

## Common Mistakes
- Using large documents unnecessarily.
- Ignoring proper indexing.
- Assuming MongoDB is always the best choice.

## Real-World Scenarios
A content platform may store flexible profile data and analytics records in MongoDB.
