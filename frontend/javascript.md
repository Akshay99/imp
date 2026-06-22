# JavaScript

## Overview
JavaScript is the language of the web and is also used in modern backend ecosystems. Strong JavaScript knowledge is essential for frontend and full-stack interviews.

## Key Concepts
- Scope and closures
- Promises and async/await
- Event loop
- Prototypes and inheritance
- Hoisting and modules

## Frequently Asked Interview Questions
1. What is a closure?
2. What is the difference between `var`, `let`, and `const`?
3. How does the event loop work?
4. What is the difference between promises and callbacks?

## Answers
A closure captures variables from its lexical scope. `var` is function-scoped, while `let` and `const` are block-scoped. The event loop coordinates the call stack and task queue to handle asynchronous work. Promises provide a cleaner approach to async code than callbacks.

## Code Examples
```javascript
const fetchData = async () => {
  const response = await fetch('/api');
  return response.json();
};
```

## Best Practices
- Prefer `const` for immutable bindings.
- Handle rejections explicitly.
- Avoid global mutable state.

## Common Mistakes
- Confusing truthy and falsy values.
- Using `==` instead of `===`.
- Forgetting to handle async errors.

## Real-World Scenarios
A frontend application may fetch user data asynchronously and update loading and error states accordingly.
