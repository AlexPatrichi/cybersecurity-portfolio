# Windows – TryHackMe

Platform: TryHackMe    
Skill Level: Beginner / Foundation   
Focus Area: User Accounts, Profiles, and Permissions

## 🎯 Objective
- Understand the different types of local user accounts in Windows.
- Learn how Windows creates and stores user profiles.
- Understand how groups simplify permission management.
- Learn basic methods for viewing and managing local users and groups.

## 🧠 Core Concepts Learned
## User Account Types
Windows local user accounts are generally one of two types:

- **Administrator**
  - Has full control over the system.
  - Can create and delete users, install software, modify system settings, and manage groups.

- **Standard User**
  - Has limited permissions.
  - Can manage personal files and settings but cannot make system-wide changes.

💡 The account type determines what actions a user is permitted to perform on the system.

## User Profiles
- A user profile is automatically created the first time a user logs in.
- Profiles are stored in:

```text
C:\Users\<username>
```

- Common folders within a profile include:
  - Desktop
  - Documents
  - Downloads
  - Music
  - Pictures

💡 Each user has a separate profile to keep their files and settings isolated from other users.

## Local Users and Groups
Windows provides **Local Users and Groups Management** for managing local accounts and permissions.

It can be opened using:

```text
lusrmgr.msc
```

This console contains:
- **Users** – Manage local user accounts.
- **Groups** – Manage permission groups.

## Groups
- A group is a collection of predefined permissions.
- Users inherit the permissions of every group they belong to.
- A user can belong to multiple groups at the same time.

💡 Using groups makes permission management much easier than assigning permissions individually.

## 🛠️ Practical Skills Developed
- Identified the difference between Administrator and Standard User accounts.
- Located user profile folders in `C:\Users`.
- Viewed and managed local users through Windows Settings.
- Opened Local Users and Groups Management using `lusrmgr.msc`.
- Understood how Windows groups are used to assign permissions.

## 🧰 Tools Used
- TryHackMe platform
- Windows Settings

## 🔐 Security Relevance
- Applying the **principle of least privilege** helps reduce security risks by giving users only the permissions they require.
- Separating administrator and standard accounts limits the impact of accidental or malicious actions.
- Group-based permission management simplifies administration and reduces configuration errors.

## 📌 Lessons Learned
💡 Windows controls what users can do through **account types** and **group memberships**. User profiles store each user's personal files and settings, while groups provide a scalable way to assign permissions across multiple users.