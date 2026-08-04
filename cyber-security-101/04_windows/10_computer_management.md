# Windows – TryHackMe

Platform: TryHackMe  
Skill Level: Beginner / Foundation  
Focus Area: Computer Management  

## 🎯 Objective
- Understand the purpose of the Computer Management console.
- Explore the tools available under System Tools, Storage, and Services and Applications.
- Learn how administrators monitor, configure, and troubleshoot Windows systems.
- Recognize how these tools are valuable during system administration and incident investigations.

## 🧠 Core Concepts Learned
## What is Computer Management?
**Computer Management (`compmgmt.msc`)** is a Microsoft Management Console (MMC) that brings together many of Windows' administrative tools into a single interface.

From one console, administrators can manage users, hardware, storage, shared resources, scheduled tasks, services, and monitor overall system activity.

Because it centralizes these essential tools, Computer Management is often one of the first utilities used when troubleshooting, maintaining, or investigating a Windows system.

The console is divided into three main sections:
- **System Tools**
- **Storage**
- **Services and Applications**

## → System Tools
### Task Scheduler
**Task Scheduler** automates tasks by launching applications, scripts, or commands when specific conditions are met.

Tasks can be triggered:
- At system startup
- At user logon or logoff
- On a schedule (daily, weekly, every few minutes, etc.)
- When a specific event occurs

> Scheduled tasks are commonly used for backups, maintenance, software updates, and automated scripts.

### Event Viewer
**Event Viewer (`eventvwr.msc`)** records system activity by storing Windows event logs.
It acts as an audit trail for the operating system and is one of the first places administrators check when troubleshooting problems.

**Common Windows Logs**
- **Application** – Software events
- **Security** – Authentication and auditing events
- **Setup** – Installation events
- **System** – Windows components and drivers
- **Forwarded Events** – Events collected from remote systems

Event Viewer is one of the most valuable forensic tools because it records:
- User logins
- Failed login attempts
- Service activity
- System changes
- Application crashes
- Security events

### Shared Folders
Displays resources that are shared across the network.

Sections include:
- **Shares** – Shared folders (including administrative shares like `C$` and `ADMIN$`)
- **Sessions** – Connected users
- **Open Files** – Files currently being accessed remotely

Administrators can quickly identify:
- Who is connected
- Which files are open
- Potential unauthorized access

### Local Users and Groups
Launches **Local Users and Groups (`lusrmgr.msc`)**, allowing administrators to manage:
- Local users
- Local groups
- Group membership

> This snap-in is unavailable in Windows Home editions.

### Performance Monitor
**Performance Monitor (`perfmon`)** collects real-time and historical performance data.

Common metrics include:
- CPU usage
- Memory usage
- Disk activity
- Network utilization

It is useful when diagnosing slow or unstable systems.

### Device Manager
**Device Manager (`devmgmt.msc`)** displays all installed hardware devices.

Administrators can:
- Enable or disable hardware
- Update drivers
- Roll back drivers
- Troubleshoot hardware issues
- View hardware properties

## → Storage
### Disk Management
**Disk Management (`diskmgmt.msc`)** manages storage devices and partitions.

Common tasks include:
- Initializing new disks
- Creating partitions
- Extending partitions
- Shrinking partitions
- Formatting drives
- Changing drive letters

> Windows Server includes additional storage tools that are not normally available on Windows Home editions.

## → Services and Applications
### Services
Windows services are background applications that often start automatically when Windows boots.

Each service has:
- Display name
- Service name
- Status
- Startup type
- Executable path

Startup Types
- **Automatic** – Starts during system boot.
- **Manual** – Starts only when required.
- **Disabled** – Cannot be started until re-enabled.

> Malware often installs itself as a Windows service to maintain persistence. Reviewing unfamiliar services is a common step during incident response.

### Windows Management Instrumentation (WMI)
**Windows Management Instrumentation (WMI)** provides a standardized interface for managing Windows systems locally or remotely.

Administrators can use WMI to:
- Retrieve system information
- Query hardware details
- Manage services
- Monitor processes
- Automate administrative tasks

Many management tools and PowerShell cmdlets rely on WMI.

## 🛠️ Practical Skills Developed
- Navigated the Computer Management console.
- Examined scheduled tasks and their triggers.
- Reviewed Windows Event Logs.
- Identified shared folders and active sessions.
- Managed local users and groups.
- Monitored system performance.
- Viewed storage partitions using Disk Management.
- Examined Windows services and startup types.
- Explored WMI and its administrative capabilities.

## 🧰 Tools Used
- TryHackMe platform
- Computer Management (`compmgmt.msc`)
- Task Scheduler (`taskschd.msc`)
- Event Viewer (`eventvwr.msc`)
- Shared Folders
- Local Users and Groups (`lusrmgr.msc`)
- Performance Monitor (`perfmon`)
- Device Manager (`devmgmt.msc`)
- Disk Management (`diskmgmt.msc`)
- Services (`services.msc`)
- Windows Management Instrumentation (WMI)

## 🔐 Security Relevance
Many tools within Computer Management are frequently used by both system administrators and security analysts during investigations.

Examples include:
- **Task Scheduler** – Detect malicious scheduled tasks used for persistence.
- **Event Viewer** – Investigate authentication events, system errors, and security incidents.
- **Shared Folders** – Identify active network sessions and unauthorized file access.
- **Services** – Detect suspicious or malicious services that start automatically.
- **Performance Monitor** – Spot abnormal resource usage that may indicate malware.
- **Device Manager** – Identify unauthorized or malfunctioning hardware.
- **WMI** – Understand legitimate system management as well as attacker techniques involving remote execution and persistence.

## 📌 Lessons Learned 
💡 Computer Management provides a centralized location for many of Windows' most important administrative tools. Learning where these tools are located—and when to use them—makes troubleshooting faster and is an essential skill for both system administrators and cybersecurity professionals.