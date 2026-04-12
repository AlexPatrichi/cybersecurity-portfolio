# Computer Fundamentals - TryHackMe and Solent University Cybersecurity Coursework 

Platform: TryHackMe  
Skill Level: Beginner / Foundation  
Focus Area: Virtualisation Basics 

## 🎯 Objective
- Understand what virtualisation is and why it is used  
- Learn how virtual machines and hypervisors work together  
- Identify different types of virtualisation technologies  
- Recognise the importance of virtualisation in modern IT and cybersecurity  

## 🧠 Core Concepts Learned
- Before virtualisation, organisations needed separate physical servers for each service (website, database, email, applications) 

### Problems with Traditional Setup:
- **High cost** – hardware, electricity, cooling, maintenance and data centre space  
- **Low utilisation** – servers often run below capacity, wasting CPU, memory and storage resources 
- **Slow deployment** – setting up new servers takes precious time  
- **Difficult scaling** – adding resources requires buying new hardware  
    
💡Virtualisation introduced a new idea: 
"What if multiple applications could share the same physical server safely?"

## Virtualisation Components 

### HYPERVISOR 
- Analogy: Building manager
- The core technology behind virtualisation
-  Software that creates and manages virtual machines, allowing each to behave like an independent computer  

#### His role is to:
- Divides a physical machine into multiple virtual machines  
- Splits the CPU, memory and storage between machines
- Keeps virtual machines isolated and safe from each other
- Manages the lifecycle of VMs (Start, Stop, Pause, Clone, Delete)

#### Types and Use Cases: 
- **Type 1: Bare-Metal**
    - Runs directly on hardware
    - Fast, efficient and secure
    - Used in data centres and production environments  

- **Type 2: Hosted**
    - Runs on top of an existing operating system
    - Easy to install and use
    - Common in testing, learning, and labs (VirtualBox)  

### VIRTUAL MACHINES (VM)
- Analogy: Apartments in a building  
- Represent the virtual computers created by the hypervisor

- Even though it is virtual, each VM behaves like a real computer:
  - Has its own virtual CPU, RAM, storage, and network  
  - Can run its own operating system  
  - Is isolated from other virtual machines  

💡 If one VM fails, others continue to run independently  

### CONTAINERS 
- Analogy: Rooms inside the apartments
- Create isolated environments for the applications 
- Share the host operating system instead of running a full OS like virtual machines  

💡 Containers are faster and more efficient than VMs, but provide less isolation 

## 🛠️ Practical Skills Developed
- Understanding how virtualisation reduces cost and improves efficiency  
- Identifying the role of hypervisors in managing virtual machines  
- Recognising differences between bare-metal and hosted hypervisors  
- Understanding the difference between virtual machines and containers

## 🧪 TryHackMe Lab Example (Virtualisation Management)
- Used a virtualisation management platform to monitor and manage virtual machines in a simulated company environment  

### Tasks Performed:
- Identified a failed virtual machine (**Mail-SERVER**) in an error state  
- Restarted the VM using the management interface to restore the company email service  
- Created a new virtual machine (**Marketing-VM**) with allocated resources (CPU, RAM, storage)  
- Analysed physical host usage and identified capacity and performance issues  

### Key Insight:
- Virtual machines can fail and require management actions to restore services  
- Resource allocation and monitoring are critical for performance and availability  
- Host capacity directly impacts the ability to run and scale virtual machines  

## 🧰 Tools Used
- Solent University Cybersecurity Coursework
- TryHackMe platform

## 🔐 Security Relevance
- Virtual machines are widely used in cybersecurity labs 
- Virtualisation allows safe testing and analysis of malware in isolated environments  
- Isolation prevents threats from spreading between systems  
- Misconfigured virtual environments can introduce security risks

## 📌 Lessons Learned
⚠️ Virtualisation allows multiple systems to run on a single physical machine, improving efficiency and reducing costs  
⚠️ Isolation is a key advantage, but proper configuration is essential to maintain security