# Introduction to Cyber Security – TryHackMe and Solent University Cybersecurity Coursework 

Platform: TryHackMe    
Skill Level: Beginner / Foundation  
Focus Area: Defensive Security (Blue Team)

## 🎯 Objective 
Develop a foundational understanding of defensive security, including:
- How organisations detect and respond to threats
- The role of SOC teams and monitoring systems
- Incident response and investigation processes
- How defensive tools protect systems in real time

## 🧠 Core Concepts Learned   

## 🔵 Defensive Security 
- Defensive security focuses on protecting systems by preventing, detecting, and responding to threats
- The goal is to minimise risk and ensure systems remain secure and operational

### Core Defensive Security Terms
- Blue Team
    - A group of cybersecurity professionals responsible for defending systems and responding to threats
- Client Infrastructure
    - The systems, networks, servers, and applications that belong to an organisation and require protection
- Visibility
    - The ability to monitor and observe activity across systems to detect potential threats
- Threat
    - A potential source of harm, such as attackers or malware
- Prevention
    - Measures used to stop attacks before they occur (firewalls, patching, antivirus)
- Detection
    - Identifying suspicious or malicious activity through monitoring and analysis
- Mitigation
    - Actions taken to reduce or stop the impact of an attack
- Risk
    - The likelihood and potential impact of a threat affecting an organisation

### Understanding The Environment
- Defenders focus on protecting their organisation’s infrastructure (includes endpoints, servers, applications, and networks)
- Effective defence starts with understanding what assets exist and gaining visibility over them  

💡 Without visibility, threats cannot be detected  

### Core Defensive Security Functions
- Prevention
    - Implementing security controls such as firewalls, antivirus software, and regular patching
- Detection
    - Monitoring logs, alerts, and system activity for suspicious behaviour
- Mitigation
    - Limiting damage during an incident (isolating affected systems, blocking traffic, or disabling compromised accounts)
- Analysis
    - Investigating how an attack happened and what was affected
- Response & Improvement
    - Recovering systems and strengthening defenses to prevent future incidents 

### Defending the Environment
- The defender’s role is to understand what assets exist, how they function, and how they could be misused, then apply controls to reduce risk.
- Attackers rarely target a single system. They compromise one asset and pivot across the environment, escalating access until they reach their objective.

### Key Defender Principles
- Threat Anticipation
    - Ask “What if?” and consider how systems could be attacked
    - Imagine realistic paths an attacker may take to achieve their goal
- Attack Awareness
    - Understand common attack patterns and frameworks
- Risk Prioritisation
    - Focus on protecting high-value assets first
- Continuous Adaptation
    - Defense is not a one-time setup
    - Security must evolve as threats and techniques change

### Areas Of Defensive Security
### **Security Operations Center (SOC)**
- A central team responsible for monitoring and responding to threats
- Operates 24/7 in many organisations
- Uses tools like SIEM to analyse logs and detect suspicious activity and anomalies
- Leverages **threat intelligence** to recognise attack patterns and anticipate emerging threats

💡 The SOC acts as the organisation’s defensive layer, focusing on early detection and rapid response to minimise impact

#### **Threat Intelligence**
- The process of collecting, processing, and analysing information about potential or active threats
- Helps organisations understand attacker behaviour, motives, and likely targets
- The purpose would be to achieve a threat-informed defence
- Threat intelligence relies on data that is collected, processed, and analysed to produce actionable insights
- Data is gathered from:
    - Internal sources (logs, system activity)
    - External sources (forums, threat feeds)
- Enables identification of attacker Tactics, Techniques, and Procedures (TTPs)
- Supports proactive defence by predicting and mitigating potential attacks

💡 Threat intelligence helps organisations move from reactive security to a proactive, intelligence-driven defence strategy

---

### **Incident Response (IR)**
- Identifying, analysing, and responding to security incidents 
- Incidents can range from critical breaches to less severe issues such as misconfigurations, intrusion attempts, or policy violations

#### **Incident Response Lifecycle**
- The four major phases of the incident response process are:

1. Preparation
- Requires trained teams, tools, and procedures
- Implement preventative measures to reduce the likelihood of incidents

2. Detection and Analysis
- Monitor systems to detect suspicious activity
- Analyse incidents to determine scope, impact, and severity

3. Containment, Eradication, and Recovery
- Containment: Limit the spread of the incident
- Eradication: Remove the root cause (malware, vulnerability)
- Recovery: Restore systems to normal operation

4. Post-Incident Activity
- Document the incident and actions taken
- Identify lessons learned and share to prevent similar future incidents

💡 Incident Response ensures organisations can detect, contain, and recover from attacks quickly, minimising damage and strengthening future security

--- 

