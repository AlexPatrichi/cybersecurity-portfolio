Windows – TryHackMe

Platform: TryHackMe
Skill Level: Beginner / Foundation
Focus Area: System Configuration (MSConfig)

## 🎯 Objective
- Understand the purpose of the System Configuration (MSConfig).
- Learn the function of each MSConfig tab.
- Understand how Windows manages startup applications.
- Learn the purpose of Advanced System Settings, Virtual Memory, and Crash Dumps.

## 🧠 Core Concepts Learned
## What is MSConfig?
**System Configuration (MSConfig)** is a Windows troubleshooting tool used to diagnose startup problems and configure how Windows boots.

> Note: Administrator privileges are required.

### Launch MSConfig
- Start Menu → System Configuration
- Win + R → msconfig

---

## MSConfig Tabs
### General
- Controls what Windows loads during startup.

**Startup Modes**  
- Normal Startup – Loads all drivers and services.
- Diagnostic Startup – Loads only essential Windows components for troubleshooting.
- Selective Startup – Allows specific services and startup items to be enabled or disabled.

> Useful when isolating startup issues.

### Boot
- Configures how Windows starts.

Common options include:
    - Safe Boot
    - Boot Timeout
    - Default Operating System
    - Advanced Boot Options

> This tab is commonly used during troubleshooting.

### Services
- Displays all installed Windows services (running or stopped).
- A service is a background application that runs without user interaction.

> Useful for troubleshooting by temporarily disabling third-party services.

### Startup
- The Startup tab behaves differently depending on the Windows version.
1. Windows 10 / Windows 11
- MSConfig no longer manages startup applications.
- Instead, Microsoft redirects to **Task Manager → Startup Apps**

2. Windows Server
- Startup programs are typically found in the Startup folder.
- This folder contains shortcuts or executables that automatically run when the user signs in.

Open it with:
```text
Win + R
shell:startup
```

>Startup folders are commonly checked during security investigations because malware often adds itself here to achieve persistence after reboot.

### Tools
- Provides quick access to various Windows administrative utilities.

Each tool includes:
- A short description
- The command used to launch it

---

## Advanced System Settings
- Additional configuration settings which you can use to control the performance behavior and system recovery.
- Open View advanced system settings from the Start Menu.

### Virtual Memory (Page File)
- When physical RAM becomes full, Windows uses a **page file** stored on disk as additional memory.
- This is called Virtual Memory.  

The page file helps:
1. Prevent application crashes
2. Reduce out-of-memory errors
3. Allow the operating system to continue functioning when RAM is exhausted

> Note: Virtual memory is much slower than RAM because it uses the storage drive.

### Startup and Recovery
- These settings control how Windows behaves after a critical system failure.

Located under:
```text 
Advanced → Startup and Recovery → Settings
```

- When Windows encounters a fatal system error (such as a Blue Screen of Death (BSOD)), it can create a **memory dump** to help identify the cause.
- A **memory dump** records information about the system at the time of the crash and helps administrators or forensic analysts determine what caused the failure.

#### Crash Dump Types
- Windows supports several types of crash dumps:
    - Automatic Memory Dump
    - Kernel Memory Dump
    - Small Memory Dump (256 KB)
    - Complete Memory Dump
    - None

- Each type saves a different amount of system information, balancing diagnostic detail against storage usage.

## 🛠️ Practical Skills Developed
- Launching and navigating MSConfig.
- Understanding Windows startup modes.
- Identifying and managing Windows services.
- Locating startup applications on Windows client and server systems.
- Viewing Virtual Memory and Startup & Recovery settings.

## 🧰 Tools Used
- TryHackMe platform
- Task Manager
- System Configuration (`msconfig`)
- Advanced System Settings (`sysdm.cpl`)

## 🔐 Security Relevance
- Identify suspicious or unnecessary services.
- Investigate startup persistence used by malware.
- Understand how startup configuration affects system security.
- Use crash dumps to assist with troubleshooting and incident response.

## 📌 Lessons Learned 
💡 MSConfig is primarily a troubleshooting tool rather than a startup manager. It helps diagnose boot issues, manage services, and access advanced Windows configuration options. Understanding startup behavior, virtual memory, and crash dump settings is valuable for both system administration and cybersecurity investigations.