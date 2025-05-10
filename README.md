# DockOps360
# DockOps360: Secure Docker Deployment with AWS Infrastructure

DockOps360 is a production-grade AWS Terraform project designed to automate the provisioning of cloud infrastructure for Dockerized applications. This project deploys a robust environment including VPCs, public subnets, EC2 instances, IAM roles/policies, and RDS with strong network security best practices.

---

## Architecture Overview

- **VPC**: Custom CIDR with two public subnets across AZs (`us-east-1a`, `us-east-1b`)
- **EC2**: Single instance launched using official Amazon Linux AMI
- **IAM**: Role and policy granting scoped EC2 access
- **RDS**: Subnet group to support future DB provisioning
- **Security**: Modular and locked-down access between components

---

## Modules

- `vpc`: Creates VPC, subnets, and outputs subnet/VPC IDs
- `iam`: IAM role and policy for EC2
- `ec2`: Launches EC2 with a referenced AMI and subnet
- `rds`: Sets up subnet group (no DB instance yet, extensible)

---

## Getting Started

### 1. Clone the Repo
```bash
git clone https://github.com/Peter-Agbenyega/DockOps360.git
cd DockOps360
2. Initialize Terraform
bash
Copy code
terraform init
3. Validate the Code
bash
Copy code
terraform validate
4. Apply the Infrastructure
bash
Copy code
terraform apply
5. Destroy the Infrastructure (optional)
bash
Copy code
terraform destroy

Author
Peter Christian Agbenyega
AWS Certified | Terraform Practitioner | DevSecOps Strategist
GitHub: Peter-Agbenyega