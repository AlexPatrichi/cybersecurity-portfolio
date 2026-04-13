# Operating System Fundamentals - TryHackMe and Solent University Cybersecurity Coursework 

Platform: TryHackMe  
Skill Level: Beginner / Foundation  
Focus Area: Linux Basics

## 🎯 Objective
- Understand what Linux is and why it is widely used
- Learn how to interact with Linux through the terminal
- Explore basic navigation, file handling, and system information commands
- Recognise why Linux skills are important in cybersecurity

## 🧠 Core Concepts Learned

## Linux Fundamentals
### Short History
- Linux is an open-source operating system based on Unix principles
- First released in 1991 by Linus Torvalds
- Widely used in servers, cybersecurity, and cloud environments

💡 Most cybersecurity tools and servers run on Linux   

### The Terminal
- A text-based interface used to interact with the system
- Users type commands instead of using graphical elements (GUI)
- Provides:
    - More control
    - Faster interaction
    - Access to advanced system functions

💡 Many security tools and servers operate only through the terminal  

### Core Linux Commands
#### 📂 Navigation
- `pwd` (Print Working Directory) →  shows the current directory

- `ls` (List) → lists files and directories  
⚠️ `ls -l` command will print more details  
⚠️ `ls -al` command will print the hidden files in the directory   
⚠️ These files starts with a . (dot) and are hidden by default  

- `cd` (Change Directory) → changes the current directory  
⚠️ To go back one level use `cd ..` command  

#### 📄 File Viewing
- `cat` (Concatenate) → displays the contents of a file  
⚠️ Originally meant to join files together  
⚠️ But in practice, you mainly use it to read files and display content quickly  

#### 🔍 File Search
- `find` (Find) → searches for files and directories  
⚠️ More powerful than it looks  
⚠️ Can search by: name, type, size, permissions  

#### ⚙️ System Information
- `whoami` → shows the current user  
- `uname` (Unix Name) → displays basic system information

💡 These commands are essential for navigating and interacting with the Linux file system  

### Key Directories in Linux
- `~` (Home Directory) → shortcut that represents the current user’s home directory
- `/` → Root directory (top level)
- `/home` → User directories
- `/etc` → Configuration files
- `/var` → Logs and variable data
- `/tmp` → Temporary files

💡 Many logs and sensitive configuration files are stored in these directories, making them important during security investigations  
💡 Understanding these directories is important for system navigation and investigation  

### 🧪 Gathering System Information on Lynux (Cybersecurity Context)
- Working in cybersecurity requires understanding the environment you are operating in, including the Linux version and available system resources
- "Who are you logged in as?" 
    - `whoami` - prints the current username

- "What system are you on?" 
    - `uname -a` - to get details about the operating system, kernel version, and architecture  
⚠️ `uname` shows basic system information, while `uname -a` provides detailed system and kernel information    

- "Check disk and storage info" 
    - `df -h` - disk usage in human-readable format  
💡 `-h` means "human-readable" and makes output easier to read (GB instead of bytes)    
💡 It is a good habit to check disk usage before running tools or analyzing logs    

- "Read a system information file"
    - Linux stores configuration and information files in `/etc` directory
    - This file exists on most Linux systems
    - `cat /etc/os-release` command shows Linux distribution details that are more detailed  than `uname`

## Command Line Interface (CLI)  
### Linux CLI Concepts
- Commands are executed by a shell (Bash)
- The shell interprets commands and interacts with the OS
- Commands can be combined and automated using scripts

💡 CLI is essential for system administration and cybersecurity tasks  

### Linux CLI Commands
| Category                     | Command | Description                          |
|------------------------------|---------|--------------------------------------|
| Navigation & File Inspection | cd      | Change directory                     |
| Navigation & File Inspection | ls      | List files and directories           |
| Navigation & File Inspection | pwd     | Show current directory               |
| Navigation & File Inspection | cat     | Display file contents                |
| Navigation & File Inspection | find    | Search for files and directories     |
| System Investigation         | whoami  | Display current user                 |
| System Investigation         | uname   | System/kernel information            |
| System Investigation         | df -h   | Disk usage (human-readable)          |
| File Operations              | cp      | Copy files                           |
| File Operations              | mv      | Move/rename files                    |
| File Operations              | rm      | Remove files                         |
| File Operations              | touch   | Create files                         |


## 🛠️ Practical Skills Developed
- Navigating a Linux system using the terminal
- Understanding basic file system structure
- Using commands to gather system information
- Performing basic file operations

## 🧰 Tools Used
- Solent University Cybersecurity Coursework
- TryHackMe platform
- Linux (terminal environment)
- Bash shell

## 🔐 Security Relevance
- Linux is widely used in servers and cybersecurity environments
- Understanding Linux helps:
    - Navigate target systems
    - Analyse logs and configurations
    - Use security tools effectively

💡 Many penetration testing and SOC tools are Linux-based

## 📌 Lessons Learned
⚠️ Linux is widely used in cybersecurity, making CLI skills essential  
⚠️ Understanding the file system is key for navigation and investigation  
⚠️ Simple commands can reveal important system information  