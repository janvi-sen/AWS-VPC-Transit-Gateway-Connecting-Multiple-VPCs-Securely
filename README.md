# AWS-VPC-Transit-Gateway-Connecting-Multiple-VPCs-Securely
# 🌐 AWS VPC Transit Gateway – Connecting Multiple VPCs Securely

## 📘 Project Info

**Student Name**: Janvi Sen  
**PRN**: 20220802016  
**Course**: B.Tech TY (Cloud Computing)  
**Subject**: Fundamentals of Cloud Computing (Lab)  
**Institute**: School of Computer Science, Engineering and Applications (SCSEA)

---

## 📝 Description

This project demonstrates how to connect multiple Amazon VPCs securely using **AWS Transit Gateway (TGW)**. Transit Gateway acts as a central hub to enable communication between three VPCs, showcasing an enterprise-ready, scalable, and secure cloud network architecture.

---

## 🧠 Key Concepts

- Multi-VPC setup
- Subnet configuration (public and private)
- Internet Gateway (IGW) setup
- EC2 instance deployment
- Transit Gateway creation and attachment
- Custom route tables
- Secure communication via security groups

---

## 🛠️ Architecture Overview

| VPC Name | CIDR Block     | Type     | IGW | EC2 | TGW |
|----------|----------------|----------|-----|-----|-----|
| VPC-1    | 10.0.0.0/25    | Public   | ✅  | ✅  | ✅  |
| VPC-2    | 11.0.0.0/25    | Private  | ❌  | ✅  | ✅  |
| VPC-3    | 12.0.0.0/25    | Private  | ❌  | ✅  | ✅  |

---

## 🧰 Services Used

- Amazon VPC
- Amazon EC2
- AWS Transit Gateway
- Route Tables
- Internet Gateway
- Security Groups
- AWS Console

---

## 🚀 EC2 User Data (VPC-1 Web Server)

```bash
#!/bin/bash
yum update -y
yum install httpd -y
systemctl start httpd
systemctl enable httpd
echo "<h1>Welcome</h1>" > /var/www/html/index.html
