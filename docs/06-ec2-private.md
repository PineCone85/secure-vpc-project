## 🔹 What I Did
1. Launched a new **EC2 instance** in the **private subnet**:
   - **AMI**: Amazon Linux 2 (or Ubuntu)
   - **Instance type**: t2.micro
   - **Subnet**: Private subnet (`10.0.2.0/24`)
   - **Auto-assign Public IP**: Disabled
   - **Security Group**: Database SG
2. Could not SSH directly (by design). Instead:
   - First connected to the **public EC2 (bastion/web server)** via SSH.
   - From there, SSH’d into the private EC2 using its private IP.
3. (Optional) Installed a database (MySQL/Postgres) or left as a placeholder server.

---

## 🔹 Why This Matters
- The **private EC2** simulates a database — it’s protected from direct internet access.  
- Only the **web server** can communicate with it (on the DB port).  
- This mirrors real-world secure architectures where databases live in private subnets.

---
