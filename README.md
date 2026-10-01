\# AWS VPC with Public \& Private Subnets, NAT Gateway and Application Load Balancer



\## 📌 Project Overview



This project demonstrates a hands-on AWS VPC architecture using public and private subnets, EC2 instances, NAT Gateway, Internet Gateway, Application Load Balancer, route tables, and security groups.



The main objective of this project is to understand how an Internet-facing application can communicate with backend servers deployed inside private subnets while maintaining controlled network access.



\---



\## 🏗️ Architecture



The architecture consists of:



\- Amazon VPC

\- Public Subnets

\- Private Subnets

\- Internet Gateway

\- NAT Gateway

\- Application Load Balancer

\- EC2 Instances

\- Route Tables

\- Security Groups



\### High-Level Architecture



```text

&#x20;                        INTERNET

&#x20;                            │

&#x20;                            ▼

&#x20;                   ┌─────────────────┐

&#x20;                   │ Internet        │

&#x20;                   │ Gateway         │

&#x20;                   └────────┬────────┘

&#x20;                            │

&#x20;                            ▼

&#x20;                   ┌─────────────────┐

&#x20;                   │ Application     │

&#x20;                   │ Load Balancer   │

&#x20;                   └────────┬────────┘

&#x20;                            │

&#x20;                   ┌────────┴────────┐

&#x20;                   │                 │

&#x20;                   ▼                 ▼

&#x20;            Private Subnet     Private Subnet

&#x20;                   │                 │

&#x20;                   ▼                 ▼

&#x20;                EC2-01            EC2-02

&#x20;                   │

&#x20;                   │ Outbound Internet

&#x20;                   ▼

&#x20;             NAT Gateway

&#x20;                   │

&#x20;                   ▼

&#x20;            Internet Gateway

&#x20;                   │

&#x20;                   ▼

&#x20;                INTERNET

