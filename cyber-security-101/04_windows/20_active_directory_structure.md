# Windows – TryHackMe

Platform: TryHackMe     
Skill Level: Beginner / Foundation     
Focus Area: Active Directory Structure

## 🎯 Objective
- Understand how Active Directory can support large organizations.
- Learn the difference between domains, trees, and forests.
- Understand how trust relationships allow access between domains.

## 🧠 Core Concepts Learned
As companies grow, so do their networks. 
A single domain may not always be enough. Active Directory allows multiple domains to be organized into **trees** and **forests**.  

A simple way to think about the structure is:  
```text
Forest
  ↓
Tree
  ↓
Domain
```

## Trees
A **tree** is a collection of related domains that share the same hierarchical namespace.

For example, different countries may have:
- Different laws and security requirements.
- Different Group Policies (GPOs).
- Separate IT teams responsible for their own resources.

An organization could create separate child domains for each country:
```text
company.com
│
├── uk.company.com
└── us.company.com
```

- `company.com` is the main domain.
- `uk.company.com` and `us.company.com` are child domains.
- Together, they form a **tree**.

## Forests
The union of several trees with different namespaces into the same network is known as a **forest**.

For example, when two companies merge:
```text
Forest
│
├── company.com
│   ├── uk.company.com
│   └── us.company.com
│
└── anothercompany.com
```

## Trust Relationships
A **trust** is a relationship that allows users from one domain to be authenticated when accessing resources in another domain.

For example:
```text
Domain A
   │
   │ Trust
   ↓
Domain B
   │
   ↓
Shared Resource
```

A trust does **not automatically give access** to resources. The user must still have the appropriate permissions.

### Direction of Trust
Trusts can be:
- **One-way** – One domain trusts another domain.
- **Two-way** – Both domains trust each other.

Example:
```text
One-way:
Domain A → Domain B

Two-way:
Domain A ←→ Domain B
```

## 🛠️ Practical Skills Developed
- Identified domains, trees, and forests.
- Understood how multiple domains can be organized.
- Learned the basic purpose of trust relationships.
- Recognized the difference between one-way and two-way trusts.

## 🧰 Tools Used
- TryHackMe platform

## 🔐 Security Relevance
- Trust relationships can allow access between different domains.
- A compromised account may affect other connected domains depending on the trust and permissions in place.
- Understanding the AD structure helps identify how access can extend across a large organization.

## 📌 Lessons Learned
💡 **Tree = Related domains with a shared namespace.**  
💡 **Forest = One or more Active Directory trees.**  
💡 **A forest is the highest-level logical structure in Active Directory.**  
💡 **Trust = Allows authentication between domains.**  
💡 **Active Directory can organize large environments using domains, trees, forests, and trusts.**     