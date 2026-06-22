# AWS

## Overview
AWS provides cloud services for compute, storage, networking, and managed platforms used by modern applications.

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

## Answers
EC2 runs virtual machines, while Lambda runs code without managing servers. IAM controls access to AWS services. S3 is object storage, while EBS is block storage. A load balancer distributes traffic across instances to improve availability and reliability.

## Code Examples
```bash
aws s3 ls
```

## Best Practices
- Follow least-privilege access.
- Use managed services when possible.
- Monitor cost and resource usage.

## Common Mistakes
- Leaving security groups too open.
- Ignoring backup and recovery planning.
- Misunderstanding storage types.

## Real-World Scenarios
An e-commerce platform may use S3 for assets, RDS for relational data, and EC2 or Lambda for application logic.
