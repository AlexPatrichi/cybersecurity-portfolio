# Operating System Fundamentals  - TryHackMe and Solent University Cybersecurity Coursework 

Platform: TryHackMe  
Skill Level: Beginner / Foundation  
Focus Area: Windows Basics

## 🎯 Objective
- Understand the structure and purpose of the Windows operating system
- Learn how users interact with Windows through GUI and CLI
- Explore built-in tools and system management features
- Recognise core Windows security mechanisms

## 🧠 Core Concepts Learned

## 🖥️ Windows Fundamentals → Basic interaction with the system
### Short History
- Early computers ran **MS-DOS (Microsoft Disk Operating System)** using a command-line interface
- Windows 1.0 (1985) introduced a graphical interface with windows, menus, and mouse interaction built on top of the DOS system 
- Over time, Windows evolved into a complete operating system with advanced features and security mechanisms

### Logging in and Authentication
- Before accessing the system, users must verify their identity
- This determines what actions they are allowed to perform
#### User Account Types:
- **Guest:** Temporary access, with minimal permissions and no ability to change system settings
- **Standard:** An account for everyday tasks, such as running applications and modifying personal settings
- **Administrator:** This account has full control over the system configuration and user management

💡 Account types enforce access control and system security

### The Windows Desktop
- Main interface used to interact with the system:
    - **Desktop:** The main workspace for files, folders, and shortcuts 
    - **Taskbar:** Control menu that provides access to applications, system tools, settings, and notifications

💡 These two features help users navigate, launch programs, and manage open applications efficiently
💡 Desktop icons are shortcuts to frequently used applications, not the actual programs

### Built-in Tools and Applications
- Windows includes essential tools by default:
    - Notepad
    - File Explorer
    - Paint
    - Calculator

💡 These tools are the foundation of every Windows system and provide essential functionality without requiring additional software

### File Exploration and Management
- - Every operating system stores data within a file system 
- Windows uses a hierarchical file system:
    - Folders can contain files and subfolders
- Users can: 
    - Navigate
    - Create 
    - Modify 
    - Organise data 

💡 This structure keeps data organised and easier to manage as systems grow

## ⚙️ System Management → Controlling and maintaining the system

### System Configuration and Updates
- Windows includes a modern **Settings application** to configure:
    - Devices
    - Security
    - System preferences
- Alternatively, **the Control Panel** provides access to older configuration tools required for specific administrative tasks
- Windows Update: 
    - Installs security patches, performance improvements, and bug fixes
    - Helps maintain system stability and security

💡 Keeping systems updated is critical for reducing vulnerabilities

### Installing and Managing Applications
- Applications can be installed via:
    - Microsoft Store (trusted source)
    - Official vendor websites
- Applications can be removed using:
    - Control Panel
    - Settings (Apps & Features)
    - Built-in uninstallers

💡 Installing software from trusted sources reduces security risks
💡 Knowing how to install, update and remove applications is a core skill for everyday use

### Task Manager 
- Built-in tool for monitoring system activity in real-time protection
#### Key Tabs:
- **Processes:** Running applications, background processes and resource usage
- **Performance:** CPU, memory, and network statistics
- **Users:** Logged-in users and their resource usage
- **Details:** Advanced process information including PIDs
- **Services:** Background services and their statuses

💡 Task Manager helps identify suspicious processes and abnormal system behaviour

## 🔐 Security & Analysis
### Native Windows Security
- Built-in security tools designed to protect the system against malware, insecure applications, and unauthorized network access
- They are enabled by default and allow the monitoring and control of the security system
### Windows Security Dashboard:
- The central dashboard for managing Windows built-in protection measures
- **Virus & Threat Protection:**
    - Helps detect and remove malicious software using real time protection and scans
- **Firewall & Network Protection:** 
    - Controls incoming and outgoing network traffic
- **App & Browser Control:** 
    - Blocks unsafe applications and files
- **Device Security:** 
    - Provides hardware based protection that helps secure the system

💡 These features form the first layer of defence against threats

## Command Line Interface (CLI)  
- The Command-Line Interface (CLI) allows users to interact directly with the operating system by typing commands
- Commands are interpreted by a shell (such as Command Prompt or PowerShell) and then executed by the operating system
- Many commands interact with the file system, processes, or network configuration
- CLI provides more control, precision, and efficiency compared to GUI-based interaction

### Shell Examples
- Command Prompt (cmd.exe): Basic command execution  
- PowerShell: Advanced scripting and system automation  

💡 PowerShell is more powerful and commonly used in both system administration and cyber operations

### Windows CLI (Command Prompt / PowerShell)
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

### Why CLI Matters in Cybersecurity
- Allows quick system investigation without relying on graphical tools  
- Enables automation through scripts  
- Commonly used in remote access (servers without GUI)  
- Provides direct visibility into system processes, users, and network configuration  

💡 CLI tools are widely used in system administration and incident response to investigate systems and identify suspicious activity  
💡 Many security tools and attack techniques rely heavily on command-line interaction

## 🛠️ Practical Skills Developed
- Navigating and managing the Windows environment
- Monitoring system activity using Task Manager
- Performing file and system operations
- Using CLI commands for troubleshooting and investigation

## 🧰 Tools Used
- Solent University Cybersecurity Coursework
- TryHackMe platform
- Windows Operating System
- Command Prompt and PowerShell

## 🔐 Security Relevance
- Windows is one of the most widely used operating systems, making it a key target for attackers
- Understanding Windows helps:
    - Detect suspicious processes
    - Identify unauthorized access
    - Investigate abnormal system behaviour
- Built-in tools provide essential visibility into system activity

💡 Many attacks rely on misconfiguration or lack of user awareness

## 📌 Lessons Learned
⚠️ Windows provides both usability and security, but requires proper configuration   
⚠️ Keeping the OS and applications up-to-date is an important part of maintaining a secure and stable system   
⚠️ Built-in tools are essential for monitoring and managing system activity   
⚠️ Understanding normal system behaviour is key to identifying potential threats  