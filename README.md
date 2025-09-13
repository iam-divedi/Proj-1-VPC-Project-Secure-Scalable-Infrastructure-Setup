# Proj-1-VPC-Project-Secure-Scalable-Infrastructure-Setup
This project demonstrates how to design and implement a Virtual Private Cloud on AWS with public and private subnets, EC2 instances, load balancing, and network security.
# AWS Networking Project

## 🎯 Goal
- Build a **resilient, production-style network** that isolates application servers in private subnets and exposes them safely via an **Application Load Balancer** across two Availability Zones for **high availability and fault tolerance**.  
- Enable **outbound internet** for private instances using **NAT Gateways** without assigning public IPs, maintaining egress while preventing unsolicited inbound traffic.  
- Provide **controlled operator access** via a **Bastion Host** in a public subnet, acting as a secure jump point into private instances using SSH.

## ⚙ Services Used (Simple Explanation)

- **VPC (Virtual Private Cloud):** Private network for all servers (gated community).  
- **Subnets:** Divide network into **public** (internet access) and **private** (internal servers only).  
- **Route Tables:** Decide where network traffic goes.  
- **Internet Gateway (IGW):** Lets public servers access the internet.  
- **NAT Gateway:** Lets private servers reach the internet safely without public IPs.  
- **Security Groups:** Firewall for individual servers.  
- **Network ACLs:** Extra firewall for subnets.  
- **EC2 Instances:** Virtual servers in public & private subnets.  
- **SSH Key Pair:** Secret key to securely login to EC2.  
- **Bastion Host:** Jump server to access private EC2s safely.  
- **Auto Scaling Group (ASG):** Automatically add/remove EC2s based on traffic.  
- **Load Balancer (ALB):** Distributes traffic across multiple EC2s.  
- **Target Group:** Group of servers that the Load Balancer sends traffic to.

---
