# Redis

## Overview
Redis is a popular in-memory store used for caching, rate limiting, distributed locks, and pub/sub. In interviews, strong answers should cover both benefits and limitations.

## Key Concepts
- Strings, hashes, lists, sets, sorted sets
- TTL and eviction policies
- Persistence modes
- Pub/sub and distributed locks

## Frequently Asked Interview Questions (moved to spring-questions.md)

## Detailed Answers
### 1) Cache hit vs miss
A cache hit means the data is found in the cache. A cache miss means the application has to fetch from the source of truth, such as a database.

### 2) Pub/sub
Redis pub/sub allows clients to subscribe to channels and receive messages in real time. It is useful for notifications and real-time updates.

### 3) TTL
TTL defines how long a key should stay valid. It helps prevent stale data and control memory usage.

### 4) Redis for locking
Redis can coordinate distributed locks but must be implemented carefully to prevent stale locks and race conditions.

### 5) Cache invalidation
Invalidation is difficult because updates may happen from multiple services or at different times. A good answer should mention TTL, event-driven invalidation, and cache-aside strategies.

### 6) Persistence vs durability
Persistence means data can survive process restarts; durability means the system is able to recover data safely after failures. Redis offers different persistence strategies depending on requirements.

## Code Examples
```bash
SET user:1 "Alice"
EXPIRE user:1 60
```

## Best Practices
- Cache expensive and frequently read data.
- Set sensible TTLs.
- Keep cache invalidation strategies clear.

## Common Mistakes
- Treating cache as the system of record.
- Ignoring invalidation rules.
- Storing too much data in memory.

## Real-World Scenarios
A dashboard service may cache user profiles and report data to reduce database load during peak hours.
