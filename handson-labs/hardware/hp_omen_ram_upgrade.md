# 🧪 RAM Upgrade
Lab Type: Real-World System Maintenance
Difficulty: Beginner / Intermediate

## 🎯 Objective
- Upgrade my HP OMEN laptop from 8 GB to 16 GB of RAM.
- Install a compatible second memory module and enable dual-channel operation.
- Verify that the upgraded memory is correctly detected and operating as expected.

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

## 📋 Investigation
Before purchasing the upgrade, I inspected the existing memory configuration using CPU-Z.

The laptop contained a single 8 GB DDR4-2666 SODIMM, leaving the second memory slot available.

The existing module specifications were used to select a compatible second 8 GB DDR4-2666 module.

## 🔧 Hardware Upgrade
### Original Memory
| Property      | Original Configuration |
| ------------- | ---------------------- |
| Capacity      | 8 GB                   |
| Type          | DDR4 SODIMM            |
| Speed         | 2666 MT/s              |
| Configuration | Single Channel         |
| Manufacturer  | SK Hynix               |
| Part Number   | HMA81GS6CJR8N-VK       |
| Slots Used    | 1 of 2                 |

### Upgraded Memory
A second compatible 8 GB DDR4-2666 SODIMM was installed in the available memory slot.

| Property       | Upgraded Configuration |
| -------------- | ---------------------- |
| Total Capacity | 16 GB                  |
| Type           | DDR4 SODIMM            |
| Speed          | 2666 MT/s              |
| Configuration  | Dual Channel           |
| Slots Used     | 2 of 2                 |
 
## 🔍 Compatibility & Verification
After installation, the laptop booted normally and Windows detected the full 16 GB of RAM.

Task Manager confirmed:
- 16 GB installed
- 15.9 GB usable
- 2667 MT/s memory speed
- 2 of 2 memory slots populated

HWiNFO was used to verify that the two memory modules were operating in dual-channel mode.

The laptop remained stable during normal use and gaming after the upgrade.

🧰 Tools Used
- Screwdriver set
- CPUID CPU-Z
- Windows Task Manager
- HWiNFO

💡 Lessons Learned
- Checking the existing RAM specifications before purchasing an upgrade helps ensure memory compatibility.
- Laptop memory modules should be matched by important characteristics such as DDR generation, form factor, capacity, and supported speed.
- Adding a second compatible module increased the available memory from 8 GB to 16 GB and enabled dual-channel operation.
- A successful boot is not enough to verify a RAM upgrade; the final capacity, speed, channel configuration, and system stability should also be checked.

## 📸 Evidence
### Figure 1 – CPU-Z (Memory Before Upgrade)

Shows the original 8 GB DDR4 memory operating in single-channel mode.
<div align="center">
  <img src="../../images/CPU-Z (Memory).png" alt="Task Manager (Processes)" width="400"/>
</div>

---

### Figure 2 – CPU-Z (SPD)

Shows the specifications of the original SK Hynix memory module used to identify a compatible upgrade.
<div align="center">
  <img src="../../images/CPU-Z (SPD).png" alt="Task Manager (Processes)" width="400"/>
</div>

---

### Figure 3 – Task Manager (Memory After Upgrade)

Shows 16 GB of installed memory running at approximately 2667 MT/s, with 2 of 2 memory slots used.

<div align="center">
  <img src="../../images/Task Manager (Memory After Upgrade).png" alt="Task Manager (Processes)" width="400"/>
</div>

---

### Figure 4 – HWiNFO (Dual-Channel Verification)

Confirms that the upgraded 16 GB DDR4-2666 memory configuration is operating in dual-channel mode.

<div align="center">
  <img src="../../images/HWiNFO RAM Upgrade.png" alt="Task Manager (Processes)" width="400"/>
</div>