# Windows – TryHackMe

Platform: TryHackMe     
Skill Level: Beginner / Foundation     
Focus Area: Windows Security

## 🎯 Objective
- Understand the purpose of Windows Security.
- Learn about the built-in security features in Windows.
- Understand how Windows protects the system from common threats.

## 🧠 Core Concepts Learned
## What is Windows Security?
**Windows Security** is the built-in security application used to view and manage the protection of a Windows system.

It provides access to several security areas, including:
### 1. Virus & Threat Protection
**Microsoft Defender Antivirus** helps protect the computer against malware such as viruses, spyware, and ransomware.

From here, you can:
- Run malware scans.
- Check for detected threats.
- View protection history.
- Manage antivirus settings.
- Check for security intelligence updates.

Virus & Threat Protection is divided into:
A. **Current threats**
#### Scan Options
Microsoft Defender provides different types of scans:

- **Quick scan** – Checks locations where threats are commonly found.
- **Full scan** – Checks all files and running programs on the system.
- **Custom scan** – Allows you to choose specific files or folders to scan.

#### Threat History
- **Quarantined threats** – Suspicious or malicious files that have been isolated and prevented from running.
- **Allowed threats** – Detected threats that the user has manually allowed to run.

B. **Virus & threat protection settings**
#### Protection Settings
- **Real-time protection** – Continuously monitors the system and stops malware from installing or running.
- **Cloud-delivered protection** – Uses Microsoft's latest threat information to help detect new threats faster.
- **Controlled folder access** – Helps protect important files and folders from unauthorized changes, including ransomware.
- **Exclusions** – Allows specific files or folders to be ignored by antivirus scans.

> Exclusions should be used carefully because malware inside an excluded location may not be detected.

#### Security Intelligence Updates
Microsoft Defender regularly receives updated threat definitions to recognize newly discovered malware.

Updates can also be checked manually from **Virus & threat protection updates**.

### 2. Firewall & Network Protection
**Microsoft Defender Firewall** controls network traffic entering and leaving the computer.

It helps prevent unauthorized network connections and provides different settings for:
- Domain networks
- Private networks
- Public networks

### 3. App & Browser Control
Helps protect the system from potentially malicious applications, files, websites, and downloads.

It includes features such as **Microsoft Defender SmartScreen**, which can warn users about suspicious or potentially unsafe content.

### 4. Device Security
Provides information about security features built into the computer's hardware.

These features can provide additional protection against attacks and unauthorized changes to the system.

### 5. Account Protection
Provides information about the security of Windows user accounts and sign-in options.

## Status Icons 
- 🟢 Green means your device is sufficiently protected, and there aren't any recommended actions.
- 🟡 Yellow means there is a safety recommendation for you to review.
- 🔴 Red is a warning that something needs your immediate attention.

## 🛠️ Practical Skills Developed
- Opened and explored Windows Security.
- Checked the system's virus and threat protection.
- Viewed firewall and network protection settings.
- Identified areas of Windows that may require security attention.

## 🧰 Tools Used
- Windows Security
- Microsoft Defender
- TryHackMe platform

## 🔐 Security Relevance
- Windows Security provides several layers of protection against common cyber threats.
- Understanding these features helps identify security problems, detect malware, control network access, and keep a Windows system protected.

## 📌 Lessons Learned
💡 Windows Security combines several built-in protection features in one place. Regularly checking its security areas can help identify problems and keep the system protected.