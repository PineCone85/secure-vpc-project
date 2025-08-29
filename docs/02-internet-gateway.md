# Step 2: Internet Gateway

---

## 🔹 What I Did
1. Created an **Internet Gateway (IGW)** in the VPC console.  
2. Attached the IGW to the `secure-vpc`.  
3. Updated the **public subnet’s route table**:  
   - Added a route: `0.0.0.0/0` → Internet Gateway  

---

## 🔹 Why This Matters
- Without an Internet Gateway, nothing inside the VPC can reach the internet.  
- Attaching it only to the **public subnet** ensures only web-facing resources are exposed.  

---