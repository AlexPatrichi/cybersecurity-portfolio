# Windows – TryHackMe

Platform: TryHackMe    
Skill Level: Beginner / Foundation   
Focus Area: User Accounts Control (UAC)

## 🎯 Objective
- Understand the purpose of User Account Control (UAC).
- Learn how UAC helps protect Windows from unauthorized system changes.
- Understand the difference between standard and elevated privileges.

## 🧠 Core Concepts Learned
## What is User Account Control (UAC)?
- **User Account Control (UAC)** is a Windows security feature that helps prevent unauthorized changes to the operating system.
- It was introduced in **Windows Vista** and is included in all modern versions of Windows.
- UAC reduces the risk of malware gaining administrator-level access without the user's knowledge.

## Why UAC Exists
Even if a user is a member of the **Administrators** group, Windows does **not** automatically run every program with full administrative privileges.

Instead:
- The user operates with **standard user privileges** during normal use.
- Administrative privileges are requested **only when needed**.

This helps limit the damage that malicious software can cause.

## UAC Prompt
When an action requires elevated privileges (such as installing software or changing system settings), Windows displays a **UAC prompt** asking for permission.

Depending on the account type:
- **Administrator account:** prompted to **confirm** the action.
- **Standard User account:** prompted to enter the credentials of an administrator.

If permission or credentials are not provided, the operation is cancelled.

## UAC Shield Icon
Some applications display a **shield icon** on their shortcut or executable.

This indicates that:
- The application requires administrator privileges.
- Launching it will trigger a UAC prompt.

## 🛠️ Practical Skills Developed
- Recognized applications that require elevated privileges.
- Identified the UAC shield icon.
- Observed how Windows requests administrator approval before performing privileged actions.
- Understood the different UAC experience for Administrator and Standard User accounts.

## 🧰 Tools Used
- TryHackMe platform
- User Account Control (UAC)
- Local Users and Groups (`lusrmgr.msc`)

## 🔐 Security Relevance
- UAC follows the **principle of least privilege**, allowing users to run with standard permissions until elevated access is required.
- Prevents many unauthorized system changes by requiring explicit approval.
- Makes it more difficult for malware to silently install software or modify critical system settings.

## 📌 Lessons Learned
💡 User Account Control acts as a security checkpoint between normal user activity and administrative actions. By requiring approval or administrator credentials before elevated operations, UAC helps reduce the risk of accidental or malicious system changes.