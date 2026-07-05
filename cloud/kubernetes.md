# Kubernetes

## Overview
Kubernetes is a major interview topic for cloud and platform roles because it tests understanding of deployment, scaling, self-healing, and networking.

## Key Concepts
- Pods, deployments, and services
- ReplicaSets
- ConfigMaps and Secrets
- Ingress and networking
- Rolling updates and scaling

## Frequently Asked Interview Questions (moved to spring-questions.md)

## Detailed Answers
### 1) Pod vs container
A pod is the smallest deployable unit in Kubernetes and may contain one or more containers. A container is the runtime process itself.

### 2) Deployment
A deployment describes the desired state of an application and manages rollout behavior, scaling, and updates.

### 3) Service
A service gives a stable network endpoint for a set of pods, allowing traffic to flow reliably even as pods move or restart.

### 4) Rolling updates
Rolling updates gradually replace old pods with new ones so the application remains available during the change.

### 5) ConfigMap vs Secret
ConfigMap stores non-sensitive configuration values. Secret stores sensitive information such as passwords or tokens.

### 6) Probes
Readiness probes determine when a pod is ready to receive traffic. Liveness probes determine whether the container should be restarted.

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
A production platform may run multiple replicas behind a load balancer and scale them automatically based on traffic.
