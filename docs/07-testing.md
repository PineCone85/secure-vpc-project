# Step 7: Testing & Validation

---

## 🔹 What I Tested
1. **Public EC2 accessibility**
   - Opened the public IP in my browser → saw the test web page.  
   - Confirmed HTTP works, but SSH only from my IP.
2. **Private EC2 isolation**
   - Tried accessing the private EC2 directly from my laptop → failed (expected).  
   - Successfully SSH’d into it via the public EC2 (bastion).  
3. **Private EC2 outbound internet**
   - From the private EC2, ran:
     ```bash
     ping google.com
     sudo yum update -y
     ```
   - Confirmed outbound internet access works via the **NAT Gateway**.
4. **Traffic restrictions**
   - Verified that the private EC2 is not accessible on database ports from the internet.  
   - Only the web server SG can talk to the database SG.

---

## 🔹 Why This Matters
- Confirms the **security boundaries are working as designed**:  
  - Public subnet = exposed but controlled.  
  - Private subnet = hidden, only accessible internally.  
  - Outbound internet = controlled through NAT.  
- This final step shows the network is both **functional and secure**.

---