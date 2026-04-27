# Linux - TryHackMe and Solent University Cybersecurity Coursework 

Platform: TryHackMe  
Skill Level: Beginner / Foundation  
Focus Area: Linux Background

## 🎯 Objective
- Understand how Linux is used in cybersecurity
- Learn basic system enumeration techniques
- Identify key system information and user context
- Recognise common Linux environments and distributions

## 🧠 Core Concepts Learned
### Linux in Cybersecurity
- Linux is the most common operating system in:
    - Servers
    - Cloud infrastructure
    - Security tools and labs

💡 Most penetration testing and SOC environments rely on Linux systems 

### Where Linux is Used
- Web servers (hosting websites)
- Cloud platforms (AWS, Azure)
- Embedded systems (IoT, traffic systems)
- Enterprise infrastructure

### Linux Distributions (Flavours)
- Because Linux is open-source, it has many variants (called distributions) 
- All distros share the same core, but differ in tools, interface, and purpose

#### Common Linux Distributions and Their Uses
1. Ubuntu
- Beginner-friendly and widely used
- Common in desktops, servers, and cloud environments
- Ubuntu Server can run on systems with only 512MB of RAM 

💡 Good starting point for learning Linux  

2. Debian
- Stable and reliable
- Often used in servers and enterprise environments

💡 Prioritises stability over latest features  

3. Kali Linux
- Designed for penetration testing and ethical hacking
- Comes pre-installed with security tools 

💡 Used by cybersecurity professionals and students

4. Parrot OS
- Security-focused distribution similar to Kali
- Includes tools for penetration testing, forensics, and privacy

💡 Lighter and more privacy-oriented than Kali

5. CentOS / Rocky Linux
- Enterprise-level server distributions
- Used in business environments and production servers

💡 Focus on long-term stability and performance

### System Enumeration (Core Cybersecurity Skill)
- When you access a Linux system, the first step is **enumeration**  
💡 Gathering information about the system  
- Working in cybersecurity requires understanding the environment you are operating in, including the Linux version and available system resources

#### "Who are you logged in as?" 
    - `whoami` - prints the current username

#### "What system are you on?" 
    - `uname -a` - to get details about the operating system, kernel version, and architecture  
⚠️ `uname` shows basic system information, while `uname -a` provides detailed system and kernel information    

#### "Check disk and storage info" 
    - `df -h` - disk usage in human-readable format  
💡 `-h` means "human-readable" and makes output easier to read (GB instead of bytes)    
💡 It is a good habit to check disk usage before running tools or analyzing logs    

#### "Read a system information file"
    - Linux stores configuration and information files in `/etc` directory
    - This file exists on most Linux systems
    - `cat /etc/os-release` command shows Linux distribution details that are more detailed  than `uname`

## Key Directories in Linux
- `~` (Home Directory) → shortcut that represents the current user’s home directory
- `/` → Root directory (top level)
- `/home` → User directories
- `/etc` → Configuration files
- `/var` → Logs and variable data
- `/tmp` → Temporary files  
💡 Linux uses a structured hierarchy to organise files  
💡 Many logs and sensitive configuration files are stored in these directories, making them important during security investigations   
💡 Understanding these directories is important for system navigation and investigation 

## 🛠️ Practical Skills Developed


## 🧰 Tools Used
- Solent University Cybersecurity Coursework
- TryHackMe platform
- Linux (terminal environment)

## 🔐 Security Relevance


## 📌 Lessons Learned
Linux is not a single OS — it comes in different distributions (distros)