# Security Fundamentals - TryHackMe and Solent University Cybersecurity Coursework 

Platform: TryHackMe  
Skill Level: Beginner / Foundation  
Focus Area: Authentication & Authorization

## 🎯 Objective
- Understand the difference between authentication and authorization  
- Learn how identity is verified and access is controlled in systems  
- Explore common authentication methods and access control mechanisms  

## 🧠 Core Concepts Learned
## 🔑 Authentication vs Authorization

👉 Authentication = **Who are you?**  
👉 Authorization = **What are you allowed to do?**

💡 These two concepts work together to secure systems and control access.

###  Authentication
- The process of verifying a user’s identity  
- Ensures that a user is who they claim to be  

**Common authentication methods:**
- **Something you know** → Password, PIN  
- **Something you have** → Phone, security token  
- **Something you are** → Biometrics (fingerprint, face recognition)  

💡 Multi-Factor Authentication (MFA) combines multiple methods for stronger security 

###  Authorization
- The process of determining what an authenticated user is allowed to access  
- Happens **after authentication**  

**Examples:**
- A user can log in (authenticated) but cannot access admin settings  
- An admin has full access to system configurations  

### Access Control Concepts
- **Least Privilege** → Users only get the access they need  
- **Role-Based Access Control (RBAC)** → Permissions based on roles (user, admin)  

💡 Proper authorization prevents misuse of systems even by legitimate users  

## 🛠️ Practical Skills Developed
- Distinguishing between authentication and authorization  
- Identifying authentication methods used in real systems  
- Understanding how access control is applied in practice 

## 🧰 Tools Used
- TryHackMe platform  
- Solent University Cybersecurity Coursework  

## 🔐 Security Relevance
- Weak authentication can lead to unauthorised access (e.g., weak passwords)  
- Poor authorization can allow privilege escalation  
- MFA significantly reduces the risk of account compromise  
- Access control mechanisms protect sensitive data and system functionality 
- A user logging into a system (authentication) may still be restricted from accessing admin features (authorization)

## 📌 Lessons Learned
⚠️ Authentication verifies identity, while authorization controls access  
⚠️ Both are required to properly secure systems  
⚠️ Strong authentication methods reduce the risk of account compromise  
⚠️ Proper authorization prevents users from accessing sensitive resources  