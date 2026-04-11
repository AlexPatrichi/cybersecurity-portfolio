# Computer Fundamentals - TryHackMe and Solent University Cybersecurity Coursework 

Platform: TryHackMe  
Skill Level: Beginner / Foundation  
Focus Area: System Boot Process  

## 🎯 Objective
- Understand the steps involved when a computer starts up  
- Learn how firmware, the bootloader, and the operating system work together  
- Recognise the importance of the boot process in system functionality and security  

## 🧠 Core Concepts Learned

## System Boot Process
- The boot process is the sequence of steps a computer follows when it is powered on  
- It prepares the hardware, checks system components, and loads the operating system into memory  

### Main Stages of the Boot Process

#### 1. Power On
- A signal is sent to the PSU, allowing power to flow to the motherboard and all connected components  

#### 2. Firmware Initialisation
- The system firmware starts running, takes control and begins the startup process
    - **BIOS (Basic Input/Output System)** - legacy firmware
    - **UEFI (Unified Extensible Firmware Interface)** - modern firmware  
- Prepares hardware components such as the CPU, memory, keyboard, and storage devices  

#### 3. POST (Power-On Self-Test) & Hardware Initialization
- The firmware performs diagnostic checks on essential hardware  
- Ensures essential components are present, correctly configured, and functional before the system continues booting  
- Initializes CPU, memory, and basic system devices required for booting

#### 4. Boot Device Selection
- The firmware follows its boot order list and looks to locate a valid **bootloader** on the configured storage device (SSD, HDD, USB) 
- It locates and loads the bootloader, which is responsible for starting the operating system

#### 5. Bootloader Execution
- The bootloader is loaded into memory 
- It loads the operating system kernel from the storage device into RAM

💡Bootloader is a small startup program that loads the OS kernel into RAM and starts its execution

#### 6. Operating System Handover
- Control of the system is transferred from firmware to the operating system
- The OS initializes drivers, services, and system processes  

#### 7. User Interface Launch
- Once startup is complete, the OS loads the graphical user interface (GUI)
- The system is ready for user interaction 

### BIOS vs UEFI Comparison
<div align="center">

<table>
  <tr>
    <th>Feature</th>
    <th>BIOS (Legacy)</th>
    <th>UEFI (Modern)</th>
  </tr>
  <tr>
    <td>Full Name</td>
    <td>Basic Input/Output System</td>
    <td>Unified Extensible Firmware Interface</td>
  </tr>
  <tr>
    <td>Interface</td>
    <td>Text-based</td>
    <td>Graphical (GUI) support</td>
  </tr>
  <tr>
    <td>Boot Speed</td>
    <td>Slower</td>
    <td>Faster</td>
  </tr>
  <tr>
    <td>Disk Support</td>
    <td>Up to 2 TB (MBR)</td>
    <td>Supports large disks (GPT, &gt;2 TB)</td>
  </tr>
  <tr>
    <td>Security</td>
    <td>Limited</td>
    <td>Supports Secure Boot</td>
  </tr>
  <tr>
    <td>Flexibility</td>
    <td>Fixed and limited</td>
    <td>More configurable and extensible</td>
  </tr>
  <tr>
    <td>Boot Process</td>
    <td>Simpler, sequential</td>
    <td>More advanced and efficient</td>
  </tr>
</table>

</div>

💡 Modern systems use UEFI due to better performance, improved security (Secure Boot), and support for larger storage devices

## 🛠️ Practical Skills Developed
- Identifying the stages of the computer boot process  
- Understanding the difference between BIOS and UEFI  
- Recognising the role of POST in hardware checks  
- Explaining how the operating system is loaded after startup  

## 🧰 Tools Used
- Solent University Cybersecurity Coursework
- TryHackMe platform

## 🔐 Security Relevance
- The boot process is a key target for attackers because it happens before the operating system fully loads  
- Secure Boot helps prevent unauthorised or malicious software from loading during startup  
- Understanding the boot process helps identify threats such as bootkits or firmware-level attacks  

## 📌 Lessons Learned
⚠️ A computer does not load the operating system immediately, it follows a structured startup process that checks hardware and hands control over in stages  
⚠️ Each stage has a specific role, from hardware checks to loading and handing control to the operating system  