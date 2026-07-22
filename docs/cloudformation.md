# AWS CloudFormation

AWS CloudFormation is an Infrastructure as Code (IaC) service that enables developers to provision and manage AWS resources using declarative templates.

Instead of creating resources manually through the AWS Management Console, CloudFormation automates infrastructure deployment, making environments reproducible, consistent, and easier to maintain.

This document introduces the core concepts of AWS CloudFormation, including templates, stacks, resources, parameters, and common use cases.

---

## Infrastructure as Code (IaC)

Infrastructure as Code (IaC) is the practice of managing infrastructure through code rather than manual configuration.

Using IaC provides several advantages:

- Repeatable deployments
- Version-controlled infrastructure
- Reduced human error
- Faster environment provisioning
- Consistent configurations

CloudFormation is AWS's native Infrastructure as Code service.

---

## Templates

A CloudFormation template defines the infrastructure that should be created.

Templates are written in either:

- JSON
- YAML

A template describes AWS resources and their configurations in a declarative format.

---

## Stacks

A stack is a collection of AWS resources created and managed together using a single CloudFormation template.

CloudFormation keeps track of every resource within the stack, making updates and deletions easier to manage.

---

## Resources

Resources are the AWS services defined inside a template.

Examples include:

- Amazon EC2
- Amazon S3
- AWS Lambda
- Amazon DynamoDB
- Amazon VPC
- Amazon RDS

Resources are automatically provisioned when the stack is created.

---

## Parameters

Parameters allow templates to receive user-defined values during deployment.

This makes templates reusable across different environments without modifying the template itself.

Common examples include:

- Instance type
- Resource names
- Environment (Development, Testing, Production)

---

## Outputs

Outputs expose useful information after a stack is created.

Examples include:

- Instance IDs
- Bucket names
- Public IP addresses
- Resource ARNs

Outputs can also be referenced by other CloudFormation stacks.

---

## Stack Updates

CloudFormation manages infrastructure changes by comparing the current stack with the updated template.

When possible, resources are updated without requiring complete replacement, reducing deployment risks.

---

## Common Use Cases

AWS CloudFormation is commonly used for:

- Infrastructure automation
- Environment provisioning
- Application deployment
- Development and production environments
- Disaster recovery
- Reproducible cloud architectures

---

## References

See [references.md](references.md) for the official AWS documentation and additional learning resources.