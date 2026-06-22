# Node.js

## Overview
Node.js is commonly used to build APIs and tooling. Interview answers should cover event-driven architecture, asynchronous execution, and how Node handles I/O efficiently.

## Key Concepts
- Non-blocking I/O
- Event-driven architecture
- Modules and package management
- Streams
- Error handling

## Frequently Asked Interview Questions
1. What is the event loop?
2. Why is Node.js non-blocking?
3. What is the difference between synchronous and asynchronous code?
4. How do you handle errors in Node.js?
5. Why is Node.js good for I/O-heavy applications?
6. What are streams used for?

## Detailed Answers
### 1) Event loop
The event loop coordinates async tasks so the runtime can continue processing other work without blocking.

### 2) Non-blocking behavior
Node.js uses non-blocking I/O so that one request does not block all other operations. This is a large reason for its scalability in network-heavy programs.

### 3) Sync vs async
Synchronous code waits for each operation to finish. Asynchronous code allows the program to continue executing while waiting for external work.

### 4) Error handling
Node applications should handle errors with try/catch, promises, and middleware so failures are managed clearly.

### 5) Why Node is good for I/O-heavy apps
Node is efficient when many operations wait on network or disk because it avoids tying up threads for each waiting task.

### 6) Streams
Streams process data in chunks, which is useful for file uploads, large responses, and efficient data transformation.

## Code Examples
```javascript
const fs = require('fs');
fs.readFile('example.txt', 'utf8', (err, data) => {
  if (err) throw err;
  console.log(data);
});
```

## Best Practices
- Use async patterns consistently.
- Keep business logic separate from HTTP handlers.
- Use environment variables for configuration.

## Common Mistakes
- Blocking the event loop.
- Not handling errors consistently.
- Using callback-heavy code without structure.

## Real-World Scenarios
A Node.js service may process uploads, API calls, and background jobs simultaneously while keeping the runtime responsive.
