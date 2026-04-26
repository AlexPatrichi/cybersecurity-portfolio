# Web Fundamentals – TryHackMe and Solent University Cybersecurity Coursework 

Platform: TryHackMe   
Level: Beginner / Foundation  
Focus Area: Web Security Basics 

## 🎯 Objective 
- Understand common web vulnerabilities  
- Learn how improper handling of user input leads to security risks  

## 🧠 Core Concepts Learned 

## Sensitive Data Exposure
- Occurs when a website fails to properly protect sensitive information

### Examples:
- Credentials exposed in HTML or JavaScript  
- Hidden links to private resources  
- Unencrypted data transmission  

⚠️ Sensitive data should never be exposed in frontend code  

## HTML Injection
- Is happening when an attacker inserts malicious HTML into a webpage  

### Cause:
- Lack of input validation and filtering  

### Impact:
- Website displays attacker-controlled content  
- Can lead to phishing or further attacks  

## Input Sanitisation 
- The process of validating and cleaning user input before processing it  

### Purpose:
- Prevent malicious input from being executed  
- Protect both frontend and backend functionality  

⚠️ Never trust user input — always validate and sanitise before processing

## Cross-Site Scripting (XSS)
- A type of attack where malicious scripts are injected into trusted websites  

### Impact:
- Steal user session data (cookies)  
- Perform actions on behalf of the user  
- Redirect users to malicious websites  

⚠️ XSS often occurs when input is not properly sanitised or escaped

## 🛠️ Practical Skills Developed
- Identifying insecure input handling  
- Understanding how basic web attacks are performed  

## 🧰 Tools Used 
- Solent University Cybersecurity Coursework  
- TryHackMe platform  

## 🔐 Security Relevance
- These vulnerabilities are commonly exploited in real-world attacks  
- Understanding them is essential for roles like SOC Analyst or Security Analyst  

## 📌 Lessons Learned  
⚠️ Most web vulnerabilities arise from improper handling of user input   
⚠️ Failing to validate or sanitise input can lead to serious attacks    
⚠️ Secure coding practices are essential to protect both users and systems  