# Linux – TryHackMe 

Platform: TryHackMe    
Skill Level: Beginner / Foundation  
Focus Area: Common Directories

## 🎯 Objective 
- Understand the purpose of common Linux directories.
- Learn how Linux organises files using a hierarchical structure.
- Recognise directories that are important for system administration and cybersecurity investigations.

## 🧠 Core Concepts Learned   
## Key Directories in Linux

### `~` (Home Directory) 
- Shortcut that represents the current user’s home directory   
- Example: `cd ~`  

### `/` 
- The root directory, which sits at the top of the Linux filesystem hierarchy.  
- All files and directories originate from this location.  

### `/home`
- Stores the home directories of regular users.
- May contain user documents, scripts, SSH keys, and other personal files relevant to investigations.
- Example: `/home/user1`

### `/etc` 
- Contains system-wide configuration files.
- Important because it stores information about user accounts and system settings.  
- Example: `/etc/passwd`

### `/var` 
- Stores variable data that changes during normal system operation.
- Example: `/var/log` 

### `/tmp` 
- Stores temporary files created by users and applications.
- Contents are often deleted automatically after a reboot.  

## 🛠️ Practical Skills Developed
- Navigating the Linux filesystem hierarchy.
- Identifying the purpose of common Linux directories.
- Locating user files, configuration files, and log data.
- Recognising directories that may be relevant during security investigations.

## 🧰 Tools Used 
- TryHackMe platform 
- Linux Terminal

## 🔐 Security Relevance
- Attackers may abuse `/tmp` to store malicious scripts or payloads.
- Log files stored in `/var/log` can provide valuable evidence during incident response investigations.
- Configuration files within `/etc` may reveal important system settings and user account information.
- Understanding common Linux directories enables faster navigation and more effective investigations.

## 📌 Lessons Learned 
💡 Linux uses a structured hierarchy to organise files.    
💡 Many logs and sensitive configuration files are stored in these directories, making them important during security investigations.     
💡 Understanding these directories improves system navigation, troubleshooting, and investigative efficiency.    
💡 Knowing where to look is just as important as knowing which commands to use during security investigations.   