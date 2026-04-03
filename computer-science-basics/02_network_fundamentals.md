# Network Fundamentals – TryHackMe and Solent University 

Platform: TryHackMe   
Date Started: 31.01.2026  
Level:  Beginner / Foundation  
Focus Area: Networking for Cybersecurity  

## Objective

Build a strong foundation in networking concepts required for cybersecurity, including:  
- How devices communicate over networks  
- How data moves between systems  
- Core protocols and services  
- Network structures and security relevance  

## Core Concepts Learned  
### 🌐 Network Fundamentals 
A network is **two or more devices connected** so they can share data.    
Example: Phone → PC → Router → Internet  

---

### Network Devices and Their Attributes
- **Devices (PC, Phone, Server)**  
  - Send and receive data  

- **Switch**  
  - Connects devices within the same network  

- **Router**  
  - Routes traffic between different networks (e.g. home → internet)  

- **Modem**  
  - Connects the router to the Internet Service Provider (ISP)  

- **Firewall**  
  - Filters incoming and outgoing traffic based on rules  

- **IDS/IPS**  
  - IDS: Detects malicious activity  
  - IPS: Detects and blocks malicious traffic  

- **Access Point**  
  - Provides wireless (Wi-Fi) connectivity 

---

### The Internet
- It is one large public network made up of many smaller private networks.
- To communicate and maintain order, devices must be both identifying and identifiable on a network. 
- Exactly like humans (name and fingerprint), devices are identified using:
  - **IP Address** → logical identity  
  - **MAC Address** → physical identity  

---

### IP Address (Internet Protocol Address)
- Every device gets an IP Address so data knows where to go.  
    Example:   
    - Device (PC): 192.168.1.10
    - Router:      192.168.1.1
- Can be used to identify a host on a network for a period of time.

<p align="center">
<strong>IP Address</strong><br>

<table align="center">
  <tr>
    <td align="center"><strong>192</strong></td>
    <td align="center"><strong>168</strong></td>
    <td align="center"><strong>1</strong></td>
    <td align="center"><strong>1</strong></td>
  </tr>
  <tr>
    <td align="center">Octet 1</td>
    <td align="center">Octet 2</td>
    <td align="center">Octet 3</td>
    <td align="center">Octet 4</td>
  </tr>
  <tr>
    <td align="center">0–255</td>
    <td align="center">0–255</td>
    <td align="center">0–255</td>
    <td align="center">0–255</td>
  </tr>
</table>

</p>

- The value of each octet (0 - 255) is calculated through a techinque known as IP addressing & subnetting. 
- IP addresses can change over time (dynamic allocation)
- IP Addresses can change from device to device, but cannot be active simulaneously more than once within same network. 
- IP addresses follow a set of standards known as protocols, allowing all devices to communicate using the same rules. 

--- 

### **Public vs Private IP Addresses**
Devices can be on both private and public networks, so they can get a public or a private IP Address.

#### Public IP Address
 - Assigned by your Internet Service Provider (ISP)
 - The router has the Public IP Address of the network
 - Used to identify your network on the internet
 - Must be unique globally

#### Private IP Address
 - Used inside local networks to identify devices
 - Not directly accessible from the internet
 - Can be reused across different networks

---

### **IPv4 and Ipv6** 

<div align="center">
<table>
  <tr>
    <th>Feature</th>
    <th>IPv4</th>
    <th>IPv6</th>
  </tr>
  <tr>
    <td>Address Size</td>
    <td>32-bit</td>
    <td>128-bit</td>
  </tr>
  <tr>
    <td>Format</td>
    <td>Decimal (e.g. 192.168.1.1)</td>
    <td>Hexadecimal (e.g. 2001:0db8::1)</td>
  </tr>
  <tr>
    <td>Total Addresses</td>
    <td>~4.3 billion</td>
    <td>~340 undecillion</td>
  </tr>
  <tr>
    <td>Structure</td>
    <td>4 octets</td>
    <td>8 groups</td>
  </tr>
  <tr>
    <td>Usage</td>
    <td>Most common today</td>
    <td>Growing adoption</td>
  </tr>
  <tr>
    <td>Security</td>
    <td>Optional</td>
    <td>Built-in (IPSec support)</td>
  </tr>
  <tr>
    <td>Limitation</td>
    <td>Limited address space</td>
    <td>Designed for scalability</td>
  </tr>
  <tr>
    <td>Routing</td>
    <td>Less efficient</td>
    <td>More efficient</td>
  </tr>
  <tr>
    <td>NAT</td>
    <td>Yes</td>
    <td>No</td>
  </tr>
</table>

</div>

---

### **NAT (Network Address Translation)**
- It is a mechanism that allows multiple devices to share one public IP Addresses.
- It made modern home internet possible as we know it; without it, the IPv4 internet would have collapsed long time ago.
- Works very well with IPv4 because allows multiple private devices to share one single public IP by translating internal addresses to external ones. 
- It hides devices, creating a false sense of security, but is not real protection.

#### **Types of NAT** 
1. SNAT (Source NAT) 
 - Internal → External  
 - Changes the **source IP** of outgoing traffic 
 - Your private IP Address becomes the router's public IP Address. 

2. DNAT (Destination NAT) 
 - External → Internal  
 - Changes the **destination IP** of incoming traffic   
 - Used for **port forwarding** (e.g. accessing CCTV remotely)  

3. PAT (Port Address Translation)
 - Used by most home routers  
 - Allows multiple devices to share one public IP Address using **different ports**  

