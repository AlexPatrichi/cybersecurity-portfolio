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

### 🔌 Network Devices and Their Attributes
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

### 🌍 The Internet
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
<strong>IP Address</strong><br><br>

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

#### **Public vs Private IP Addresses**
Devices can be on both private and public networks, so they can get a public or a private IP Address.

- Public IP Address
 - Assigned by your Internet Service Provider (ISP)
 - The router has the Public IP Address of the network
 - Used to identify your network on the internet
 - Must be unique globally

- Private IP Address
 - Used inside local networks to identify devices
 - Not directly accessible from the internet
 - Can be reused across different networks

---

#### **IPv4 and Ipv6** 

| Feature | IPv4 | IPv6 |
|--------|------|------|
| Address Size | 32-bit | 128-bit |
| Format | Decimal (e.g. 192.168.1.1) | Hexadecimal (e.g. 2001:0db8::1) |
| Total Addresses | ~4.3 billion | ~340 undecillion |
| Structure | 4 octets | 8 groups |
| Usage | Most common today | Growing adoption |
| Security | Optional | Built-in (IPSec support) |
| Limitation | Running out of addresses | Designed for scalability |
| Efficiency | Less efficient routing | More efficient routing |
| NAT | Yes | No |

---

#### **NAT (Network Address Translation)**
- It is a mechanism that allows multiple devices to share one public IP Addresses.
- It made modern home internet possible as we know it; without it, the IPv4 internet would have collapsed long time ago.
- Works very well with IPv4 because allows multiple private devices to share one single public IP by translating internal addresses to external ones. 
- It hides devices, creating a false sense of security, but is not real protection.

**Types of NAT** 
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

**How they work together?**  
Your home router typically uses:

- **SNAT** → when traffic goes out to the internet  
- **PAT** → to keep track of multiple devices using one public IP  
- **DNAT** → when port forwarding is configured  

Example:
1. Your PC (192.168.1.10) sends a request to a website  
2. Router applies **SNAT + PAT** → replaces your IP with public IP + assigns a port  
3. Response comes back to router  
4. Router uses the port to send data back to the correct device 

**How PAT works?**
- Each device is assigned a **unique port number** when sending traffic  
- Router keeps a **translation table**:

| Private IP | Private Port | Public IP | Public Port |
|-----------|-------------|-----------|-------------|
| 192.168.1.10 | 1234 | 203.0.113.1 | 50001 |
| 192.168.1.11 | 5678 | 203.0.113.1 | 50002 |

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

<p align="center">
<strong>MAC Address</strong><br><br>

<table>
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

</p>

#### Important Notes
⚠️ MAC Addresses can be facked or "spoofed" in a proccess known as **SPOOFING**.
It occurs when a network device pretends to identify as another using its MAC Address.

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