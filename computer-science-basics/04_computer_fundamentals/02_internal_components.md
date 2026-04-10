# Computer Fundamentals - TryHackMe and Solent University Cybersecurity Coursework 

Platform: TryHackMe  
Skill Level: Beginner / Foundation   
Focus Area: Internal Components

## 🎯 Objective
- Understand the main internal components of a computer system
- Identify the role of each component and how they interact
- Recognise how hardware design impacts performance and security

## 🧠 Core Concepts Learned 

## Internal Components
- A computer system is made up of multiple internal components that work together to process, store, and manage data.

💡 These components do not work independently — they constantly communicate to execute tasks efficiently.

## Central Processing Unit (CPU)
- The “brain” of the computer responsible for executing instructions
- Performs calculations and logical operations  

**Key characteristics:**
- **Cores**
    - Physical processing units inside the CPU
    - More cores allow more tasks to run in parallel

- **Threads**
    - A virtual execution path inside a CPU core
    - Allows a single core to handle multiple tasks
    - Typically 2 threads per core using technologies like Simultaneous Multithreading (SMT - AMD) or Hyper-Threading (Intel)

 💡While a task is waiting to be completed, the same core can run another task   

- **Clock speed (GHz)**
    - Number of cycles the CPU can perform per second  
    - Higher GHz generally means faster instruction execution 

- **Architecture**
    - The design model of the CPU 
    - Can determine performance, power efficiency 

- **Efficiency**
    - Performance per watt of power used
    - Important for mobile devices and data centres 

## Motherboard
- The main circuit board that connects all components
- Enables communication between CPU, RAM, storage, and peripherals
- Acts as the backbone of the system  

**Key characteristics:**
- **Chipset**
    - The control hub of the motherboard
    - Determines supported features such as CPU compatibility, number of USB ports, and storage options  

- **Socket Type**
    - The physical interface where the CPU is installed  
    - Defines which processors are compatible with the motherboard

- **Expansion Slots**
    - Slots used to add additional components  
    - Examples: GPU, network cards, sound cards  

- **Connectivity**
    - Interfaces that allow the system to communicate with external devices  
    - Includes: USB ports, Ethernet, Bluetooth, Wi-Fi, audio ports, and display outputs  

💡 The motherboard plays a critical role in system compatibility and upgrade potential

## Power Supply Unit (PSU)
- Converts electrical power from the outlet into stable, usable energy
- Distributes power to all internal components
- Critical for system stability and hardware protection  

**Key characteristics:**
- **Wattage**
    - The total amount of power the PSU can supply to all components
    - Must be sufficient to support all system components 
    - Higher wattage allows for future upgrades and expansion

- **Efficiency Rating**
    - Measures how much input power is actually delivered vs wasted as heat
    - Higher efficiency reduces energy waste and heat generation 

- **Reliability**
    - The ability to deliver stable and consistent power over time 
    - Affects system stability, other components lifespan, and protection against power spikes or drops

💡 An unreliable PSU can cause system crashes, data corruption, or even hardware damage

## Graphics Processing Unit (GPU)
- Responsible for rendering images, video, and graphics  
- Designed for parallel processing (performing many calculations simultaneously)  
- Widely used in gaming, video editing, and AI workloads  

**Key characteristics:**
- **VRAM (Video Memory)**
    - Dedicated memory used by the GPU to store textures, frames, and graphical data  
    - More VRAM improves performance in high-resolution and complex graphical tasks 

- **Processing Power**
    - The GPU’s ability to process data in parallel
    - Determines performance in gaming, video editing, AI and computing tasks

- **Efficiency**
    - Performance per watt of power consumed
    - Higher efficiency reduces heat output, power usage, and cooling requirements

- **Workload Type**
    - The intended use of the GPU (gaming, workstation)

💡 GPUs are increasingly used beyond graphics, especially in AI and data processing due to their ability to handle parallel workloads efficiently

