# Operating System Basics – TryHackMe

Platform: TryHackMe  
Date Completed: 23.03.2026  
Skill Level: Beginner / Foundation  
Focus Area: Cybersecurity Fundamentals

## Objective
Gain a foundational understanding of operating systems and cybersecurity, including:

- Core functions of operating systems (process, memory, and file management)
- Differences between Windows and Linux environments
- Use of command-line interfaces (CLI) in both systems
- Basic security principles, including the CIA triad
- User roles and privilege levels (standard user vs administrator/root)
- Introduction to privilege escalation in controlled environments

## Key Concepts
1. Introduction to Operating Systems
- Definition and purpose of an operating system
- Role as an interface between hardware and user applications
- Core functions: process management, memory management, file systems, and device control

2. Windows Basics
- Short history and evolution of Windows from Ms-Dos to Windows 1.0 (1985)
- Understanding the desktop environment, taskbar, and file explorer
- File system navigation and management
- Basic system settings and configuration

3. Linux Fundamentals
- Understanding Linux distributions and terminal-based interaction
- File system hierarchy (/, /home, /etc, /var, /bin, /tmp)
- Permissions model (read, write, execute)

4. Command Line Interface (CLI)  

**Windows CLI (Command Prompt / PowerShell)**  

| Category                     | Command      | Description                  |
|------------------------------|--------------|------------------------------|
| Navigation & File Inspection | cd           | Change directory             |
| Navigation & File Inspection | dir          | List files and directories   |
| Navigation & File Inspection | dir /s       | List all files recursively   |
| Navigation & File Inspection | type         | Display file contents        |
| System Identification        | whoami       | Display current user         |
| System Identification        | hostname     | Show system name             |
| File Operations              | copy         | Copy files                   |
| File Operations              | move         | Move/rename files            |
| File Operations              | del          | Delete files                 |
| System & Network Information | ipconfig     | View network configuration   |
| System & Network Information | tasklist     | View running processes       |
| System & Network Information | systeminfo   | Detailed system information  |

**Linux CLI** 
  
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

5. Operating System Security  
- **CIA Triad**:
    - Confidentiality: Protecting sensitive information from unauthorized access
    - Integrity: Ensuring data is accurate and unmodified
    - Availability: Ensing systems and data are accessible when needed
- User roles and privilege levels:
    - Differences between standard users and administrator/root accounts
    - Importance of least privilege in reducing attack surface
- Vulnerabilities & Misconfigurations:
    - Weak passwords and poor authentication practices
    - Incorrect file permissions leading to unauthorized access
    - Misconfigured services and exposed system files
    - Risks posed by malicious or untrusted programs
- Privilege Escalation (Practical Exposure):
    - Basic understanding of how attackers exploit misconfigurations to gain elevated privileges
    - Hands-on experience in controlled environments (e.g., AttackBox labs)

## Actions Taken
- Explored Windows environment, including file management and system settings
- Practiced Linux commands in a terminal environment
- Executed common CLI commands for navigation, file manipulation, and system monitoring
- Used a virtualized lab environment (AttackBox) to simulate real-world scenarios
- Performed privilege escalation exercises to gain root/administrator access in a controlled environment
- Applied CIA triad concepts to understand system security risks

## Tools Used
- Windows Operating System
- Linux (terminal-based environment)
- Command Prompt and PowerShell
- Bash shell
- AttackBox (cloud-based virtual machine for penetration testing labs)

## Security Relevance
This project supports the development of foundational cybersecurity skills by building a better understanding of how operating systems function and how they can be secured.

- Understanding how operating systems function is critical for identifying vulnerabilities
- CLI proficiency enables efficient system interaction and incident response
- Knowledge of permissions and user roles is key to preventing unauthorized access
- Practical exposure to privilege escalation highlights common attack vectors
- Applying the CIA triad provides a framework for evaluating and improving system security

These skills provide a starting point for further development towards roles such as SOC Analyst, Security Engineer, or Penetration Tester.