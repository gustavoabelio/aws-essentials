# AWS Fundamentals

Before exploring individual AWS services, it's important to understand the fundamental concepts that form the foundation of the AWS Cloud.

---

## Cloud Computing

Cloud computing provides on-demand access to computing resources over the internet, eliminating the need to provision and maintain physical infrastructure.

### Cloud Service Models

- **IaaS (Infrastructure as a Service):** Delivers virtualized computing resources such as virtual machines, storage, and networking.
- **PaaS (Platform as a Service):** Offers a managed platform for developing and deploying applications.
- **SaaS (Software as a Service):** Provides complete software applications over the internet.

---

## AWS Global Infrastructure

AWS operates a globally distributed infrastructure designed for high availability, fault tolerance, scalability, and low latency.

### Regions

A Region is a physical geographic area where AWS operates multiple isolated data centers distributed across Availability Zones.

### Availability Zones

Each Region contains one or more Availability Zones (AZs), which are isolated locations connected through high-speed, low-latency networks.

This architecture allows applications to achieve higher availability and resilience by distributing resources across multiple Availability Zones.

---

## Managed Services

Managed services reduce operational overhead by allowing AWS to manage the underlying infrastructure, enabling developers to focus on application development instead of server administration.

Examples of managed AWS services include Amazon S3, AWS Lambda, Amazon RDS, and Amazon DynamoDB.

---

## AWS Account

Access to AWS services requires an AWS account. For security reasons, the root account should be reserved for administrative tasks that cannot be performed by IAM users.

---

## Identity and Access Management (IAM)

AWS Identity and Access Management (IAM) enables secure control over access to AWS resources.

Recommended practices include:

- Creating IAM users instead of using the root account for daily operations.
- Enabling Multi-Factor Authentication (MFA).
- Assigning permissions through IAM Groups and Policies.
- Following the principle of least privilege whenever possible.

---

## Cost Management

AWS provides services that help monitor and optimize cloud spending.

### AWS Budgets

AWS Budgets allows users to define spending limits and receive alerts when costs or usage exceed predefined thresholds.

---

## Access Methods

AWS resources can be managed through different interfaces depending on the workflow.

- **AWS Management Console:** Web-based graphical interface.
- **AWS CloudShell:** Browser-based terminal with the AWS CLI preconfigured.
- **AWS CLI:** Command-line interface for managing AWS resources and automating tasks.

The AWS CLI can be configured using the `aws configure` command, which stores credentials and default settings for authenticated access.

---

## References

See [references.md](references.md) for the official AWS documentation and additional learning resources.
