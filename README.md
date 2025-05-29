# ☁️ terraform-ops

This repository contains modular Terraform infrastructure templates, reusable provisioning modules, and helper utilities designed to manage secure, scalable environments across AWS and Azure.

Built for infrastructure engineers, cloud practitioners, and DevSecOps learners who want repeatable, audit-ready IaC operations.

## 📁 Repo Structure

| Folder        | Description                                                           |
|---------------|-----------------------------------------------------------------------|
| `modules/`     | Self-contained reusable Terraform modules (e.g., EC2, S3, VPC, Azure VM) |
| `examples/`    | Usage examples and test deployments using the modules                 |
| `templates/`   | Provider configs, remote state setups, backend templates              |
| `utils/`       | Shell helpers for state cleanup, plan comparison, automation tips     |
| `docs/`        | Terraform process docs, linting, and IaC best practices               |

## 🚀 Key Modules

- `ec2-instance/`: Create tagged, key-based EC2 with SGs and EBS encryption
- `s3-bucket/`: Hardened bucket with versioning, encryption, public block
- `vpc-basic/`: Base VPC layout with subnets and routing tables
- `azure-vm/`: Secure Azure VM with NSG and optional diagnostics

## 🔧 Example Deployments

```bash
cd examples/aws-single-instance/
terraform init
terraform apply -var-file=terraform.tfvars

