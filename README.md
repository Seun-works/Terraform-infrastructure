# Terraform AWS Infrastructure Configuration

This repository contains Terraform configurations to provision and manage AWS resources. The `main.tf` file defines key components of a simple infrastructure setup, including a VPC, subnet, and an internet gateway.

## Key Components

1. **VPC (Virtual Private Cloud)**:
   - CIDR block: `10.123.0.0/16`
   - DNS support and hostnames enabled.
   - Tagged as `dev`.

2. **Public Subnet**:
   - CIDR block: `10.123.1.0/24`
   - Associated with the VPC.
   - Configured to map public IP addresses on launch.
   - Located in the `us-east-1a` availability zone.
   - Tagged as `dev-public`.

3. **Internet Gateway**:
   - Attached to the VPC to enable internet access for public resources.

## Prerequisites

- Install Terraform: [Terraform Download](https://www.terraform.io/downloads)
- Configure AWS credentials locally or using an IAM role.

## Usage

1. Clone this repository:
   ```bash
   git clone <repo-url>
   cd <repo-directory>
   ```

2. Initialize Terraform:
   ```bash
   terraform init
   ```

3. Review the plan:
   ```bash
   terraform plan
   ```

4. Apply the configuration:
   ```bash
   terraform apply
   ```

5. Destroy the resources if no longer needed:
   ```bash
   terraform destroy
   ```

## Notes

- Adjust CIDR blocks and availability zones in `main.tf` based on your requirements.
- Ensure proper IAM permissions to create and manage AWS resources.

---

Let me know if you'd like to customize this further!
