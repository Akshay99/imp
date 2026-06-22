# Spring Security

## Overview
Spring Security helps secure applications through authentication, authorization, and protection against common web threats.

## Key Concepts
- Authentication and authorization
- Filters and security chain
- Roles and permissions
- JWT and OAuth2 basics
- CSRF protection

## Frequently Asked Interview Questions
1. What is the difference between authentication and authorization?
2. How does JWT work?
3. What is CSRF?
4. How do you secure REST APIs?

## Answers
Authentication verifies who a user is, while authorization determines what a user can do. JWT stores claims in a signed token that can be checked by the server. CSRF targets browser-based state changes, and protection is usually provided through tokens or same-site policies. Secure APIs should use HTTPS, strong authentication, and explicit permission checks.

## Code Examples
```java
http
    .authorizeHttpRequests(auth -> auth
        .requestMatchers("/public/**").permitAll()
        .anyRequest().authenticated()
    );
```

## Best Practices
- Prefer stateless authentication for APIs.
- Use strong password hashing.
- Keep authorization rules explicit and reviewed.

## Common Mistakes
- Storing passwords insecurely.
- Forgetting to secure sensitive endpoints.
- Relying on weak token validation.

## Real-World Scenarios
A banking application may protect endpoints by role, enforce HTTPS, and validate tokens on each request.
