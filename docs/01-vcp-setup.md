# Step 1: VPC & Subnet Setup

In this step, I created the foundation of the secure network: the **VPC** and its **subnets**.

---

## 🔹 What I Did
1. Opened the AWS Management Console → **VPC service**.  
2. Created a new VPC with the following settings:
   - **Name**: `secure-vpc`
   - **CIDR block**: `10.0.0.0/16`  
   - Tenancy: default
3. Created two subnets:
   - **Public Subnet** → `10.0.1.0/24` (for the web server)  
   - **Private Subnet** → `10.0.2.0/24` (for the database)  
4. Enabled **Auto-assign Public IPv4** for the **public subnet** so instances here can be accessed directly.  
5. Left **private subnet** without public IP assignment.

---

## 🔹 Why This Matters
- A **VPC** is like a private network in the cloud — isolated from others.  
- Splitting into **public** and **private** subnets follows the **principle of least privilege**:  
  - Public-facing resources go in the public subnet.  
  - Sensitive resources (like databases) stay hidden in the private subnet.  

This separation is the foundation of secure cloud design.

---

