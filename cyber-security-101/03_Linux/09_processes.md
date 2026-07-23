# Linux – TryHackMe 

Platform: TryHackMe    
Skill Level: Beginner / Foundation  
Focus Area: Processes 101

## 🎯 Objective 
- Understand how Linux processes work.
- Learn how to view and manage running processes.
- Understand how processes are started and controlled by the operating system.
- Learn the difference between foreground and background processes.

## 🧠 Core Concepts Learned   
## Processes 
- Processes are the programs that are currently running and are managed by the Linux kernel.
- Each process is assigned a unique Process ID (PID).
- New processes are typically assigned the next available PID. After a process terminates, its PID may be reused by the operating system.

## Viewing Processes 
`ps command`
- Displays a list of the running processes plus some additional information such as status code, running session etc
- In order to see the processes run by other users we need to use `ps aux` command.

`top command`
- Displays running processes in real time.
- Shows useful information such as: CPU usage, Memory usage, Running time, Process status.

## Managing Processes 
- The `kill command` sends signals to a running process.
- These signals can terminate, stop, or control the behaviour of a process.
(exp: kill command + associated PID that we wish to kill).
- Common signals: 
    - `SIGTERM (15)` – Gracefully terminates a process, allowing it to perform cleanup tasks before exiting.
    - `SIGKILL (9)` – Immediately terminates a process without allowing cleanup.
    - `SIGSTOP (19)` – Suspends a running process until it is resumed.

## How Processes Start 
- During system boot, the Linux kernel starts the first userspace process.
- On most modern Linux distributions, this process is `systemd`, which usually has a PID of 1.
- Most other processes are created as `child processes` of `systemd`.
- The operating system uses `namespaces` to isolate processes and their resources.
- Process isolation improves security by preventing processes from unnecessarily interacting with one another.

## Starting Services at Boot (Getting Processes)
- Linux uses service managers such as `systemd` to automatically start services during boot.
- Services can be managed using the `systemctl command`.
- Examples:
    - `systemctl`[option][service]
    - `systemctl start nginx`
    - `systemctl stop nginx`
    - `systemctl enable nginx`
    - `systemctl disable nginx`

## Background and Foreground in Linux
- Processes can run in two states: **foreground** or **background**.
- Foreground processes occupy the current terminal until they finish.
- Background processes continue running while allowing you to use the terminal.
- Useful commands: 
    - `Ctrl + Z` - Suspend the current process
    - `bg` - Resume a suspended process in the background
    - `fg` - Bring a background process back to the foreground

## 🛠️ Practical Skills Developed
- Viewing running processes using ps and top.
- Identifying processes by their Process ID (PID).
- Managing running processes using the kill command.
- Understanding how Linux starts and manages processes.
- Working with foreground and background processes.

## 🧰 Tools Used 
- TryHackMe platform 
- Linux Terminal

## 🔐 Security Relevance
- Monitoring running processes helps identify suspicious or malicious activity.
- Security analysts regularly inspect running processes during incident response investigations.
- Understanding process management is essential for troubleshooting Linux systems and terminating unwanted or compromised processes.
- Reviewing services that start automatically helps reduce a system's attack surface.

## 📌 Lessons Learned 
💡Every running program is represented as a process with a unique PID.    
💡Linux provides several tools for monitoring and managing processes.    
💡Signals such as `SIGTERM` and `SIGKILL` allow administrators to control running processes.  
💡Most user processes are started and managed by `systemd`.  
💡Understanding foreground and background processes improves efficiency when working in the Linux terminal.   