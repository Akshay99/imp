# Node.js

## Overview
Node.js allows JavaScript to run on the server and is widely used to build APIs, tooling, and real-time systems.

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

## Answers
The event loop coordinates asynchronous tasks so the runtime can continue processing other work. Node.js uses non-blocking I/O to avoid waiting on slow operations. Asynchronous code helps scale applications that perform many I/O operations. Errors are commonly handled with try/catch, callbacks, and promises.

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
A Node.js service may process file uploads, API calls, and background jobs concurrently without blocking the main thread.
