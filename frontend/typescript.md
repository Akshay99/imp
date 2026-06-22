# TypeScript

## Overview
TypeScript adds static typing to JavaScript, improving maintainability and reducing errors in large applications.

## Key Concepts
- Types and interfaces
- Union and intersection types
- Generics
- Type inference
- Utility types

## Frequently Asked Interview Questions
1. What is the difference between `interface` and `type`?
2. What are generics?
3. What is the benefit of type inference?
4. How does `unknown` differ from `any`?

## Answers
An `interface` is typically used for object shapes, while a `type` can describe unions and other complex declarations. Generics make components reusable across different types. Type inference reduces the need to annotate everything manually, and `unknown` is safer than `any` because it forces narrowing.

## Code Examples
```typescript
interface User {
  id: number;
  name: string;
}

function greet(user: User): string {
  return `Hello, ${user.name}`;
}
```

## Best Practices
- Prefer specific types over broad ones.
- Use interfaces for contracts.
- Avoid `any` unless absolutely necessary.

## Common Mistakes
- Overcomplicating types.
- Forgetting to narrow union types.
- Using `as any` to bypass checks.

## Real-World Scenarios
A large frontend codebase can use TypeScript to validate API responses and shared models consistently.
