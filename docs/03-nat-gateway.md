# Step 3: NAT Gateway

---

## 🔹 What I Did
1. Allocated an **Elastic IP**.  
2. Created a **NAT Gateway** in the **public subnet** using that Elastic IP.  
3. Updated the **private subnet’s route table**:  
   - Added a route: `0.0.0.0/0` → NAT Gateway  

---

## 🔹 Why This Matters
- The private subnet should **not** be directly reachable from the internet.  
- With a NAT Gateway:
  - Instances in the private subnet can **initiate outbound connections** (e.g., OS updates).  
  - But nobody from outside can directly connect in.  

---
