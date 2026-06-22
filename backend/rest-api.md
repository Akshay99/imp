# REST APIs

## Overview
REST APIs are a core part of modern systems. Strong interview responses should explain HTTP semantics, status codes, security, versioning, and how to design APIs that are predictable and scalable.

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
5. Why should APIs return consistent error structures?
6. What is pagination and why is it needed?

## Detailed Answers
### 1) `PUT` vs `PATCH`
`PUT` replaces an entire resource, while `PATCH` partially updates it.

### 2) Common status codes
`200` indicates success, `201` means created, `204` means no content, `400` means bad request, `401` means unauthorized, `404` means not found, and `500` means server error.

### 3) Idempotency
An idempotent request gives the same result even if repeated. This is important for retry safety.

### 4) API versioning
Versioning can be done by URL, headers, or query parameters. The right choice depends on client needs and backward compatibility.

### 5) Consistent error structures
A standard error response makes client integration easier and helps teams debug problems faster.

### 6) Pagination
Pagination prevents huge responses and reduces memory and network pressure. It is also important for user experience.

## Code Examples
```http
GET /api/users/1 HTTP/1.1
Accept: application/json
```

## Best Practices
- Use meaningful resource naming.
- Return consistent responses and error payloads.
- Document endpoints clearly.

## Common Mistakes
- Using verbs in URLs.
- Returning inconsistent error shapes.
- Ignoring API versioning and backward compatibility.

## Real-World Scenarios
A mobile app may call REST APIs to fetch products, submit orders, and authenticate users while keeping payloads stable across releases.
