# Web Fundamentals – TryHackMe and Solent University Cybersecurity Coursework 

Platform: TryHackMe   
Level: Beginner / Foundation  
Focus Area: DNS Record Types

## 🎯 Objective
- Understand different DNS record types  
- Learn how domains are linked to services (web, email, etc.)  
- Identify how DNS records are used in real-world systems  

## 🧠 Core Concepts Learned 
## DNS Record Types
- DNS records are standardized instructions stored in DNS servers that tell the system how to handle requests for a domain   
- Each record type defines how traffic should be routed for services such as websites, email, and verification systems  

### DNS Record Types
1. **A Record**  
- Maps a domain to an IPv4 address  
- Example: `example.com` → `93.184.216.34`  

2. **AAAA Record**  
- Maps a domain to an IPv6 address   
- Example: `example.com` → `2606:28000:220:1:248:1893:25c8:1946`   

3. **CNAME (CANONICAL NAME)**  
- Creates an alias from one domain to another  
- Example: `www.example.com` → `example.com`  

4. **MX (Mail Exchange) Record**
- Specifies the mail servers responsible for receiving emails for a domain  
- Example: `example.com` → `mail.example.com`  

5. **TXT Record**  
- Stores text-based (notes) information used for verification and security     
- Just hold information which other systems can read and trust your domain for specific purposes, like email or domain ownership verification  

## 🧪 TryHackMe Lab Example (DNS Queries)
- Used an online tool to build and analyse DNS queries and responses  

### Tasks Performed:
- Created DNS requests to resolve domain names into IP addresses  
- Observed how DNS servers respond with different record types  
- Analysed query results and the returned data  
- Reviewed equivalent commands that can be used on a local machine  

### Key Insight:
- Different DNS record types return different types of information (A, AAAA, MX)  
- DNS queries follow a structured request-response model 
- Tools such as `nslookup` or `dig` can be used to perform DNS queries from the command line 

## 🛠️ Practical Skills Developed
- Identified common DNS record types and their functions  
- Understood how domains are connected to web and email services  
- Recognised how DNS records support infrastructure and communication  

## 🧰 Tools Used 
- Solent University Cybersecurity Coursework 
- TryHackMe platform  
- Command Line Interface (CLI)
  - Windows Command Prompt (cmd)
  - Linux Terminal (bash)

## 🔐 Security Relevance
DNS records play a critical role in security and are often targeted or misconfigured.

- **Phishing attacks:** Fake domains may use misleading DNS records  
- **Email spoofing:** Incorrect records can allow attackers to send fraudulent emails  
- **Subdomain takeover:** Misconfigured CNAME records can be exploited  
- **DNS reconnaissance:** Attackers gather DNS records to map infrastructure  

## 📌 Lessons Learned  
⚠️ DNS records control how traffic is routed across the internet   
⚠️ Misconfigured records can lead to security vulnerabilities   
⚠️ Understanding DNS records helps identify misconfigurations and detect potential threats.  
⚠️ Understanding DNS records is essential for analysing real-world network behaviour       