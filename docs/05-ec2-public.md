# Step 5: Public EC2 Web Server

---

## 🔹 What I Did
1. Launched a new **EC2 instance** in the **public subnet**:
   - **AMI**: Amazon Linux 2 (or Ubuntu)
   - **Instance type**: t2.micro (free tier)
   - **Subnet**: Public subnet (`10.0.1.0/24`)
   - **Auto-assign Public IP**: Enabled
   - **Security Group**: Web Server SG
2. Connected to the instance via SSH from my local machine.
3. Installed a simple web server:
   ```bash
   sudo yum update -y
   sudo yum install -y httpd
   sudo systemctl start httpd
   echo "Hello from Secure VPC Web Server" | sudo tee /var/www/html/index.html
   ```
4. Verified by opening the public IP in my browser.

## 🔹 Why This Matters
- The public EC2 acts as the “front door” of the application.
- By restricting inbound rules, only HTTP/HTTPS traffic is exposed.
- SSH access is limited to my IP, ensuring admin access is secure.