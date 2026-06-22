# AWS

## Overview
AWS is a common cloud platform in interviews because it tests understanding of core services, security, availability, and trade-offs in distributed systems.

## Key Concepts
- EC2, S3, RDS, Lambda
- IAM and permission management
- Load balancing and auto-scaling
- Networking basics
- Monitoring and cost efficiency

## Frequently Asked Interview Questions
1. What is the difference between EC2 and Lambda?
2. What is IAM?
3. How does S3 differ from EBS?
4. What is the role of a load balancer?
5. Why is least-privilege access important?
6. What is the difference between vertical and horizontal scaling?

## Detailed Answers
### 1) EC2 vs Lambda
EC2 gives you managed virtual machines, while Lambda runs code without requiring server management. EC2 is better when you need full control; Lambda is useful for event-driven or short-lived workloads.

### 2) IAM
IAM controls who can do what on AWS resources. It is essential for security and compliance.

### 3) S3 vs EBS
S3 is object storage for files and static content; EBS is block storage attached to a compute resource.

### 4) Load balancer
A load balancer distributes traffic across multiple instances so the system stays available and performs better under load.

### 5) Least-privilege access
Least-privilege access keeps permissions minimal, reducing the risk of accidental or malicious misuse.

### 6) Vertical vs horizontal scaling
Vertical scaling increases capacity on one machine. Horizontal scaling adds more machines to share the work and improve availability.

## Code Examples
```bash
aws s3 ls
```

## Best Practices
- Follow least-privilege access.
- Use managed services when possible.
- Monitor cost and usage.

## Common Mistakes
- Leaving security groups too open.
- Ignoring backup and recovery planning.
- Misunderstanding storage types.

## Real-World Scenarios
An e-commerce platform may use S3 for assets, RDS for relational data, and EC2 or Lambda for application logic.
