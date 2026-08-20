# Windows – TryHackMe

Platform: TryHackMe     
Skill Level: Beginner / Foundation     
Focus Area: Windows Domains

## 🎯 Objective
- Understand what a Windows Domain is.
- Learn the purpose of a Domain Controller.
- Understand how Active Directory manages users and computers.
- Learn why domains are commonly used in organizations.

## 🧠 Core Concepts Learned
## What is a Windows Domain?
A **Windows Domain** is a group of computers and users that are managed together from a central location.

Instead of managing every computer separately, an organization can use a domain to centrally manage:
- Users
- Computers
- Passwords and accounts
- Permissions
- Security settings

For example:
```text
Domain Controller (Server)
│
└── Active Directory
    │
    ├── Users
    │   ├── Alice
    │   └── Bob
    │
    ├── Groups
    │   ├── IT
    │   └── HR
    │
    └── Computers
        ├── PC-01
        └── PC-02
```

## Domain Controller
A **Domain Controller (DC)** is a server responsible for managing the domain.

It handles tasks such as:
- Authenticating users.
- Managing user and computer accounts.
- Applying security policies.
- Controlling access to domain resources.

💡 Think of the **Domain Controller as the central authority of the domain**.

## Active Directory
**Active Directory Domain Services (AD DS)** or simply **Active Directory (AD)** is Microsoft's directory service used to store and manage users, computers, groups, and other resources in a Windows Domain.

For example, when an employee logs into a domain computer:

```text
Alice logs into PC-01
        ↓
PC-01 contacts the Domain Controller
        ↓
Active Directory / domain services check Alice's account
        ↓
Credentials valid?
        ↓
       YES
        ↓
Alice can log in
```

## Users and Groups
Users can be placed into **groups** to make permissions easier to manage.

Instead of giving permissions to every user individually:

```text
Alice ─┐
Bob   ─┼──→ IT Group ──→ Access to IT resources
John  ─┘
```

Permissions can be assigned to the group, and members of that group receive those permissions.

## 🛠️ Practical Skills Developed
- Identified the purpose of a Windows Domain.
- Learned the role of a Domain Controller.
- Explored basic Active Directory concepts.
- Understood how users and computers can be centrally managed.

## 🧰 Tools Used
- TryHackMe platform
- Windows 
- Active Directory

## 🔐 Security Relevance
- Windows Domains and Active Directory are widely used in organizations.
- If an attacker compromises a Domain Account or Domain Controller, they may gain access to other computers and resources across the network.
- Understanding Active Directory is therefore important for both offensive and defensive cybersecurity.

## 📌 Lessons Learned
💡 A Windows Domain allows an organization to centrally manage users, computers, permissions, and security policies. The Domain Controller and Active Directory are key components that make this possible.