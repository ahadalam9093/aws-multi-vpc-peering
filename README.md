
# EWB AWS INTERNSHIP – OCTOBER 2026

# AWS Multi-VPC Peering

## 📌 Project Overview

This project demonstrates how to establish private communication between two isolated Amazon Virtual Private Clouds (VPCs) using AWS VPC Peering.

VPC Peering allows resources in different VPCs to communicate using private IP addresses without routing application traffic through the public internet.

The project focuses on AWS networking fundamentals, routing configuration, security group management, EC2 deployment, and secure remote access through a Bastion Host.

## 🎯 Project Objectives

- Understand AWS VPC architecture and networking.
- Create and configure multiple VPCs.
- Design public and private subnets.
- Configure Internet Gateway and route tables.
- Establish connectivity using VPC Peering.
- Implement network security using Security Groups.
- Configure SSH access through a Bastion Host.
- Validate private connectivity between EC2 instances.

## 🛠️ AWS Services Used

| AWS Service | Purpose |
|---|---|
| Amazon VPC | Create isolated virtual networks |
| Amazon EC2 | Host virtual servers |
| VPC Peering | Connect two VPCs privately |
| Internet Gateway | Provide internet connectivity |
| Route Tables | Control network traffic routing |
| Security Groups | Manage instance-level traffic |
| Subnets | Organize public and private resources |

## 🏗️ Network Architecture

The project consists of two VPCs.

### VPC-A

- CIDR Block: `10.10.0.0/16`
- Public Subnet: `10.10.1.0/24`
- Private Subnet: `10.10.2.0/24`
- Internet Gateway attached.
- Bastion Host deployed in the public subnet.
- Private EC2 instance deployed in the private subnet.

### VPC-B

- CIDR Block: `10.20.0.0/16`
- Private Subnet: `10.20.1.0/24`
- Private EC2 instance deployed in the private subnet.

Both VPCs communicate through a VPC Peering Connection.

## ⚙️ Project Implementation Steps

1. Create two separate VPCs with non-overlapping CIDR blocks.
2. Create public and private subnets.
3. Create and attach an Internet Gateway to VPC-A.
4. Configure custom route tables.
5. Associate route tables with the appropriate subnets.
6. Create and configure Security Groups.
7. Launch EC2 instances in the respective subnets.
8. Establish a VPC Peering Connection between VPC-A and VPC-B.
9. Accept the peering request.
10. Update both VPC route tables to enable bidirectional communication.
11. Configure SSH access through the Bastion Host.
12. Test private connectivity between EC2 instances using ICMP Ping.

## 🔐 Security Configuration

Security Groups control access to the EC2 instances.

- Bastion Host: SSH access restricted to the administrator's public IP.
- App-A: SSH access from the authorized Bastion Host.
- App-B: SSH access from authorized sources.
- ICMP traffic: Allowed between the required private network ranges for connectivity testing.

## 🧪 Testing and Validation

The following tests help validate the network configuration:

- Verify the VPC Peering Connection status.
- Verify route table entries in both VPCs.
- Test SSH connectivity to the private EC2 instance through the Bastion Host.
- Test ICMP connectivity between App-A and App-B.
- Verify successful bidirectional communication.
- Temporarily remove the ICMP security group rule to understand firewall behavior.

## 📚 Learning Outcomes

- VPC creation and configuration.
- Public and private subnet architecture.
- CIDR allocation and IP addressing.
- Route table configuration.
- VPC Peering and private communication.
- Security Group management.
- Bastion Host architecture.
- SSH and ICMP connectivity testing.
- Basic AWS network troubleshooting.

## 🧹 Resource Cleanup

After completing the practical implementation:

1. Terminate EC2 instances.
2. Delete the VPC Peering Connection.
3. Detach and delete the Internet Gateway.
4. Delete custom route tables.
5. Delete associated subnets.
6. Delete the custom VPCs.
7. Verify that no unnecessary billable resources remain.

## 🏁 Conclusion

This project explores AWS networking by demonstrating how two isolated VPCs can communicate privately using VPC Peering.

It provides an understanding of network architecture, private routing, security controls, and troubleshooting in an AWS cloud environment.

---

**Project:** AWS Multi-VPC Peering  
**Program:** EWB AWS Internship – October 2026


<footer> lets connect & configure | <a href="www.linkedin.com/in/ahad-alam-7797973b2">LinkedIn
</a></footer>
