# Operating System Fundamentals - TryHackMe and Solent University Cybersecurity Coursework 

Platform: TryHackMe  
Skill Level: Beginner / Foundation  
Focus Area: Linux Basics

## 🎯 Objective
- Understand what Linux is
- Learn how users interact with Linux systems
- Recognise basic file system structure
- Perform simple navigation using the terminal

## 🧠 Core Concepts Learned

## Linux Fundamentals
- Linux is an open-source operating system based on Unix principles
- First released in 1991 by Linus Torvalds
- Widely used in servers, cybersecurity, and cloud environments

💡Linux powers a large portion of the internet and modern infrastructure  
💡 Most cybersecurity tools and servers run on Linux   

## The Terminal
- A text-based interface used to interact with the system
- Users type commands instead of using graphical elements (GUI)
- Provides:
    - More control
    - Faster interaction
    - Access to advanced system functions

💡 Many systems (especially servers) are managed only through the terminal

## Core Linux Commands
### 📂 Moving Around the System
- `pwd` (Print Working Directory) →  shows the current directory
- `ls` (List) → lists files and directories 
- `cd` (Change Directory) → changes the current directory 

⚠️ To go back one level use `cd ..` command   
💡 These commands allow you to move through the system  

### 📄 Viewing Files
- `cat` (Concatenate) → displays the contents of a file  

⚠️ Originally meant to join files together   
⚠️ But in practice, you mainly use it to read files and display content quickly   

### 🔍 File Search
- `find` (Find) → searches for files and directories  

⚠️ More powerful than it looks  
⚠️ Can search by: name, type, size, permissions  

### ⚙️ System Information
- `whoami` → shows the current user  
- `uname` (Unix Name) → displays basic system information

💡 These commands are essential for navigating and interacting with the Linux file system  

📂 Important Directories (Security Context)
- `/home` → user files
- `/etc` → configuration files
- `/var` → logs (VERY important)
- `/tmp` → temporary files (often abused)  

💡 Attackers and analysts both check these locations first

## Command Line Interface (CLI)  
- Commands are executed by a shell (Bash)
- The shell interprets commands and interacts with the OS

💡 The CLI is a core way to interact with Linux systems  

## 🛠️ Practical Skills Developed
- Navigating directories using basic commands
- Understanding Linux structure
- Interacting with the system through the terminal

## 🧰 Tools Used
- Solent University Cybersecurity Coursework
- TryHackMe platform
- Linux (terminal environment)
- Bash shell

## 🔐 Security Relevance
- Linux is widely used in servers and cybersecurity environments
- Basic knowledge helps:
    - Understand how systems are structured
    - Prepare for advanced security tools

💡 Many penetration testing and SOC tools are Linux-based

## 📌 Lessons Learned
⚠️ Linux is a fundamental skill in IT and cybersecurity  
⚠️ The terminal is the primary way to control Linux systems  
⚠️ Understanding structure comes before advanced usage  