#### **How they work together?**  
Your home router typically uses:

- **SNAT** → when traffic goes out to the internet  
- **PAT** → to keep track of multiple devices using one public IP  
- **DNAT** → when port forwarding is configured  

Example:
1. Your PC (192.168.1.10) sends a request to a website  
2. Router applies **SNAT + PAT** → replaces your IP with public IP + assigns a port  
3. Response comes back to router  
4. Router uses the port to send data back to the correct device 

#### **How PAT works?**
- Each device is assigned a **unique port number** when sending traffic  
- Router keeps a **translation table**:

<div align="center">

<table>
  <tr>
    <th>Private IP</th>
    <th>Private Port</th>
    <th>Public IP</th>
    <th>Public Port</th>
  </tr>
  <tr>
    <td>192.168.1.10</td>
    <td>1234</td>
    <td>203.0.113.1</td>
    <td>50001</td>
  </tr>
  <tr>
    <td>192.168.1.11</td>
    <td>5678</td>
    <td>203.0.113.1</td>
    <td>50002</td>
  </tr>
</table>

</div>

This allows:
- Many devices → one public IP  
- Router to know exactly where to send responses  

#### Important Notes
⚠️ Most home and small-business routers use **PAT + SNAT by default**.    
⚠️ **DNAT** is used to allow external users to access internal network services. 
(Example: CCTV system when you are on vacation)

---

### MAC Address (Media Access Control Address)
- A MAC address is assigned to a network interface card (NIC), which is typically built into the device motherboard. 
- It is a 12-character hexadecimal value (48 bits), written as 6 pairs separated by colons.
   - **Part A (first 3 bytes)** → Organizationally Unique Identifier (OUI), identifies the manufacturer (Intel).
   - **Part B (last 3 bytes)** → Unique identifier assigned to the specific device.
- MAC Addresses are used for LAN communication and do not travel across the internet.
   - They only exist inside the local network. 
   - Once traffic hits the router, MAC Adreesses are replaced.
- Operates at **Layer 2 (Data Link layer)** of the OSI model

<div align="center">

<strong>MAC Address</strong><br>

<table align="center">
  <tr>
    <td colspan="3" align="center"><strong>Part A (OUI)</strong></td>
    <td colspan="3" align="center"><strong>Part B (Device ID)</strong></td>
  </tr>
  <tr>
    <td align="center"><strong>a4</strong></td>
    <td align="center"><strong>c3</strong></td>
    <td align="center"><strong>f0</strong></td>
    <td align="center"><strong>85</strong></td>
    <td align="center"><strong>ac</strong></td>
    <td align="center"><strong>2d</strong></td>
  </tr>
</table>

</div>

#### Important Notes
⚠️ MAC Addresses can be facked or "spoofed" in a proccess known as **SPOOFING**.
It occurs when a network device pretends to identify as another using its MAC Address.

--- 
### 📡 Internet Control Message Protocol (ICMP)

- A protocol used by network devices to send **error messages and operational information**
- Helps diagnose network issues and check connectivity
- Works alongside IP, but does not carry user data
- ICMP operates at Layer 3 (Network layer) of the OSI model
- Common ICMP messages include "Echo Request" and "Echo Reply" (used by ping)

#### Network Diagnostic Tools
**ping** 
- One of the most fundamental network tools available
- Uses ICMP packets to check if a device is reachable and how reliable the connection is
- Measures latency (response time)
- Can indicate packet loss (network instability)
- It works on devices on the network, or resources like websites

⚠️ May be blocked by firewalls, so failure does not always mean the host is down  

**ipconfig (Windows) / ifconfig (Linux or macOs)**
- Shows your network configuration (IP address, subnet mask, gateway)  
- Helps identify network misconfigurations  
- Useful for troubleshooting connectivity issues 

**tracert (Windows) / traceroute (Linux or macOs)** 
- Shows the path packets take through the network  
- Helps identify where delays or failures occur  
- Useful for diagnosing routing problems  

⚠️ Uses ICMP (or UDP depending on implementation)  

**nslookup**
- Queries DNS servers to resolve domain names to IP addresses  
- Helps detect DNS issues or misconfigurations  
- Useful for identifying suspicious or malicious domains  
- Very useful for security investigations

**netstat**
- Shows active network connections and listening ports  
- Helps identify unusual or suspicious connections  

⚠️ Useful for detecting malware communication, backdoors, and exposed services

**arp**
- Displays the mapping between IP addresses and MAC addresses  
- Used to identify devices on the local network  

⚠️ Useful for detecting ARP spoofing attacks and identifying unknown devices 

---



## Practical Skills Developed   
1. Understanding traffic flow between systems  
2. Reading basic network diagrams  
3. Recognizing normal vs abnormal traffic behavior  
4. Identifying attack surfaces in network design  
5. Understanding how attacks move across networks  

## Tools Used  

- TryHackMe platform 
- Browser developer tools  
- Command-line tools:  
    - ping  
    - ipconfig / ifconfig  
    - tracert / traceroute  
    - nslookup  
    - netstat  

## Security Relevance  

- Network devices are key points for monitoring and defence  
- Firewalls and IDS/IPS help detect and prevent attacks  
- Understanding network flow is essential for analysing traffic and incidents  

## Lessons Learned  

- Every cyber attack moves through a network  
- Logs and alerts are meaningless without network context  
- Network visibility = security visibility  
- Strong network fundamentals increase effectiveness in any cybersecurity role  