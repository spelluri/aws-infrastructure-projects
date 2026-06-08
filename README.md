# AWS Infrastructure Portfolio

A collection of hands-on AWS projects covering identity, networking, compute, storage,
databases, serverless, scaling, observability, and infrastructure-as-code. Each project is a
self-contained, deployable build with architecture notes, the reasoning behind key design
decisions, and full teardown steps.

A distinguishing thread runs through several of these projects: a **Raspberry Pi homelab node
acting as an on-prem server**, used to build genuine **hybrid-cloud** scenarios (on-prem → AWS
backups, metrics shipping, and running infrastructure-as-code against AWS from a local machine).

---

## Skills demonstrated

| Domain | Services / Tools |
|---|---|
| Identity & access | IAM users, groups, roles, policies, least-privilege, assume-role |
| Networking | VPC, public/private subnets, route tables, IGW, NAT, Security Groups, NACLs, Route 53 |
| Compute | EC2, AMIs, EBS, key pairs, user-data bootstrapping |
| Storage | S3, storage classes, versioning, lifecycle policies |
| Databases | RDS (relational), DynamoDB (NoSQL) |
| Scaling & HA | Application Load Balancer, Auto Scaling Groups, launch templates, multi-AZ |
| Serverless | Lambda, API Gateway, event-driven (S3 events, SQS/SNS) |
| Observability | CloudWatch metrics/logs/alarms, CloudWatch Agent, CloudTrail |
| Infrastructure as Code | Terraform, CloudFormation |
| Hybrid / on-prem | Raspberry Pi node integrated with AWS |

---

## Projects

| # | Project | Focus | Status |
|---|---------|-------|--------|
| 01 | [IAM Foundation](./01-iam-foundation) | Secure account baseline, least-privilege identity model | 🔲 Planned |
| 02 | [Multi-Tier VPC Network](./02-vpc-multi-tier-network) | Custom VPC, public/private subnets, NAT, routing, SGs | 🔲 Planned |
| 03 | [EC2 Web Tier](./03-ec2-web-tier) | Compute inside the VPC, AMIs, EBS, bootstrapping | 🔲 Planned |
| 04 | [Hybrid On-Prem → S3 Backup](./04-s3-hybrid-backup) | Raspberry Pi backs up to S3 with lifecycle + versioning | 🔲 Planned |
| 05 | [RDS Database Tier](./05-rds-database-tier) | Managed relational DB in a private subnet | 🔲 Planned |
| 06 | [Auto-Scaling Load-Balanced App](./06-autoscaling-load-balanced-app) | ALB + ASG across AZs | 🔲 Planned |
| 07 | [Serverless Image Pipeline](./07-serverless-image-pipeline) | S3 → Lambda → DynamoDB, API Gateway | 🔲 Planned |
| 08 | [Monitoring & Observability](./08-monitoring-observability) | CloudWatch + shipping Raspberry Pi metrics to AWS | 🔲 Planned |
| 09 | [Infrastructure as Code (Terraform)](./09-iac-terraform) | Reproduce infra declaratively, run from the Pi | 🔲 Planned |
| 10 | [CI/CD Pipeline](./10-cicd-pipeline) | Automated deploys to AWS | 🔲 Planned |

> Status legend: 🔲 Planned · 🚧 In Progress · ✅ Complete

---

## How each project is documented

Every project folder contains its own `README.md` following a consistent structure:

- **Overview & architecture** — what it is, with a diagram
- **Problem it solves** — the real-world need driving the design
- **What was built** — the concrete components
- **Key decisions** — the *why* behind the choices (the part interviews probe)
- **Deploy it** — reproducible steps
- **Validation** — proof the build was reproduced from scratch without instructions, plus a real failure that was debugged along the way
- **Gotchas & cost notes** — what bites people, what costs money
- **Teardown** — clean removal of all resources
- **Skills demonstrated** — quick reference

---

## Environment

- **AWS sandbox** for safe, disposable experimentation
- **Raspberry Pi 3** homelab node as the on-prem/edge component
- All work followed by **strict resource teardown** to keep environments clean

---

## A note on reproducibility

Where practical, projects include CLI commands or Terraform so the infrastructure can be
recreated from scratch. Secrets, credentials, and state files are **never** committed
(see `.gitignore`).
