# Redis

## Overview
Redis is an in-memory data store often used for caching, session management, rate limiting, and pub/sub.

## Key Concepts
- Strings, hashes, lists, sets, sorted sets
- TTL and eviction policies
- Persistence modes
- Pub/sub and distributed locks

## Frequently Asked Interview Questions
1. What is a cache hit vs cache miss?
2. How does Redis support pub/sub?
3. What is TTL?
4. When should Redis be used for locking?

## Answers
A cache hit occurs when the data is already available in cache; a miss requires fetching it from the source. Redis pub/sub allows real-time messaging to subscribers. TTL determines how long a key remains valid. Redis locks can coordinate distributed tasks, but they require careful handling to avoid stale lock issues.

## Code Examples
```bash
SET user:1 "Alice"
EXPIRE user:1 60
```

## Best Practices
- Use cache for expensive and frequently read data.
- Set sensible TTL values.
- Keep cache invalidation strategies clear.

## Common Mistakes
- Treating cache as the system of record.
- Ignoring invalidation rules.
- Storing too much data in memory.

## Real-World Scenarios
A dashboard service may cache user profiles and report data to reduce database load.
