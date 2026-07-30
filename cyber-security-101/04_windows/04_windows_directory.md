# Windows – TryHackMe

Platform: TryHackMe    
Skill Level: Beginner / Foundation   
Focus Area: The Windows Directory

## 🎯 Objective
- Understand the purpose of the Windows directory.
- Learn what environment variables are and why they are useful.
- Become familiar with the System32 folder and its importance.

## 🧠 Core Concepts Learned
## The Windows Directory
The **Windows** directory (`C:\Windows`) contains the core files required for the Windows operating system to function.   
Although Windows is typically installed on the **C:** drive, it can technically be installed on another drive or in a different directory.  
The Windows directory contains many important subfolders that store system files, configuration data, drivers, fonts, logs, and built-in utilities.  

## Environment Variables
An **environment variable** is a named value that stores information about the operating system or user environment.  
Instead of using a full directory path, Windows can reference these variables, making scripts and applications more portable.  

## Common Environment Variables

| Variable | Typical Value | Description |
|----------|---------------|-------------|
| `%windir%` | `C:\Windows` | Windows installation directory. |
| `%SystemRoot%` | `C:\Windows` | Another variable that points to the Windows directory. |
| `%SystemDrive%` | `C:` | Drive where Windows is installed. |
| `%TEMP%` | `C:\Users\<User>\AppData\Local\Temp` | Stores temporary files. |
| `%USERPROFILE%` | `C:\Users\<User>` | Current user's profile folder. |

## Why Use `%windir%` Instead of `C:\Windows`?
For example, if Windows is installed on the **D:** drive instead of **C:**:

**Hardcoded path**
```text
C:\Windows
```
❌ Only works if Windows is installed on the **C:** drive.

**Environment variable**
```text
%windir%
```
✅ Automatically expands to the correct Windows directory (for example, `D:\Windows`).

This allows scripts, applications, and administrators to reference the Windows installation directory without knowing its exact location.

## System32
The **System32** folder (`C:\Windows\System32`) contains many of the files required for Windows to operate.  

It includes:
- Core system libraries (DLL files)
- Windows utilities
- Administrative tools
- Device drivers
- System configuration files

Many of the tools used by system administrators and security professionals are located in this directory.

Examples include:

| Tool | Purpose |
|------|---------|
| `cmd.exe` | Command Prompt |
| `WindowsPowerShell` | PowerShell |
| `taskmgr.exe` | Task Manager |
| `regedit.exe` | Registry Editor |
| `mstsc.exe` | Remote Desktop Connection |

> ⚠️ **Use caution:** Modifying or deleting files within the **System32** directory can cause Windows to become unstable or even fail to boot.

## 🛠️ Practical Skills Developed
- Locate the Windows installation directory.
- Use common environment variables.
- Identify the purpose of the System32 folder.
- Recognize common Windows administrative tools.

## 🧰 Tools Used
- TryHackMe platform
- File Explorer
- Windows

## 🔐 Security Relevance
- Many Windows administrative and security tools are stored within **System32**.
- Malware often targets or impersonates files in the Windows directory to evade detection.
- Environment variables are frequently used in scripts, malware, and forensic investigations to reference important system locations.

## 📌 Lessons Learned
💡 The Windows directory contains the operating system's essential files, while **System32** houses many of the tools and libraries Windows relies on every day. Understanding environment variables such as `%windir%` makes navigating Windows and analyzing scripts much easier.