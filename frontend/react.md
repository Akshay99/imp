# React

## Overview
React is a core frontend topic because it tests whether you understand component design, state management, rendering, and performance. In interviews, your answer should show how React works under the hood and how to build maintainable UIs.

## Key Concepts
- Components and props
- State and lifecycle
- Hooks
- Context API
- Rendering and reconciliation
- Performance optimization

## Frequently Asked Interview Questions (moved to spring-questions.md)

## Detailed Answers
### 1) Props vs state
Props are inputs passed from parent components. State is internal data that can change over time. A good interview answer explains that props are read-only from the child’s perspective, while state is managed by the component.

### 2) Hooks
Hooks let functional components use state and lifecycle behavior without writing classes. They improve readability and reduce boilerplate.

### 3) Reconciliation
Reconciliation is the process React uses to compare the current tree with the next tree and update only what changed.

### 4) Performance optimization
Use memoization, avoid unnecessary re-renders, split code when appropriate, and keep components focused.

### 5) Keys in lists
Keys help React identify which items changed, were added, or removed. Using unstable or non-unique keys can cause incorrect rendering behavior.

### 6) Controlled vs uncontrolled components
Controlled components rely on React state for the form value, while uncontrolled components let the DOM manage the value. Controlled components are usually easier to validate and test.

## Code Examples
```jsx
function Counter() {
  const [count, setCount] = React.useState(0);
  return <button onClick={() => setCount(count + 1)}>Count: {count}</button>;
}
```

## Best Practices
- Keep components small and focused.
- Use keys correctly when rendering lists.
- Prefer composition for complex UI flows.

## Common Mistakes
- Mutating state directly.
- Using unstable keys in lists.
- Overusing global state.

## Real-World Scenarios
A dashboard may use React components to display charts, filters, tables, and status cards while keeping data flow predictable.
