# Amazon EC2

Amazon Elastic Compute Cloud (EC2) is AWS's virtual server service for running scalable applications in the cloud.

Users can launch virtual machines on demand while choosing the operating system, instance type, networking, and storage configuration that best fits their workloads.

This document presents the core concepts of Amazon EC2, including instance types, purchasing options, Amazon Machine Images (AMIs), Security Groups, Amazon EBS, snapshots, and scaling strategies.

---

## Instance Types

EC2 instances are available in multiple families, each optimized for different workloads.

| Instance Family | Optimized For |
|-----------------|---------------|
| General Purpose | Balanced compute, memory and networking |
| Compute Optimized | CPU-intensive workloads |
| Memory Optimized | Memory-intensive applications |
| Accelerated Computing | GPU and hardware acceleration |
| Storage Optimized | High-performance local storage |

Choosing the correct instance family improves both application performance and cost efficiency.

---

## Instance Naming Convention

EC2 instance names provide information about their characteristics.

Example:

`c7gn.xlarge`

- **c** → Instance family
- **7** → Generation
- **gn** → Additional capabilities
- **xlarge** → Instance size

Newer generations generally offer better performance and efficiency.

---

## Amazon Machine Images (AMI)

Amazon Machine Images contain the operating system and software configuration required to launch EC2 instances.

An AMI serves as a template for creating new EC2 instances.

AMIs can be:

- Public
- Private
- Custom

Creating custom AMIs allows environments to be replicated consistently and reduces deployment time.

---

## Security Groups

Security Groups function as virtual firewalls for EC2 instances.

They control:

- Inbound traffic
- Outbound traffic
- Allowed protocols
- Ports
- Source and destination IP addresses

Security Groups are stateful, meaning return traffic is automatically allowed for any permitted connection.

---

## Amazon Elastic Block Store (EBS)

Amazon Elastic Block Store (EBS) offers persistent block storage volumes that can be attached to EC2 instances.

It behaves like a virtual hard drive and is commonly used for:

- Operating systems
- Application data
- Databases
- Persistent storage

EBS volumes are designed for low-latency access and are tied to a specific Availability Zone.

---

## Snapshots

EBS snapshots are point-in-time backups of EBS volumes.

Snapshots are stored internally in Amazon S3 and can be used for:

- Backup and recovery
- Disaster recovery
- Creating new EBS volumes
- Replicating data across Regions

Snapshots improve data resilience and provide a straightforward restore mechanism for EC2-based workloads.

---

## AMI vs. EBS Snapshot

Although related, AMIs and EBS snapshots serve different purposes.

- **AMI:** Used to launch EC2 instances with a predefined operating system and software configuration.
- **EBS Snapshot:** Used to create point-in-time backups of EBS volumes.

Snapshots are often used as part of the process of creating or preserving AMIs.

---

## Purchasing Options

AWS offers different pricing models depending on workload characteristics.

### On-Demand

Pay only for the resources while they are running.

Best for:

- Testing
- Development
- Unpredictable workloads

### Reserved Instances

Commit to a specific instance type for a 1- or 3-year term in exchange for reduced pricing.

Best for:

- Stable workloads
- Long-running applications

### Savings Plans

Flexible pricing model that offers reduced rates in exchange for a committed usage amount, measured in dollars per hour, over a 1- or 3-year term.

Unlike Reserved Instances, Savings Plans commit to a spend rate rather than a specific instance type, offering more flexibility.

Two main types are available:

- **Compute Savings Plans:** Apply across instance families, sizes, Regions, operating systems, AWS Fargate, and AWS Lambda.
- **EC2 Instance Savings Plans:** Apply to a specific EC2 instance family within a Region and provide the highest savings for predictable workloads.

Best for:

- Workloads with predictable usage
- Long-term cost optimization

### Spot Instances

Use spare AWS capacity at significantly lower prices.

Best for:

- Fault-tolerant workloads
- Batch processing
- Temporary jobs

Spot Instances may be interrupted by AWS when capacity is reclaimed.

---

## Cost Optimization

Cloud infrastructure costs can be reduced significantly by matching workloads to the appropriate compute resources and pricing models.

Some common practices include:

- Choosing the appropriate instance family
- Stopping or terminating unused instances
- Removing idle resources
- Scaling infrastructure according to demand

---

## Scaling

Applications can scale in two ways.

### Vertical Scaling

Increase the resources of a single instance.

Example:

`t3.micro` → `t3.large`

### Horizontal Scaling

Increase the number of instances running simultaneously behind a load balancer.

This approach is commonly used to improve availability, fault tolerance, and scalability.

---

## References

See [references.md](references.md) for the official AWS documentation and additional learning resources.