# Introduction to Cyber Security – TryHackMe and Solent University Cybersecurity Coursework 

Platform: TryHackMe    
Skill Level: Beginner / Foundation  
Focus Area: Offensive Security (Ethical Hacking)

## 🎯 Objective 
Gain a foundational understanding of offensive security, including:
- Differences between offensive and defensive security  
- Common roles and career paths in offensive security  
- Understand how cybersecurity roles connect to real-world environments
- How attackers think and operate in real-world scenarios
- Overview of practical tasks in SOC and ethical hacking  
- Common vulnerabilities and exploitation techniques
- Legal and ethical boundaries of penetration testing
- Overview of attack simulation methodologies

## 🧠 Core Concepts Learned   

## 🔴 Offensive Security  
### Ethical Hacking
- Simulating attacks in a controlled and authorised environment
- Focus on identifying and exploiting vulnerabilities before malicious actors do
- Must follow strict legal frameworks (permission-based testing only)

### Core Offensive Security Terms
- Red Teaming
    - A structured and authorised attack simulation that mimics real-world adversaries to evaluate the effectiveness of an organisation’s defenses.
- Penetration Testing (Pentest)
    - A controlled security assessment where authorised testers identify and attempt to exploit vulnerabilities to assess real-world risk.
- Vulnerability
    - A weakness or misconfiguration in a system, application, or process that could be exploited by an attacker.
- Exploit
    - A method or technique used to take advantage of a vulnerability to gain unauthorised access or perform unintended actions.
- Scope
    - The defined boundaries of an engagement, specifying what systems, applications, and actions are permitted — and what is strictly off-limits.

### Ethical Hacking and Permission
- Although these terms are sometimes used interchangeably, they all operate under one critical principle: **explicit permission**
- Ethical hackers are explicitly allowed to test systems within a defined scope, making this work intentional and safe
- Activities are carefully controlled to avoid damage or disruption
- All actions must align with agreed rules of engagement

⚠️ In real-world scenarios, organisations hire security professionals to simulate attacks against their own systems. The goal is not to cause harm, but to:

- Identify weaknesses before malicious actors do
- Test the effectiveness of existing security controls
- Improve the organisation’s overall security posture

### 🧪 TryHackMe Lab Example - Enumeration
- Assessed a simulated web application `http://www.onlineshop.thm/` to identify exposed or hidden pages

**Actions Performed:**
- Manually tested common endpoints (/sitemap, /mail, /admin, /login, /register) by appending them to the URL
- Identified valid pages based on HTTP responses (200 OK vs 404 Not Found)
- Used **Gobuster** to automate directory and file discovery

**Command Used:**  
`gobuster dir --url http://www.onlineshop.thm/ -w /usr/share/wordlists/dirbuster/directory-list.txt`  

**Key Finding:**  
- Discovered that the /login page was publicly accessible, indicating a potential access control weakness 

**Key Insight:** 
- Hidden or unlinked pages can still be accessed if not properly secured
- Automated tools significantly speed up the discovery of exposed resources

💡 This lab demonstrates how attackers enumerate web applications to uncover sensitive or unintended functionality

### 🔍 Enumeration
- The process of systematically discovering and listing information about a target
- Commonly used to identify hidden pages, services, or endpoints
- Often performed using automated tools like **Gobuster**

### 🧪 TryHackMe Lab Example - Directory Enumeration
- Enumerated a simulated banking web application `http://fakebank.thm/` to identify hidden or unsecured functionality

**Actions Performed:**
- Used command-line tool **Gobuster** to brute-force FakeBank's website to find hidden directories and pages
- Analysed HTTP response codes to identify valid pages (Status: 200)
- Investigated discovered endpoints manually via browser

**Command Used:**  
`gobuster dir -u http://fakebank.thm -w wordlist.txt`

**Key Finding:**  
- Discovered an exposed `/bank-transfer` page that allowed direct money transfers between accounts without authentication

**Key Insight:**
- Sensitive functionality should never be accessible without proper authentication and authorization
- Automated enumeration tools can quickly uncover critical vulnerabilities that are not visible through normal navigation

💡 This lab demonstrates how attackers use directory brute-forcing to uncover hidden application features and identify security misconfigurations

### 🧪 TryHackMe Lab Example – Credential Attack
- Tested authentication security of the web application `http://www.onlineshop.thm/login`  

**Actions Performed:**  
- Attempted login using common credentials (username: admin)
- Manually tested a short password list (123456, password, qwerty)
- Successfully identified valid credentials
- Used Hydra to automate password testing **(dictionary attack)**

**Command Used:**  
`hydra -l admin -P passlist.txt www.onlineshop.thm http-post-form "/login:username=^USER^&password=^PASS^:F=incorrect" -V`

**Key Finding:**  
- Weak password allowed successful login as admin, demonstrating poor authentication security  
  
**Key Insight:**   
- Applications without proper protections are vulnerable to brute-force attacks
- Automated tools can test hundreds or thousands of credentials rapidly

💡 This lab demonstrates how attackers exploit weak credentials to gain unauthorised access to systems

### **Attack Lifecycle** 
- Reconnaissance: Gathering information about the target
- Scanning & Enumeration: Identifying open ports, services, and weaknesses
- Exploitation: Gaining access using vulnerabilities
- Privilege Escalation: Increasing access level on the system
- Post-Exploitation: Maintaining access and extracting data

### **Common Vulnerabilities**
- Weak passwords / poor authentication
- Misconfigured services
- Outdated software
- Web vulnerabilities

## 💼 Career Path – Offensive Security
**Common Roles**  
- Penetration Tester (Pentester)
- Red Team Operator
- Bug Bounty Hunter
- Security Consultant

**Key Skills Required**
- Strong networking knowledge
- Linux proficiency
- Scripting (Python, Bash)
- Deep understanding of vulnerabilities and exploits

**Reality Check**
- Entry-level offensive roles are harder to get than defensive ones
- Most people transition into offensive security after building experience in SOC or IT

## 🛠️ Practical Skills Developed    
- Completed the Introduction to Cyber Security room step by step on TryHackMe  
- Identified exposed endpoints through enumeration techniques
- Reviewed career options and real-world applications    

## 🧰 Tools Used 
- TryHackMe platform 
- Solent University Cybersecurity Coursework 
- Lab virtual machines (sandboxed environments for ethical hacking)    

## 🔐 Security Relevance
- Understanding offensive and defensive security **builds a foundation for real-world cybersecurity roles** 
- Offensive security helps organisations identify weaknesses before attackers do   
- Improves overall system resilience through proactive testing
- Provides insight into real attack techniques used in the wild
- Awareness of SOC and DFIR tasks prepares for real-world security operations  
- Learning career paths helps focus your learning trajectory and skill development  

## 📌 Lessons Learned 
⚠️ Thinking like an attacker improves defensive skills massively  
⚠️ Exploitation is rarely one-step — it’s usually a chain of small weaknesses   
⚠️ Cybersecurity requires a balance between **attacking and defending skills**   
⚠️ Offensive exercises teach how vulnerabilities are exploited, which informs better defense   
⚠️ Legal boundaries are critical — hacking without permission is illegal   
⚠️ Offensive security requires patience, creativity, and persistence   
⚠️ Early career exploration is important to set goals and learning paths    
  