# Operating System Fundamentals - TryHackMe and Solent University Cybersecurity Coursework 

Platform: TryHackMe  
Skill Level: Beginner / Foundation  
Focus Area: Operating Systems 

## 🎯 Objective
- Understand what an operating system is and why it is essential
- Learn how the OS acts as a bridge between hardware and applications
- Explore core OS functions: process, memory, file system, and device management
- Recognise the OS as a critical layer of system security

## 🧠 Core Concepts Learned

## Operating Systems
- An **Operating System (OS)** is the core software that manages all hardware and software resources on a computer
- It acts as an intermediary between the user, applications, and hardware
- Without an OS, programs would need to directly control hardware, leading to instability and inefficiency

💡 The OS is the foundation that allows all other software to function reliably

## System Privilege Layers
- The OS separates execution into two main environments:
    - Kernel Space (high privilege)
    - User Space (restricted access)
- This separation improves stability and security
- If an application crashes in user space, it does not affect the entire system

### Kernel Space
- Contains the kernel, the core part of the OS that directly manages hardware and system resources  
- Kernel has full access to:
    - CPU
    - Memory
    - Storage
    - Hardware devices

### User Space
- All standard applications in this space are deliberately prevented from accessing hardware directly
- Before any action, they need to make a **system call** and request services from the kernel

💡 This isolation is critical for preventing malware from taking full control of a system

## Main Functions of an Operating System
### 1. Process Management 
- Creates, schedules, prioritizes, and terminates processes
- Decides how much CPU time each process gets

💡 If you have many programs on, the OS rapidly switches the CPU time between them so they all appear to run simultaneously  

### 2. Memory Management
- Allocates RAM to active processes
- Prevents memory conflicts between applications (programs from accessing each other's memory)
- Reclaims memory when apps are closed

💡 When RAM runs low, the OS uses **virtual memory** to keep the system stable - simulates additional memory using disk space

### 3. File System Management
- Organises data on storage devices into files and directories
- Manages:
    - File names and paths
    - Permissions
    - Metadata (size, type, timestamps)

### 4. Device Management
- Controls hardware using device drivers
- Ensures communication between OS and hardware components

💡 Drivers allow the OS to communicate with hardware

### 5. User Management
- Handles multiple user accounts and access control
- Manages permissions for different users and roles

## Operating System Security 
- The OS is the first line of defence in any system
- Before any antivirus, firewall, or other security tools, the OS enforces protection in the background

- Key Security Functions: 
    - Authentication: Verifies user identity (passwords, biometrics)
    - Permissions: Controls which user or app is allowed to read, write or execute
    - Isolation: Separates processes to prevent interference
    - System Protection: Protects critical files and configurations

💡 If the OS is compromised, all higher-level security controls become ineffective  

## Operating System Interfaces 
### Graphical User Interface (GUI)
- Allows users to interact with the system through visual elements like windows, icons, and buttons
- Easy to learn and beginner-friendly, but slow for advanced tasks, consumes more system resources, and is harder to automate

### Command-Line Interface (CLI)
- Lets users interact with the OS by typing text-based commands
- Provides more control and efficiency
- Preferred in cybersecurity and system administration
- Requires knowledge of commands and syntax

💡 GUIs increase the attack surface, while CLIs reduce unnecessary exposure

## Why Multiple Types of Operating Systems Exist
- Different devices and environments require different capabilities:
    - Desktop OS: Can be user-friendly and support multitasking (Windows OS)
    - Server OS: Requires stability, security, and continuous operations (Linux)
    - Mobile OS: Rely on power efficiency and tight hardware integration to extend battery life (Android)

## 🧪 Real-World Example: Opening a Web Browser
- When a user opens a web browser such as Google Chrome, the operating system performs multiple coordinated actions:

1. **User Action (GUI / CLI)**
    - The user clicks the browser icon (GUI) or runs a command (CLI)
2. **Process Creation**
    - The OS creates a new process for the browser
    - Assigns a unique Process ID (PID)
3. **Memory Allocation**
    - The OS allocates RAM for the browser to run
    - Loads required files and libraries into memory
4. **File System Access**
    - The OS locates the browser executable on disk
    - Reads configuration and system files
5. **Device Interaction**
    - Uses drivers to interact with hardware (CPU, disk, network card)
6. **Network Communication**
   - The application (Google Chrome) initiates the request
   - It uses system calls to ask the OS to send data (TCP/IP)
   - The OS then passes data to the network interface card (NIC) via drivers
7. **Security Enforcement**
    - The browser runs in user space, preventing direct hardware access
    - The OS enforces permissions and isolates the process from others

💡 This process shows how the OS manages resources, ensures stability, and enforces security every time an application is launched

## 🛠️ Practical Skills Developed
- Understanding OS structure and functionality
- Identifying how processes and memory are managed
- Using both GUI and CLI environments
- Recognising OS-level security mechanisms

## 🧰 Tools Used
- Solent University Cybersecurity Coursework
- TryHackMe platform
- Windows Operating System
- Linux (terminal-based environment)

## 🔐 Security Relevance
- Understanding OS internals is essential for:
    - Detecting malicious processes
    - Analysing system behaviour
    - Identifying privilege escalation attacks
    - Hardening systems against vulnerabilities

💡 Many cyber attacks target weaknesses in OS design or misconfiguration

## 📌 Lessons Learned
⚠️ The OS is not just software, it is the control center of the entire system
⚠️ System security depends heavily on proper OS configuration and isolation  
⚠️ Understanding OS internals and CLI usage is essential for cybersecurity roles