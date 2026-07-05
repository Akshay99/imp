# Docker

## Overview
Docker is frequently discussed in interviews because it shows whether you understand packaging, portability, and deployment workflows.

## Key Concepts
- Images and containers
- Dockerfile creation
- Volumes and networking
- Docker Compose
- Multi-stage builds

## Frequently Asked Interview Questions (moved to spring-questions.md)

## Detailed Answers
### 1) Container vs VM
Containers share the host OS kernel and are lighter than virtual machines. VMs include their own OS guest layer.

### 2) Dockerfile
A Dockerfile defines how an image is built, including dependencies, file copies, and startup commands.

### 3) Volumes
Volumes persist data outside the container lifecycle so important data is not lost when a container restarts.

### 4) Multi-stage builds
Multi-stage builds allow you to separate compile-time and runtime steps, resulting in smaller and cleaner final images.

### 5) `COPY` vs `ADD`
`COPY` is simpler and clearer; `ADD` has extra features like URL support and tar extraction, but it is less predictable.

### 6) Immutability
Immutable images and containers reduce drift between environments and make deployments more predictable.

## Code Examples
```dockerfile
FROM node:18-alpine
WORKDIR /app
COPY . .
RUN npm install
CMD ["npm", "start"]
```

## Best Practices
- Keep images small and deterministic.
- Avoid embedding secrets in images.
- Use health checks and proper restart policies.

## Common Mistakes
- Running containers as root unnecessarily.
- Forgetting to persist important data.
- Ignoring startup and health checks.

## Real-World Scenarios
A team may containerize both frontend and backend services so they run consistently across development, testing, and production environments.
