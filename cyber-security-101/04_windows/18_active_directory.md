# Windows – TryHackMe

Platform: TryHackMe     
Skill Level: Beginner / Foundation     
Focus Area: Active Directory

## 🎯 Objective
- Understand how Active Directory organizes a Windows domain.
- Learn about common Active Directory objects.
- Understand Organizational Units (OUs) and groups.
- Learn how Group Policy helps administrators manage computers and users.

## 🧠 Core Concepts Learned

## Active Directory Overview
**Active Directory (AD)** is the directory service used by a **Domain Controller** to manage and organize resources within a Windows domain.

```text
Windows Domain
      ↓
Domain Controller
      ↓
Active Directory
      ↓
Users • Computers • Groups • OUs • Policies
```

## Active Directory Objects
Everything stored inside Active Directory is considered an **object**.

For example:
```text
Active Directory
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

Common objects include:
- **Users** – Represent people or service accounts.
- **Computers** – Represent computers connected to the domain.
- **Groups** – Combine users or computers to make permissions easier to manage.

## Organizational Units (OUs)
**Organizational Units (OUs)** are containers used to organize objects inside Active Directory.

For example:

```text
Company
│
├── IT
│   ├── Alice
│   └── PC-01
│
├── HR
│   ├── Bob
│   └── PC-02
│
└── Finance
    ├── John
    └── PC-03
```

This allows administrators to organize users and computers based on departments or other requirements.

💡 Think of an **OU as a folder used to organize Active Directory objects**.

## Groups
**Groups** are used to give permissions to multiple users at once.

Instead of:

```text
Alice → Permission
Bob   → Permission
John  → Permission
```

An administrator can use:

```text
Alice ─┐
Bob   ─┼──→ IT Group → Permission
John  ─┘
```

This makes permissions much easier to manage.

## Group Policy
**Group Policy** allows administrators to centrally configure settings for users and computers in a domain.

For example, an administrator could:
- Set password requirements.
- Disable certain Windows settings.
- Configure security settings.
- Apply settings to many computers at once.

These settings are managed using **Group Policy Objects (GPOs)**.

For example:

```text
GPO
"Disable Control Panel"
        ↓
      IT OU
        ↓
All affected users/computers receive the policy
```

## 🛠️ Practical Skills Developed
- Explored the structure of Active Directory.
- Identified users, computers, groups, and OUs.
- Understood how groups simplify permission management.
- Learned how Group Policy can centrally manage domain systems.

## 🧰 Tools Used
- Active Directory
- TryHackMe platform

## 🔐 Security Relevance
- Active Directory is commonly used to manage users and computers in organizations.
- Attackers often target Active Directory accounts, permissions, and configurations to gain access to additional systems or increase their privileges.
- Understanding how AD is structured helps both attackers and defenders understand how access is controlled across a Windows domain.

## 📌 Lessons Learned
💡 Active Directory provides centralized management of users, computers, groups, and policies within a Windows domain.

**OU → Organize objects**  
**Group → Manage permissions**  
**GPO → Apply settings and policies**