# Networking Lab: Configuring an Amazon VPC

## Overview
In this lab, I’ll walk through the process of creating and configuring an Amazon Virtual Private Cloud (VPC). A VPC is a logically isolated network in AWS that allows you to launch AWS resources securely and control network traffic.

By the end of this lab, I’ll have a custom VPC with public and private subnets, route tables, internet and NAT gateways, and EC2 instances to test connectivity.

## Objective
1. Create a VPC with a custom CIDR block
2. Configure public and private subnets
3. Set up route tables and gateways for internet access
4. Launch EC2 instances in public and private subnets
5. Apply security groups and network ACLs for controlled access
6. Test connectivity between resources

## Prerequisites
1. An AWS account with access to VPC and EC2 services
2. Basic understanding of networking concepts: subnets, CIDR blocks, route tables
3. Existing key pair or the ability to create one for SSH/RDP access to EC2 instances

## Steps Taken
1. Create a VPC – Open the VPC Dashboard and create a new VPC with a custom CIDR block (e.g., 10.0.0.0/16).
2. Add Subnets – Create public and private subnets in different Availability Zones for high availability.
3. Configure Route Tables – Associate route tables with subnets and define routes for internet and internal traffic.
4. Set Up Gateways – Attach an Internet Gateway to the VPC and a NAT Gateway for private subnet internet access.
5. Launch EC2 Instances – Deploy instances in public and private subnets to test connectivity.
6. et Security Groups and NACLs – Control inbound and outbound traffic for each instance and subnet.
7. Test Connectivity – SSH or RDP into the public instance and test connections to the private instance.

## Clean Up
Delete the VPC, subnets, route tables, gateways, EC2 instances, and security groups to avoid unnecessary AWS charges.

## Wrap-Up
Through this lab, I learned how to design and deploy a secure and functional VPC. It reinforced the importance of subnetting, routing, and layered security when managing AWS networks.

## Screenshots
**Creating an EC2 Instance**

<img src="CreateEC2.png" alt="EC2 Creation" width="400"/>

**EC2 Instance Connect session**

<img src="EC2Connect.png" alt="EC2 Connection" width="400" height="100"/>

- Retrieves the Availability Zone of the running instance from metadata
- Extracts the Region from the Availability Zone and sets it as an environment variable
- Uses AWS Systems Manager (SSM) with get-parameters to fetch the AMI ID from Parameter Store
- The requested AMI is Amazon Linux 2 (same as used for the bastion host)
- Stores the AMI ID in an environment variable called AMI

**Creating a new EC2 instance using EC2 Instance Connect session**

<img src="EC2ConnectNewInstance.png" alt="Web Server Instance" width="400" height="100"/>
