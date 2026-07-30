# Windows – TryHackMe

Platform: TryHackMe    
Skill Level: Beginner / Foundation   
Focus Area: Windows File Systems  

## 🎯 Objective
- Understand the purpose of a file system.
- Learn the differences between FAT and NTFS.
- Explore key NTFS features, including permissions and Alternate Data Streams (ADS).

## 🧠 Core Concepts Learned
## ## What is a File System?
A **file system** defines how an operating system stores, organizes, and retrieves data on a storage device such as a hard drive, SSD, or USB flash drive.  

---

## Evolution of Windows File Systems
Windows has used several file systems over the years, each improving on the limitations of its predecessor.    

**FAT (File Allocation Table)** was the original family of file systems used by Windows and DOS.  
**HPFS (High Performance File System)** 
**NTFS (New Technology File System)** was later introduced to provide better security, reliability, and support for modern storage devices.  


| File System | Introduced | Notes |
|-------------|:----------:|-------|
| **FAT16** | 1984 | Simple and widely compatible but limited in file size and security. |
| **FAT32** | 1996 | Improved FAT16 by supporting larger partitions, but individual files are still limited to **4 GB**. Commonly found on USB drives and SD cards. |
| **HPFS** | 1989 | Designed for IBM OS/2 with improved performance over FAT but eventually replaced. |
| **NTFS** | 1993 | Modern Windows file system offering security, reliability, and advanced features. |

Today, **NTFS (New Technology File System)** is the default file system used by modern Windows installations.

---

## Why NTFS?
NTFS was designed to overcome many limitations of FAT-based file systems.  

Key advantages include:
- Supports files larger than **4 GB**.
- Supports very large storage volumes.
- Provides file and folder permissions.
- Supports file compression.
- Supports encryption through **Encrypting File System (EFS)**.
- Improves reliability using **journaling**.

## Journaling
NTFS is known as a **journaling file system**.  

Before making important changes to the file system, NTFS records them in a **journal (log)**.  

If the computer loses power or crashes unexpectedly, Windows can use this journal to recover the file system and reduce the risk of corruption.  

Unlike FAT, NTFS can automatically recover from many file system errors.  

## NTFS Permissions
One of NTFS's biggest advantages is the ability to control who can access files and folders.   

Common permissions include: 

| Permission | Description |
|------------|-------------|
| **Full Control** | Complete access, including changing permissions and ownership. |
| **Modify** | Read, write, edit, and delete files. |
| **Read & Execute** | View and run files or applications. |
| **List Folder Contents** | View the contents of a folder. |
| **Read** | View files and their contents. |
| **Write** | Create new files or modify existing ones. |

### Viewing Permissions
To view a file or folder's permissions:  

1. Right-click the file or folder.
2. Select **Properties**.
3. Open the **Security** tab.
4. Select a user or group to view their assigned permissions.

---

## Alternate Data Streams (ADS)
**Alternate Data Streams (ADS)** are a feature unique to NTFS.  

Normally, a file contains a single data stream (`$DATA`), but NTFS allows additional hidden streams to be attached to the same file.  

### Common Uses
- Stores metadata about downloaded files.
- Allows applications to save additional information without modifying the main file.

### Security Implications
Because Windows File Explorer does not display ADS by default, attackers have abused ADS to hide malicious data or malware.

However, ADS also has legitimate uses. For example, Windows records whether a file was downloaded from the Internet by storing information in an alternate data stream.

---

## FAT vs NTFS

| Feature | FAT32 | NTFS |
|---------|:-----:|:----:|
| Maximum file size | **4 GB** | Very large files |
| File permissions | ❌ | ✅ |
| Encryption | ❌ | ✅ |
| Compression | ❌ | ✅ |
| Journaling | ❌ | ✅ |
| Reliability | Basic | High |
| Common use today | USB drives, SD cards | Windows system drives |

## 🛠️ Practical Skills Developed
- Identify the Windows file system in use.
- Differentiate between FAT32 and NTFS.
- View NTFS permissions on files and folders.
- Understand how NTFS improves security and reliability.
- Recognize the purpose of Alternate Data Streams.

## 🧰 Tools Used
- TryHackMe platform
- Windows Desktop
- File Explorer

## 🔐 Security Relevance
- NTFS permissions form the basis of Windows access control.
- Misconfigured permissions can expose sensitive files or allow privilege escalation.
- Alternate Data Streams can be abused by attackers to hide malicious data.
- Understanding the Windows file system is essential for forensic investigations, malware analysis, and system administration. 

## 📌 Lessons Learned
💡  NTFS is the standard file system used by modern Windows operating systems because it provides better security, reliability, and functionality than older file systems like FAT32. Features such as permissions, journaling, encryption, and Alternate Data Streams make NTFS an essential concept for Windows administration and cybersecurity.  




