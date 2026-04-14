# Operating System Fundamentals - TryHackMe and Solent University Cybersecurity Coursework 

Platform: TryHackMe  
Skill Level: Beginner / Foundation  
Focus Area: Operating System Security

## 🎯 Objective
- Understand core principles of operating system security  
- Learn the CIA Triad and its role in protecting systems  
- Identify common security weaknesses in operating systems  
- Explore basic attack concepts and privilege escalation  

## 🧠 Core Concepts Learned
## Operating System Security
- Devices such as phones and computers store large amounts of sensitive data, making operating system security essential
- The operating system acts as the first layer of defence against unauthorized access and attacks

💡 If the operating system is compromised, all other security measures become ineffective

## CIA Triad
- A foundational security model used to guide information security 
### Confidentiality 
- Ensures that data is only accessible to authorised users
### Integrity 
- Ensures that data cannot be altered or tampered with
### Availability 
- Ensures systems and data are accessible when needed

## Common Security Weaknesses
### Weak Authentication and Passwords
- Authentication is the act of verifying a users identity when accessing a system
- Common methods include:
    - Something you know → password or PIN
    - Something you are → biometrics
    - Something you have → phone number or sms

- Weak passwords are a major vulnerability:
    - Users tend to use easy-to-guess passwords
    - Reusing passwords across multiple systems 
    - Using personal information 

### Weak File Permissions
- Systems should follow the principle of **least privilege**
- Incorrect permissions can expose sensitive data
- In a work environment, users should only have access to what they need
- On a personal level, user should not share files publicly

### Malicious Programs
- This programs (such as Trojan Horses) can give attackers access to a system

- Attackers may:
    - Read or modify files
    - Disrupt system availability
    - Deploy ransomware (encrypt the files and demand payment)

## 🧪 Practical Example: Weak Authentication Attack
- An attacker attempts to gain access to a remote system
- They identify a valid username and attempt to guess the password
- Once access is gained, they try to escalate privileges to an administrator/root account

- Commands Used:
- `ssh` → remote login
- `whoami` → confirm user identity
- `ls` → list files
- `cat` → read file contents
- `history` → view command history

💡 This demonstrates how weak passwords can lead to system compromise
💡 Privilege escalation allows attackers to gain full control over a system

## 🛠️ Practical Skills Developed
- Understanding core OS security principles
- Identifying common vulnerabilities such as weak passwords and permissions
- Recognising basic attack techniques
- Using simple commands to investigate systems

## 🧰 Tools Used
- TryHackMe platform
- Solent University Cybersecurity Coursework
- AttackBox (cloud-based virtual machine for hands-on labs)

## 🔐 Security Relevance
- Operating systems are primary targets for attackers
- Weak authentication and misconfigurations are common entry points
- Understanding OS security helps:
    - Prevent unauthorized access
    - Detect suspicious behaviour
    - Protect sensitive data

💡 Many successful attacks rely on simple weaknesses rather than complex exploits

## 📌 Lessons Learned
⚠️ Weak passwords are one of the biggest security risks
⚠️ Proper permissions are essential to protect sensitive data
⚠️ Understanding system behaviour helps detect attacks early
⚠️ Basic commands can be used for both administration and exploitation