# Windows – TryHackMe

Platform: TryHackMe     
Skill Level: Beginner / Foundation     
Focus Area: Resource Monitor (`resmon`)  

## 🎯 Objective
- Understand the purpose of Resource Monitor.
- Learn how to monitor CPU, memory, disk, and network activity in real time.
- Identify processes that are consuming system resources.
- Understand how Resource Monitor assists with troubleshooting and performance analysis.

## 🧠 Core Concepts Learned
## What is Resource Monitor?
**Resource Monitor (`resmon`)** is a Windows utility that provides detailed, real-time information about how system resources are being used.

## Task Manager vs Resource Monitor
- Task Manager → Quick overview of running applications and resource usage.
- Resource Monitor → Detailed analysis of CPU, memory, disk, and network activity, including which processes are responsible.

## Resource Categories
Resource Monitor is divided into four primary sections:

### → CPU
Displays processor usage, including:
- Running processes
- Services associated with each process
- CPU utilization
- Process IDs (PIDs)
- Threads and handles

Useful for identifying processes causing high CPU usage.

### → Memory
Displays memory usage, including:
- Processes using RAM
- Physical memory allocation
- Hard faults per second
- Available and used memory

Useful for diagnosing memory bottlenecks and excessive RAM consumption.

### → Disk
Displays disk activity, including:
- Processes reading and writing files
- Disk response time
- Read and write speeds
- Files currently being accessed

Useful for identifying applications causing heavy disk usage.

### → Network
Displays network activity, including:
- Active network connections
- Listening ports
- Network utilization
- Processes generating network traffic

Useful for identifying applications communicating over the network.

## Filtering
One of **Resource Monitor's** most useful features is its ability to filter information by selecting a specific process.

When a process is selected, the CPU, Memory, Disk, and Network tabs display only the resources associated with that process, making troubleshooting much easier.

## 🛠️ Practical Skills Developed
- Opened Resource Monitor (`resmon`).
- Monitored CPU utilization.
- Examined memory usage.
- Reviewed disk activity.
- Observed active network connections.
- Identified resource-intensive processes.
- Filtered resource usage by individual process.

## 🧰 Tools Used
- TryHackMe platform
- Resource Monitor (`resmon`)

## 🔐 Security Relevance
**Resource Monitor** is useful during troubleshooting and security investigations because it provides detailed insight into process activity.

It can help analysts:
- Detect processes consuming excessive CPU or memory.
- Identify unexpected disk activity.
- Monitor network connections established by running processes.
- Correlate resource usage with suspicious applications.
- Investigate abnormal system behavior that may indicate malware.

## 📌 Lessons Learned
💡 **Resource Monitor** provides a detailed, real-time view of CPU, memory, disk, and network usage. It is an effective troubleshooting tool for identifying resource bottlenecks and investigating suspicious process activity.