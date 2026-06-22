# Spring MVC

## Overview
Spring MVC is the web layer used to build request-driven applications and expose REST endpoints.

## Key Concepts
- Controllers and request mapping
- Request parameters and path variables
- Models and views
- Validation and exception handling
- `@RequestBody` and `@ResponseBody`

## Frequently Asked Interview Questions
1. What is the role of `@Controller`?
2. How does request mapping work?
3. What is the difference between `@RequestBody` and `@ModelAttribute`?
4. How do you validate user input?

## Answers
`@Controller` marks a class as a web handler. Request mapping binds URLs to specific methods and HTTP verbs. `@RequestBody` reads JSON payloads into objects, while `@ModelAttribute` binds form data or request parameters. Validation is commonly done using annotations such as `@Valid` and custom exception handlers.

## Code Examples
```java
@RestController
public class UserController {
    @GetMapping("/users/{id}")
    public User getUser(@PathVariable Long id) {
        return new User(id, "Alice");
    }
}
```

## Best Practices
- Keep controllers thin.
- Use DTOs at API boundaries.
- Return consistent response structures.

## Common Mistakes
- Returning entities directly from controllers.
- Missing validation boundaries.
- Using inconsistent status codes.

## Real-World Scenarios
A product service may expose endpoints for creating, retrieving, and updating catalogs while keeping business logic in services.
