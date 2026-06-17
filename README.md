# AWS VPC Network Architecture Project

## Project Overview

This project demonstrates the design and implementation of a secure and scalable AWS Virtual Private Cloud (VPC) architecture. The infrastructure is designed using public and private subnets distributed across multiple Availability Zones (AZs) to ensure high availability, fault tolerance, and network isolation.

The architecture follows AWS networking best practices and provides a strong foundation for deploying production-ready cloud applications.

---

## Project Highlights

* Designed a custom AWS VPC with CIDR block `10.0.0.0/16`
* Created 2 Public Subnets and 2 Private Subnets
* Configured Internet Gateway (IGW) for internet connectivity
* Implemented Public and Private Route Tables
* Distributed resources across multiple Availability Zones
* Established network segmentation for enhanced security
* Followed AWS Well-Architected Framework principles

---

## Architecture Diagram

![AWS VPC Architecture](https://github.com/user-attachments/assets/37ca44f7-536a-408d-b500-baa2026507ba)

---

## Architecture Details

### VPC Configuration

| Resource | CIDR Block  |
| -------- | ----------- |
| VPC      | 10.0.0.0/16 |

### Public Subnets

| Subnet          | CIDR Block  |
| --------------- | ----------- |
| Public-Subnet-1 | 10.0.1.0/24 |
| Public-Subnet-2 | 10.0.2.0/24 |

### Private Subnets

| Subnet           | CIDR Block  |
| ---------------- | ----------- |
| Private-Subnet-1 | 10.0.3.0/24 |
| Private-Subnet-2 | 10.0.4.0/24 |

### Networking Components

* Internet Gateway attached to VPC
* Public Route Table associated with Public Subnets
* Private Route Table associated with Private Subnets
* Route configured for internet access through Internet Gateway

---

## Architecture Flow

```text
Internet
    │
    ▼
Internet Gateway
    │
    ▼
Public Route Table
    │
 ┌──┴──┐
 ▼     ▼
Public Public
Subnet Subnet
  1      2

Private Route Table
    │
 ┌──┴──┐
 ▼     ▼
Private Private
Subnet  Subnet
  1       2
```

---

## AWS Services Used

* Amazon VPC
* Subnets
* Route Tables
* Internet Gateway (IGW)

---

## Implementation Summary

The following tasks were completed during implementation:

* Created a custom VPC with CIDR block `10.0.0.0/16`
* Created 2 Public Subnets and 2 Private Subnets
* Attached an Internet Gateway to the VPC
* Configured Public and Private Route Tables
* Associated subnets with their respective route tables
* Implemented internet access for public resources
* Validated subnet and routing configurations

---

## Multi-AZ Design

The architecture distributes public and private subnets across multiple Availability Zones to improve fault tolerance and availability.

### Benefits

* High Availability
* Better Fault Isolation
* Improved Disaster Recovery Readiness
* Production-Ready Infrastructure Design

---

## Project Outcome

Successfully created a secure and scalable AWS networking environment with:

* Network Isolation
* Public and Private Segmentation
* High Availability Design
* Secure Internet Connectivity
* Foundation for Multi-Tier Application Deployment

---

## Real-World Use Case

A typical enterprise cloud deployment uses a similar architecture pattern.

### Public Subnets

* Application Load Balancer (ALB)
* Bastion Host
* Web Servers

### Private Subnets

* Amazon RDS Databases
* Backend Services
* Internal APIs
* Application Servers

This design improves security by restricting direct internet access to sensitive resources while allowing public-facing applications to remain accessible.

---

## Key Learnings

Through this project, I gained hands-on experience with:

* AWS VPC Design
* CIDR Planning
* Public vs Private Subnets
* Route Tables
* Internet Gateway Configuration
* AWS Network Security Concepts
* Multi-AZ Architecture Design

---

## Interview Questions Covered

1. What is a VPC?
2. What is CIDR notation?
3. What is the difference between Public and Private Subnets?
4. How does a subnet become public?
5. What is an Internet Gateway?
6. What is a Route Table?
7. Why are databases deployed in Private Subnets?
8. What are the benefits of Multi-AZ architecture?

---

## Screenshots

### Resource Map

* AWS Resource Map

### Networking Configuration

* VPC Dashboard
* Public & Private Subnets
* Route Tables
* Internet Gateway

---

## Author

**Ayush Garg**

AWS Cloud & DevOps Engineer

LinkedIn: https://www.linkedin.com/in/ayushgarg0925
