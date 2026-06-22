# Kubernetes

## Overview
Kubernetes is used to orchestrate containerized applications and manage deployment, scaling, and recovery.

## Key Concepts
- Pods, deployments, and services
- ReplicaSets
- ConfigMaps and Secrets
- Ingress and networking
- Rolling updates and scaling

## Frequently Asked Interview Questions
1. What is the difference between a pod and a container?
2. What is a deployment?
3. What is the purpose of a service?
4. How do rolling updates work?

## Answers
A pod is the smallest deployable unit and may contain one or more containers. A deployment manages the desired state of pods and supports updates. A service provides stable networking for pods. Rolling updates allow new versions to be introduced gradually.

## Code Examples
```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: app
spec:
  replicas: 2
```

## Best Practices
- Use readiness and liveness probes.
- Externalize configuration.
- Set resource requests and limits.

## Common Mistakes
- Ignoring probe configuration.
- Overlooking monitoring and alerting.
- Assuming a single pod is enough for production.

## Real-World Scenarios
A production platform may run multiple replicas behind a load balancer and scale them automatically.
