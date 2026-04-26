# Search Skills – TryHackMe and Solent University Cybersecurity Coursework 

Platform: TryHackMe    
Skill Level: Beginner / Foundation  
Focus Area: Specialized Search Engines

## 🎯 Objective 
- Understand how specialised search engines are used in cybersecurity  
- Learn how to gather intelligence on devices, domains, and files  
- Apply search tools to support investigations and threat analysis  

## 🧠 Core Concepts Learned   

- Specialised search engines are used to find specific types of results (devices, files, breaches)   
- They provide deeper insights than traditional search engines  
- These tools are widely used in OSINT and cybersecurity investigations 

### VirusTotal
- One of the most commonly used tools in cybersecurity  
- Analyses files, URLs, and hashes using multiple antivirus engines
- Provides detection results and community insights

💡 Example: Check if a suspicious file or domain has been flagged as malicious

### Have I Been Pwned
- Checks if an email address appears in known data breaches

💡 Example: Verify if user credentials may have been exposed

### Shodan 
- A search engine for Internet-connected devices (servers, routers, IoT devices)
- Instead of searching pages, it finds real machines connected to the internet
- Allows filtering by location, service, and software version

💡 Example: Identify outdated systems (exposed services running legacy software)

### Censys
- Focuses on internet-wide scanning data, including hosts, certificates, and services
- Similar to Shodan, but more focused on data analysis and structure
- It’s used more by researchers and professionals
- Useful for analysing exposed infrastructure and network assets

💡 Example: Discover all servers using a certain certificate

### GreyNoise
- Identifies whether an IP address is part of background internet noise or real malicious activity  

💡 Example: Determine if repeated traffic from an IP is a real threat or false alarms

### URLScan.io
- Analyses websites safely in a controlled environment  

💡 Example: Investigate a suspicious link without directly visiting it  


### Hybrid Analysis
- Runs files in a sandbox to observe real behaviour  

💡 Example: Analyse what a suspicious file does when executed  

### SecurityTrails
- Tracks domain history, DNS records, ownership

💡 Example: Investigate domain ownership and infrastructure changes  

## 🛠️ Practical Skills Developed
- Checking files and domains for malicious activity  
- Identifying exposed systems and services  
- Verifying potential data breaches  
- Analysing suspicious links safely    

## 🧰 Tools Used 
- TryHackMe platform 
- Solent University Cybersecurity Coursework 
- Mozilla Firefox (research and validation)  
    
## 🔐 Security Relevance
- Helps identify exposed systems and misconfigurations  
- Supports threat intelligence and incident investigations  
- Enables quick validation of suspicious files, domains, and credentials  

## 📌 Lessons Learned 
⚠️ Specialised tools provide powerful insights, but results must always be verified   
⚠️ Not all flagged results are malicious — context and analysis are essential   
⚠️ Combining multiple tools gives a more accurate picture of potential threats   
