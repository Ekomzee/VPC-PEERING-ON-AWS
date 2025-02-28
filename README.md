# AWS VPC Peering Guide #
Introduction
This repository provides a simple guide to setting up VPC Peering in AWS. It covers the configuration steps, common use cases, and best practices to ensure secure and efficient cross-VPC communication.

# What is VPC Peering? #
VPC Peering is a private network connection between two AWS VPCs, allowing direct communication without using the internet or VPN.

# Prerequisites #
Two VPCs with non-overlapping CIDR blocks
IAM permissions to create and manage VPC Peering connections
Ability to update route tables and security groups

## How to Set Up VPC Peering ##
Create a Peering Connection
Go to VPC Dashboard → Peering Connections → Create Peering Connection
Select source and destination VPCs
Accept the request in the target VPC
Update Route Tables

Add routes in both VPCs to allow traffic via the Peering Connection
Modify Security Groups

Allow traffic between VPCs based on required protocols
Test the Connection

Use ping to verify connectivity

## Common Use Cases ##
Communication between VPCs in different AWS accounts
Isolating backend services in separate VPCs
Enabling cross-region connectivity for multi-cloud architectures

## Best Practices ##
Use non-overlapping CIDR blocks to prevent routing conflicts
Enable DNS resolution for private hostname access (enableDnsSupport)
Monitor traffic using AWS CloudWatch and VPC Flow Logs
Troubleshooting
Can’t reach the other VPC? Check route tables and security groups
DNS resolution not working? Enable DNS hostnames in VPC settings
Connection latency issues? Prefer same-region peering for better performance