## Random Access Memory (RAM)
- Temporary (volatile) memory used to store data for active programs
- Provides fast access to data required by the CPU  
- Data is lost when the system is powered off 

**Key characteristics:**
- **Capacity (GB)**
    - The amount of data that can be stored in active memory  
    - More RAM allows more applications and processes to run simultaneously without performance loss  

- **Speed (MHz)**
    - How quickly data can be read from or written to memory  
    - Higher speed improves data transfer between RAM and CPU  

- **Latency (CL)**
    - How long it takes for RAM to respond to a request
    - Lower latency results in faster response times 

- **Generation (DDR4 or DDR5)**
    - The version of RAM technology  
    - Newer generations offer better performance, efficiency, and bandwidth  
 
💡 RAM acts as a bridge between the CPU and storage, allowing fast access to frequently used data

## Storage (HDD / SSD)
- Permanent (non-volatile) storage for data and operating systems

### **HDD (Hard Disk Drive)**
- Uses spinning magnetic disks to store data  
- Slower but cheaper compared to SSDs  
- Typically uses SATA interface

### **SSD (Solid State Drive)**
- Uses flash memory with no moving parts  
- Faster, more reliable, and energy-efficient  
- Can use SATA or NVMe interface  

💡 NVMe (Non-Volatile Memory Express) is a modern interface that provides significantly faster data transfer speeds than SATA  

**Key characteristics:**
- **Capacity (GB/TB)**
    - The amount of data that can be stored  

- **Speed**
    - How quickly data can be read or written  
    - NVMe SSDs are significantly faster than SATA SSDs and HDDs 

- **Reliability**
    - How dependable is the drive over time

- **Endurance**
    - The number of write cycles the device can handle before wearing out  

💡 Storage is critical for both performance and security, as it holds operating systems, applications, and sensitive user data

## Cooling System 
- Maintains safe operating temperatures for internal components  
- Prevents overheating, which can reduce performance or damage hardware 

**Key characteristics:**
- **Airflow**
    - How effectively air moves through the case and over the components
    - Proper airflow improves cooling efficiency and system stability

- **Cooling Capacity**
    - The amount of heat the system can dissipate  
    - Higher capacity keeps components cooler under heavy workloads  

- **Noise Level**
    - The amount of sound produced during operation  
    - Depends on fan speed and cooling design  

- **Cooling Type**
    - The method used to remove heat from components  
    - Examples:
        - Air cooling (fans and heat sinks)  
        - Liquid cooling (more efficient, used in high-performance systems)

## How Components Work Together
- A simple data flow inside a system:

1. Data is loaded from storage
2. Sent to RAM for quick access
3. CPU processes the data
4. Results may be:
    - Displayed via GPU on the desktop screen
    - Stored back in storage

💡 Efficient communication between components is essential for system performance

## 🛠️ Practical Skills Developed
- Identified core internal components and their functions
- Understood how hardware components interact
- Connected system architecture to real-world performance

## 🧰 Tools Used
- Solent University Cybersecurity Coursework
- TryHackMe platform
- Task Manager (system monitoring)

## 🔐 Security Relevance
- Hardware components can be targeted by low-level attacks (firmware or memory attacks)
- Storage devices may contain unencrypted or recoverable data
- The CPU and motherboard firmware can be targeted by advanced malware
- Sensitive data stored in RAM can be extracted through memory-based attacks while the system is running
- Data stored on drives can often be recovered if not properly encrypted or securely erased

💡 Understanding internal components helps identify where attacks can occur within a system

## 📌 Lessons Learned
⚠️ A computer system is not a single unit — it is a collection of components working together  
⚠️ Performance depends not only on individual components, but on how efficiently they interact  
⚠️ Understanding internal architecture is essential for analysing system behaviour and security risks  
⚠️ Heat is one of the biggest enemies of a computer system, affecting performance, stability, and hardware lifespan  

