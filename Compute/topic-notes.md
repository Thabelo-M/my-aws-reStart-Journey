# Networking Notes

## What is Networking?
Networking in the cloud is about how resources, applications, and users communicate with each other securely and efficiently. In AWS, networking services make it possible to connect, route, and protect traffic between your resources, the internet, and even on-premises environments.

### Examples
- VPC (Virtual Private Cloud): A logically isolated section of the AWS cloud where I can launch resources. I control IP addressing, subnets, routing tables, and security settings.
- Subnets: Smaller sections within a VPC that group resources. They can be public (accessible from the internet) or private (internal only).
- Internet Gateway (IGW): A gateway that allows communication between a VPC and the internet.
- NAT Gateway: Lets private resources (like databases) connect out to the internet without being directly accessible from it.
- Route 53: AWS’s DNS service that translates human-friendly names (like www.example.com) into IP addresses and supports routing policies.
- VPN & Direct Connect: Services that securely link an on-premises network to AWS for hybrid setups.

## Key Concepts
CIDR Blocks:
- Defines IP address ranges in VPCs and subnets (e.g., 10.0.0.0/16). Helps organise and allocate IPs.
Security Groups & NACLs:
- Security Groups: Act like virtual firewalls for instances; they control inbound and outbound traffic at the instance level.
- NACLs (Network Access Control Lists): Work at the subnet level, allowing or denying traffic into/out of subnets.
Routing:
- Route tables determine how traffic flows inside a VPC, to the internet, or to other networks.
Load Balancers (Networking context):
- Distribute traffic at the network or application level (NLB/ALB) to ensure availability and performance.
Peering & Transit Gateway:
- VPC Peering: Connects two VPCs for private communication.
- Transit Gateway: A hub-and-spoke model to connect multiple VPCs and on-premises networks.

## Reflection
I’ve realised that networking is the backbone of cloud infrastructure. It’s not just about “connecting things,” but about securing, isolating, and directing traffic correctly. Choosing the right networking setup ensures performance, security, and scalability for applications.