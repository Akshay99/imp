# REST APIs

## Overview
REST APIs are a core building block of modern applications and are commonly discussed in backend interviews.

## Key Concepts
- HTTP methods and status codes
- Resource modeling
- Pagination and filtering
- Authentication and authorization
- Idempotency and versioning

## Frequently Asked Interview Questions
1. What is the difference between `PUT` and `PATCH`?
2. What are common HTTP status codes?
3. What is idempotency?
4. How do you version an API?

## Answers
`PUT` replaces a resource, while `PATCH` partially updates it. Status codes communicate success or failure clearly, like 200, 201, 400, 401, 404, 409, and 500. Idempotency means repeating a request does not change the result beyond the first application. APIs can be versioned through URLs, headers, or content negotiation.

## Code Examples
```http
GET /api/users/1 HTTP/1.1
Accept: application/json
```

## Best Practices
- Use meaningful URLs and standard HTTP methods.
- Return consistent responses and error payloads.
- Document endpoints clearly.

## Common Mistakes
- Using verbs in URLs.
- Returning inconsistent error shapes.
- Ignoring backwards compatibility.

## Real-World Scenarios
A mobile app may rely on REST APIs to fetch user data, submit forms, and manage authentication tokens reliably.
