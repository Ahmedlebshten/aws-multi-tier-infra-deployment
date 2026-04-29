# 🚀 AWS Multi-Tier Infrastructure Deployment

This project demonstrates the deployment of a complete multi-tier AWS infrastructure across multiple Availability Zones following best practices for scalability, security, and high availability.

## 🖼️ System Architecture
<img width="1536" height="1024" alt="new-aws" src="https://github.com/user-attachments/assets/783e30bd-7b84-4392-9cd0-9cb1bbbaf66f" />

## 📌 Architecture Overview

#### The infrastructure includes:
- Two separate VPCs
- Public and Private Subnets
- EC2 instances distributed across multiple AZs
- Application Load Balancer (ALB)
- S3 bucket for centralized log storage
- IAM roles & policies for secure access
- VPC Peering between both VPCs
- Automated log upload using shell scripting

____

## 🏗️ Infrastructure Components

🌐 VPC-01 (10.0.0.0/16)
- 2 Public Subnets (AZ-1a & AZ-1b)
- 2 Private Subnets
- EC2 Instances (Nginx – Public IP)
- IAM Role attached to EC2
- ALB distributing traffic across instances

🔐 VPC-02 (192.168.0.0/24)
- Private Subnet
- EC2 instance (Private IP only)
- Connected via VPC Peering

📦 S3 Bucket
- Stores Nginx access logs
- Logs uploaded automatically every 30 minutes using cron job

____

## ⚙️ Tools & Technologies Used
- AWS
- EC2
- S3
- IAM
- Application Load Balancer
- VPC & VPC Peering
- Bash Scripting
- Amazon Linux 2

____

## 🔄 Automation
- Shell script uploads Nginx logs to S3 every 30 minutes
- IAM role used instead of hardcoded credentials (best practice)
- Multi-AZ deployment ensures high availability

____

## 🎯 Key Learning Outcomes
- Designing secure AWS network architecture
- Implementing multi-tier infrastructure
- Working with ALB & traffic distribution
- Configuring VPC Peering
- Managing IAM Roles securely
- Automating operational tasks using Bash

