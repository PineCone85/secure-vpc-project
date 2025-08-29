# Step 4: Security Groups & NACLs

---

## 🔹 What I Did
- **Security Groups**
  - Web Server SG:
    - Allow inbound HTTP (80) and HTTPS (443) from anywhere
    - Allow inbound SSH (22) only from my IP
    - Allow outbound traffic to private subnet DB SG
  - Database SG:
    - Allow inbound MySQL/Postgres traffic (port 3306) only from Web Server SG
    - No inbound from the internet
- **NACLs**
  - Public Subnet NACL → allows HTTP/HTTPS in, ephemeral ports out
  - Private Subnet NACL → only allows traffic from public subnet, blocks everything else

---

## 🔹 Why This Matters
- **Security Groups** are like firewalls on each instance.  
- **NACLs** are an extra layer at the subnet level.  
- Together, they enforce the “least privilege” model:  
  - Web server can talk to database.  
  - Internet can only reach web server.  
  - Database is invisible to the internet.

---
