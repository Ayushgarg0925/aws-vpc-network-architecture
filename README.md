# AWS VPC Network Architecture Project

## Project Overview

This project demonstrates the creation of a secure AWS networking environment using Amazon VPC. The architecture consists of public and private subnets distributed across multiple Availability Zones to improve security and availability.

# Architecture Diagram

Internet
    |
Internet Gateway
    |
Public Route Table
    |
-------------------------
|                       |
Public Subnet-1     Public Subnet-2
|                       |
-------------------------
Private Route Table
|                       |
Private Subnet-1    Private Subnet-2

## Architecture

VPC CIDR: 10.0.0.0/16

Public Subnet 1: 10.0.1.0/24

Public Subnet 2: 10.0.2.0/24

Private Subnet 1: 10.0.3.0/24

Private Subnet 2: 10.0.4.0/24

Internet Gateway attached to VPC

Public Route Table associated with Public Subnets

Private Route Table associated with Private Subnets

## AWS Services Used

- Amazon VPC
- Subnets
- Route Tables
- Internet Gateway

## Implementation Steps

### Step 1: Create VPC

Name: Test-VPC

CIDR Block: 10.0.0.0/16

### Step 2: Create Public Subnets

Public-Subnet-1 (10.0.1.0/24)

Public-Subnet-2 (10.0.2.0/24)

### Step 3: Create Private Subnets

Private-Subnet-1 (10.0.3.0/24)

Private-Subnet-2 (10.0.4.0/24)

### Step 4: Create Internet Gateway

Name: Test-IGW

Attach Internet Gateway to VPC

### Step 5: Configure Route Tables

Public Route Table

Route:

Destination: 0.0.0.0/0

Target: Internet Gateway

Associate Public Subnets

Private Route Table

Associate Private Subnets

## Project Outcome

Successfully created a secure and scalable AWS networking environment with:

- Network Isolation
- Public and Private Segmentation
- High Availability Design
- Internet Connectivity for Public Resources

# Real World Use Case

A typical production deployment uses:

    - Public Subnets:
        Application Load Balancer
        Bastion Host
        Web Servers

    - Private Subnets:
        Databases
        Internal Services
        Backend Applications

This architecture pattern is commonly used in enterprise cloud environments.

## Screenshots

Add the following screenshots:

- VPC Dashboard
- Subnets
- Internet Gateway
- Route Tables
- Resource Map

## Author

Ayush Garg

AWS Cloud & DevOps Engineer
