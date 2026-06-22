# Spring Security

## Overview
Spring Security is essential for protecting applications. In interviews, you should be able to explain authentication, authorization, roles, JWT, and why secure defaults are important.

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
5. Why should passwords be hashed?
6. What is the difference between roles and permissions?

## Detailed Answers
### 1) Authentication vs authorization
Authentication verifies who the user is; authorization decides what the user can do. A login flow is authentication, while checking whether a user can delete a record is authorization.

### 2) JWT
A JWT contains claims and is digitally signed so the receiving system can verify it. It is commonly used in stateless APIs because the server does not need to store session state.

### 3) CSRF
CSRF attacks trick a browser into making requests on behalf of a logged-in user. Protection methods include CSRF tokens and same-site cookie policies.

### 4) Securing REST APIs
REST APIs should use HTTPS, proper authentication, authorization checks, input validation, and rate limiting where needed.

### 5) Password hashing
Passwords should be hashed using a strong algorithm such as BCrypt or PBKDF2 so that even if the database leaks, attackers cannot easily recover the original passwords.

### 6) Roles vs permissions
Roles are broad groups such as USER or ADMIN. Permissions are finer-grained actions such as READ_ORDER or DELETE_ORDER.

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
- Keep authorization rules explicit.

## Common Mistakes
- Storing passwords insecurely.
- Forgetting to secure sensitive endpoints.
- Relying on weak token validation.

## Real-World Scenarios
A banking system may secure endpoints according to role and validate tokens on every request to protect financial information.
