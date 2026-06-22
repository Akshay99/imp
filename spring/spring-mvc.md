# Spring MVC

## Overview
Spring MVC is the request-handling layer for web applications in the Spring ecosystem. Interviews often focus on controller structure, request mapping, validations, and how to build clean REST APIs.

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
5. Why should controllers stay thin?
6. What is the difference between `@RestController` and `@Controller`?

## Detailed Answers
### 1) `@Controller`
`@Controller` marks a class as a web handler. It is used to process incoming requests and return appropriate responses.

### 2) Request mapping
`@GetMapping`, `@PostMapping`, and similar annotations map HTTP methods to controller methods. They let the framework route requests based on URL patterns and request parameters.

### 3) `@RequestBody` vs `@ModelAttribute`
`@RequestBody` reads JSON payloads and binds them to objects. `@ModelAttribute` is often used for form data or query parameters. In REST APIs, `@RequestBody` is more common.

### 4) Validation
Validation can be done with annotations like `@Valid`, `@NotNull`, and `@Size`. The framework then checks the object and returns helpful validation errors.

### 5) Thin controllers
Controllers should coordinate input, call the service layer, and return responses. They should not contain business logic or database logic.

### 6) `@RestController` vs `@Controller`
`@RestController` combines `@Controller` and `@ResponseBody`, making it easier to return JSON directly.

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
A product service may expose endpoints for creating, retrieving, and updating catalogs while keeping business rules in services and repositories.
