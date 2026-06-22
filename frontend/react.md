# React

## Overview
React is a JavaScript library for building user interfaces with reusable components and a declarative programming model.

## Key Concepts
- Components and props
- State and lifecycle
- Hooks
- Context API
- Rendering and reconciliation
- Performance optimization

## Frequently Asked Interview Questions
1. What is the difference between props and state?
2. What are React hooks?
3. What is reconciliation?
4. How do you optimize React performance?

## Answers
Props are inputs passed from a parent component, while state stores internal data. Hooks let functional components use state and lifecycle features. Reconciliation is the process React uses to update the DOM efficiently. Performance optimization often involves memoization, code splitting, and avoiding unnecessary renders.

## Code Examples
```jsx
function Counter() {
  const [count, setCount] = React.useState(0);
  return <button onClick={() => setCount(count + 1)}>Count: {count}</button>;
}
```

## Best Practices
- Keep components focused and reusable.
- Use keys correctly when rendering lists.
- Prefer composition for complex UI flows.

## Common Mistakes
- Mutating state directly.
- Using unstable keys in lists.
- Overusing global state.

## Real-World Scenarios
A dashboard may use React components to display charts, filters, and tables while keeping data flow predictable.
