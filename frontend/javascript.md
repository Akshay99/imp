# JavaScript

## Overview
JavaScript is central to frontend and full-stack development. Interviewers often test closures, async behavior, prototypes, and event handling because these concepts appear constantly in real programs.

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
5. What is hoisting?
6. What is the difference between shallow copy and deep copy?

## Detailed Answers
### 1) Closure
A closure captures variables from its lexical scope even after the outer function has finished executing. This is why callbacks can still access values from their enclosing environment.

### 2) `var`, `let`, `const`
`var` is function-scoped and can be re-declared. `let` and `const` are block-scoped, and `const` prevents reassignment but does not make objects immutable.

### 3) Event loop
The event loop coordinates the call stack and task queue so asynchronous operations can run without blocking the main thread.

### 4) Promises vs callbacks
Promises provide cleaner async flow and built-in error handling, while callbacks can lead to nested logic and harder-to-read code.

### 5) Hoisting
Hoisting means declarations are moved to the top of the scope during execution. This affects how variables and functions behave before they are initialized.

### 6) Shallow vs deep copy
A shallow copy duplicates the top-level structure but not nested values. A deep copy duplicates nested data as well, preventing shared references.

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
A frontend app may fetch user data asynchronously, show a loading state, and update the UI once the response arrives.
