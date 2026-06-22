# TypeScript

## Overview
TypeScript is important because it improves code safety, developer productivity, and maintainability. In interviews, you should be able to explain types, inference, and how TypeScript helps catch bugs earlier.

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
5. What is a union type?
6. Why is TypeScript useful in large applications?

## Detailed Answers
### 1) `interface` vs `type`
An interface is best for object shapes and declarations that may be extended. A type alias can represent unions, tuples, and other complex forms.

### 2) Generics
Generics let you write reusable code that works with many types while preserving type safety.

### 3) Type inference
Type inference allows TypeScript to deduce types when possible, reducing repeated annotations while keeping safety.

### 4) `unknown` vs `any`
`unknown` forces you to narrow the value before using it. `any` disables type checking and should be avoided when possible.

### 5) Union types
A union type allows a variable to be one of several possible types, which is helpful for API responses and dynamic data.

### 6) Why TypeScript matters
TypeScript helps catch mistakes before runtime and makes large codebases easier to understand and refactor.

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
- Use interfaces for object contracts.
- Avoid `any` unless absolutely necessary.

## Common Mistakes
- Overcomplicating types.
- Forgetting to narrow union types.
- Using `as any` to bypass checks.

## Real-World Scenarios
A frontend app may use TypeScript to validate API responses, props, and shared domain models consistently.
