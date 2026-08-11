# 🧪 Windows Performance Optimization 
Lab Type: Real-World System Maintenance    
Difficulty: Beginner / Intermediate  

## 🎯 Objective
- Investigate performance issues during normal Windows use.
- Identify unnecessary background processes, startup applications, and installed software.
- Reduce unnecessary resource usage and identify potential hardware limitations.

## 🖥️ Environment
**Device**
- HP OMEN Laptop

**Operating System**
- Windows 11 Home

**Processor**
- Intel Core i7-8750H
- 6 Cores / 12 Threads

**Graphics**
- NVIDIA GeForce GTX 1060

**Memory**
- 8 GB DDR4 2666 MHz
- Single Channel

## 🔍 Initial Assessment
During normal daily usage, the laptop felt slower than expected while multitasking.

Symptoms included:
- High memory usage
- Reduced responsiveness when switching between applications
- Multiple background applications running automatically at startup

Task Manager reported:

| Resource | Usage |
|----------|------:|
| CPU | ~20% |
| Memory | 85–90% |
| Disk | Low |
| Network | Idle |

Available memory averaged around **1 GB**, indicating that the system was approaching its physical memory limit.

## 📋 Investigation
### Running Processes
Task Manager identified several applications consuming memory.

Largest consumers included:
| Process | Approximate Usage |
|----------|------------------:|
| Firefox | ~1.9 GB |
| Bitdefender | ~250 MB |
| Microsoft Edge | ~95 MB |
| Steam WebHelper | ~86 MB |

The remaining memory usage was attributed to Windows services and background processes.

### Startup Applications
Startup applications were reviewed.

The following applications were identified as unnecessary during boot:

- Microsoft 365 Copilot
- Steam
- Mobile Devices
- HP Utilities
- Logitech Download Assistant
- Webex

These applications were disabled from startup to reduce boot time and background resource usage.

### Installed Applications
Installed software was reviewed through **Programs and Features**.

Applications identified for possible removal:
- HP Support Assistant
- HP Support Solutions Framework
- Bitdefender (replace with Microsoft Defender)

### Hardware Analysis
Memory analysis using CPUID CPU-Z confirmed:

| Property | Value |
|----------|-------|
| Installed RAM | 8 GB |
| Memory Type | DDR4 |
| Speed | 2666 MT/s |
| Configuration | Single Channel |
| Manufacturer | SK Hynix |
| Part Number | HMA81GS6CJR8N-VK |

One memory slot remained available. This indicated that the system could also benefit from a future memory upgrade.

## 🛠️ Optimization
### Software
- Disable unnecessary startup applications.
- Remove unused software.
- Replace Bitdefender with Microsoft Defender.
- Reduce background resource usage.

### Hardware
Upgrade memory:
**Before**

- 8 GB DDR4
- Single Channel

**After**

- 16 GB DDR4
- Dual Channel

## 🧰 Tools Used
- Task Manager
- CPUID CPU-Z
- System Information (msinfo32)
- Windows Settings
- Control Panel
- Startup Apps

## 💡 Lessons Learned
- Task Manager is an essential troubleshooting tool for identifying performance bottlenecks.
- The investigation demonstrated that the primary limitation of the system was insufficient physical memory rather than CPU performance. By combining software optimization with a planned RAM upgrade and cooling maintenance, the laptop can continue to provide strong performance for programming, cybersecurity labs, virtualization, and everyday productivity.

## 📸 Evidence
### Figure 1 – Task Manager (Processes)
Shows the applications consuming the most system memory during the investigation.

Firefox was identified as the primary memory consumer, followed by Visual Studio Code and Windows background services.

<div align="center">
  <img src="../../images/Task Manager (Processes).png" alt="Task Manager (Processes)" width="400"/>
</div>

---

### Figure 2 – Task Manager (Performance)
Shows the overall memory usage before optimization.

<div align="center">
  <img src="../../images/Task Manager (Performance).png" alt="Task Manager (Performance)" width="400"/>
</div>

---

### Figure 3 – CPU-Z (Memory)
Shows the installed memory configuration before the upgrade.

<div align="center">
  <img src="../../images/CPU-Z (Memory).png" alt="CPU-Z (Memory)" width="400"/>
</div>

---

### Figure 4 – CPU-Z (SPD)
Identifies the installed memory module used to purchase a compatible upgrade.

<div align="center">
  <img src="../../images/CPU-Z (SPD).png" alt="CPU-Z (SPD)" width="400"/>
</div>

---

### Future Evidence

### Figure 5 – Task Manager (Memory After Upgrade)
Shows the memory configuration after the RAM upgrade.

The system now detects **16 GB DDR4 at 2667 MT/s**, with **both memory slots populated**. Memory usage during normal operation is approximately **54%**, providing significantly more available memory for multitasking compared with the original 8 GB configuration.

<div align="center">
  <img src="../../images/Task Manager (Memory After Upgrade).png" alt="Task Manager (Performance)" width="400"/>
</div>