### **Digital Forensics**
- Digital forensics is the application of scientific methods to investigate and analyse digital evidence after a security incident
- In defensive security, digital forensics focuses on:
    - Investigating security incidents
    - Identifying attacker activity and methods
    - Collecting and preserving evidence for analysis

#### Key Areas of Analysis
1. Disk Forensics
- Analyses a digital forensic image (low-level copy) of storage devices
- Reveals installed programs, created files, deleted data, and hidden artefacts
2. Memory Forensics
- Examines system memory (RAM) 
- Useful if the attacker runs their malicious program in memory without saving it to the disk
3. System Logs
- Records of system activity (logins, processes, errors)
- Helps reconstruct events and identify suspicious behaviour
4. Network Logs
- Captures network traffic and communication between systems
- Helps detect intrusions, data exfiltration, and attacker activity

---

### **Malware**
- Malware refers to malicious software (programs and instructions) designed to disrupt, damage, or gain unauthorised access to systems

#### **Malware Types**
1. Virus
- Malicious code that attaches itself to legitimate programs
- Designed to spread between systems and can alter, overwrite, or delete files
- Impact ranges from system slowdown to complete failure
2. Trojan Horse
- Disguised as legitimate software but contains hidden malicious functionality
- Often used to gain unauthorised access or control over a system
3. Ransomware
- Encrypts a victim’s files, making them inaccessible
- Attackers demand payment (ransom) in exchange for the decryption key

### **Malware Analysis**
The process of studying malware to understand its behaviour, purpose, and impact.

1. Static Analysis
- Examines malware without running it
- Involves analysing code, structure, and signatures
- Often requires knowledge of low-level programming  
2. Dynamic Analysis
- Runs malware in a controlled environment (sandbox)
- Observes behaviour such as file changes, network activity, and system impact

💡 Malware analysis helps security teams understand threats, improve detection, and develop effective mitigation strategies

---

### Defensive Workflow Connection
- Threat Intelligence helps anticipate threats
- SOC detects suspicious activity in real time
- Incident Response contains and mitigates attacks
- Digital Forensics investigates and provides evidence

💡 Together, these functions form a complete defensive security lifecycle within an organisation

---

### 🧪 TryHackMe Lab Example – SOC Alert Investigation
- Analysed security alerts as a SOC analyst in a simulated banking environment using a SIEM dashboard to monitor system and network activity.

**Actions Performed:** 
- Investigated multiple alerts flagged by the SIEM system (not all alerts are malicious)
- Analysed login activity, including repeated failed login attempts
- Reviewed connections from unknown IP addresses
- Differentiated between normal behaviour and potential security threats

**Key Finding:**  
- Not all alerts indicate malicious activity — some are false positives or normal user behaviour
- Suspicious patterns (repeated failed logins, unknown IP access) require further investigation before classification

**Key Insight:** 
- SOC analysts must apply critical thinking to determine whether alerts are genuine threats
- SIEM tools assist with detection, but human analysis is essential for accurate decision-making

💡 This lab demonstrates how security analysts investigate alerts, identify potential threats, and distinguish between benign and malicious activity

## 💼 Career Path – Defensive Security
**Common Roles**
- SOC Analyst (Level 1 / Junior)
- Incident Responder
- Threat Intelligence Analyst
- Security Analyst

**Key Skills Required**
- Networking fundamentals (very important)
- Log analysis and pattern recognition
- Understanding of attacks and how they appear in logs
- Basic scripting (Python, PowerShell is a plus)

**Reality Check**
- Defensive roles are the most common entry point into cybersecurity
- SOC Analyst is the fastest realistic route into the industry 

## 🛠️ Practical Skills Developed
- Gained exposure to SOC workflows and monitoring concepts  
- Understood the role of SIEM in detecting and analysing events  
- Recognised basic patterns of suspicious activity in simulated scenarios  
- Reviewed career options and real-world applications  

## 🧰 Tools Used 
- TryHackMe platform 
- Solent University Cybersecurity Coursework 
- Lab virtual machines (sandboxed environments)    

## 🔐 Security Relevance
- Defensive security is responsible for real-time protection of organisations
- Detects and stops attacks before they cause damage
- Critical for maintaining business continuity and data protection

## 📌 Lessons Learned 
⚠️ Defensive roles (SOC, malware analysis, threat intel) require strong monitoring and analytical skills    
⚠️ Most real-world work is monitoring, analysing, and responding — not hacking    
⚠️ Small anomalies can indicate major security incidents     
⚠️ Speed and accuracy are critical in incident response   
⚠️ Strong fundamentals (networking, logs, systems) matter more than flashy tools    
⚠️ Defensive and offensive skills complement each other    
  
