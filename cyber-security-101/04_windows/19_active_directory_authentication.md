# Windows – TryHackMe

Platform: TryHackMe     
Skill Level: Beginner / Foundation     
Focus Area: Active Directory Authentication

## 🎯 Objective
- Understand how authentication works in a Windows domain.
- Learn the basic Kerberos authentication process.
- Understand the purpose of TGT and TGS tickets.
- Learn how NetNTLM uses challenge-response authentication.

## 🧠 Core Concepts Learned
## Authentication Methods
Windows domains mainly use two authentication protocols:

- **Kerberos** – The default authentication protocol in modern Windows domains.
- **NetNTLM** – An older authentication protocol maintained for compatibility.

## Kerberos Authentication
**Kerberos** is a ticket-based authentication protocol.

Instead of repeatedly sending credentials when accessing resources, Kerberos uses **tickets** to prove the user's identity.

### TGT – Ticket Granting Ticket
After successfully authenticating, the user receives a **Ticket Granting Ticket (TGT)**.

The TGT can then be used to request additional tickets for specific services.

```text
User logs in
     ↓
Authentication
     ↓
Receives TGT
```
💡 Think of the TGT as proof that you have already authenticated.

### TGS – Ticket Granting Service
When the user wants to access a service, the TGT is used to request a service ticket (TGS) for that service.

```text
User
 ↓
TGT
 ↓
Requests access to File Server
 ↓
Receives TGS / Service Ticket
 ↓
Presents ticket to File Server
 ↓
File Server
```

The service ticket can then be presented to the requested service.

💡 TGT = Used to request more tickets
💡 TGS / Service Ticket = Used to access a specific service

## NetNTLM Authentication
NetNTLM is an older authentication protocol that uses a challenge-response mechanism.

Simplified process:
```text
Client requests access
        ↓
Server sends a challenge
        ↓
Client creates a response
        ↓
Server verifies the response
        ↓
Access granted
```
The user's actual password is not transmitted across the network.

## 🛠️ Practical Skills Developed
- Identified the main authentication protocols used in Windows domains.
- Understood the basic Kerberos ticket process.
- Learned the difference between TGT and service tickets.
- Understood the basic NetNTLM challenge-response process.

## 🧰 Tools Used
- TryHackMe platform

## 🔐 Security Relevance
- Authentication controls access to domain resources.
- Attackers may target Kerberos tickets or NTLM authentication to gain unauthorized access.
- Understanding normal authentication makes it easier to understand Active Directory attacks later.

## 📌 Lessons Learned
💡 Windows domains primarily use Kerberos, while NTLM remains available for compatibility. 