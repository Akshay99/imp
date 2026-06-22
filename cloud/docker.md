# Docker

## Overview
Docker makes it easier to package applications and their dependencies into portable containers.

## Key Concepts
- Images and containers
- Dockerfile creation
- Volumes and networking
- Docker Compose
- Multi-stage builds

## Frequently Asked Interview Questions
1. What is the difference between a container and a virtual machine?
2. What is a Dockerfile?
3. How do volumes help?
4. Why are multi-stage builds useful?

## Answers
A container shares the host OS kernel and is lighter than a VM. A Dockerfile defines how to build an image. Volumes persist data beyond the container lifecycle. Multi-stage builds reduce final image size and separate compile-time dependencies from runtime dependencies.

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
A team may containerize both frontend and backend services so they run consistently across development and deployment environments.
