# Windows – TryHackMe

Platform: TryHackMe    
Skill Level: Beginner / Foundation   
Focus Area: System Information (msinfo32)  

## 🎯 Objective
- Understand the purpose of the System Information utility.
- Explore the information available about hardware, components, and the software environment.
- Learn how System Information assists with troubleshooting and system diagnostics. 

## 🧠 Core Concepts Learned
## What is System Information?
**System Information (`msinfo32`)** is a Windows utility that gathers detailed information about the computer's hardware, system components, and software environment.

It provides a centralized view of system configuration, making it useful for troubleshooting, diagnostics, and verifying system specifications.

The information is organized into three main categories:
- **Hardware Resources**
- **Components**
- **Software Environment**

## System Summary
The **System Summary** provides general information about the computer, including:
- Operating system version
- Computer name
- Processor
- Installed memory (RAM)
- BIOS version
- System manufacturer and model
- Boot device

This section offers a quick overview of the system's technical specifications.

### → Hardware Resources
Displays low-level hardware resource information, including:
- IRQs (Interrupt Requests)
- DMA channels
- Memory addresses
- I/O ports

> This information is primarily useful for advanced troubleshooting and hardware diagnostics.

### → Components
Provides detailed information about installed hardware devices.

Examples include:
- Display (graphics adapter)
- Storage devices
- Network adapters
- USB devices
- Sound devices
- Input devices

> This section helps verify installed hardware and driver information.

### → Software Environment
Displays information about the operating system and installed software.

Common sections include:
- Running Tasks
- Services
- Drivers
- Loaded Modules
- Network Connections
- Environment Variables

> This information is particularly useful when troubleshooting software or startup issues.

## 🛠️ Practical Skills Developed
- Opened System Information (`msinfo32`).
- Examined system specifications.
- Explored hardware resource information.
- Reviewed installed hardware components.
- Investigated the software environment.
- Located and understood environment variables.
- Used the search feature to quickly find system information.

## 🧰 Tools Used
- TryHackMe platform
- System Information (`msinfo32`)

## 🔐 Security Relevance
System Information is commonly used during system administration and incident response to quickly gather information about a Windows machine.

It can help analysts:
- Verify hardware and operating system details.
- Identify installed network adapters and IP addresses.
- Review running services and drivers.
- Inspect environment variables.
- Gather system information before beginning an investigation.


## 📌 Lessons Learned 
💡 System Information (`msinfo32`) provides a centralized view of a Windows system's hardware, software, and configuration. It is an essential diagnostic tool for troubleshooting, verifying system specifications, and gathering information during security investigations.