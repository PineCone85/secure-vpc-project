# Secure VPC Project (AWS Console)

This project demonstrates how to build a **secure, multi-tier Virtual Private Cloud (VPC)** on AWS using the AWS Management Console. The goal is to design a network that follows **security best practices**, with strict traffic controls between public-facing and private resources.

## 🔹 What I Built
- **VPC** with CIDR block `10.0.0.0/16`
- **Public subnet** hosting a web server (EC2 instance)
- **Private subnet** simulating a database server (EC2 instance)
- **Internet Gateway (IGW)** so the public instance can be reached from the internet
- **NAT Gateway** so the private instance can access the internet (for updates) without being exposed
- **Security Groups & NACLs** to strictly control traffic flows

## 🔹 Why This Matters
This project is a hands-on demonstration of:
- Network segmentation (public vs private resources)
- Principle of least privilege (restricting access tightly)
- Layered security using **Security Groups** and **Network ACLs**
- How AWS networking components work together

These concepts are the foundation of **cloud security architecture**.

## 🔹 Step-by-Step Documentation
Each stage of the project is documented in detail with explanations and screenshots:

1. [VPC & Subnet Setup](./docs/01-vpc-setup.md)  
2. [Internet Gateway](./docs/02-internet-gateway.md)  
3. [NAT Gateway](./docs/03-nat-gateway.md)  
4. [Security Groups & NACLs](./docs/04-security-groups-nacls.md)  
5. [Public EC2 Web Server](./docs/05-ec2-public.md)  
6. [Private EC2 Database Server](./docs/06-ec2-private.md)  
7. [Testing & Validation](./docs/07-testing.md)  

## 🔹 Future Improvements
- Recreate the same architecture using **Terraform** (Infrastructure-as-Code)  
- Add monitoring/logging with **VPC Flow Logs** and **CloudWatch**  

---

## ✅ Skills Demonstrated
- AWS VPC, subnets, IGW, NAT
- Security Groups & Network ACLs
- EC2 provisioning
- Network security design
- Documentation & diagramming
