# Windows – TryHackMe

Platform: TryHackMe     
Skill Level: Beginner / Foundation     
Focus Area: Windows Command Line

## 🎯 Objective
- Understand the purpose and advantages of the Windows Command Line.
- Learn basic commands for viewing system information.
- Check and troubleshoot network configuration.
- Navigate directories and manage files from the command line.
- View and terminate running processes.
- Learn how command-line tools can support system administration and cybersecurity tasks.

## 🧠 Core Concepts Learned
## WHAT IS THE COMMAND LINE?
A **Command-Line Interface (CLI)** allows users to interact with the operating system by typing commands instead of using a graphical interface.

The default command-line interpreter in Windows is: 
`cmd.exe`

Although the CLI has a learning curve, it can become faster and more efficient than using a graphical interface for many tasks.

### Advantages of the CLI
- **Lower resource usage** – Requires fewer system resources than a graphical interface.
- **Automation** – Commands can be placed into scripts or batch files to automate repetitive tasks.
- **Remote management** – Useful for managing servers and other remote systems, especially over slower network connections.
- **Efficiency** – Many administrative tasks can be completed quickly without navigating through multiple menus.

## BASIC SYSTEM INFORMATION
→ `set` - Displays environment variables configured on the system.

One important variable is `Path = ...`  
- The **PATH environment variable** contains directories where Windows searches for executable commands.  
- This allows commands stored in those directories to be executed without typing their full location.  

→ `ver` - Displays the Windows operating system (OS) version.

→ `systeminfo`- Displays detailed information about the system.

Information includes:
- OS name and version
- System manufacturer and model
- Processor information
- Installed memory
- BIOS information
- Network configuration
- System boot time

→ `help` - Displays a list of available commands and basic help information.  
- `help command` or `command /?`- Provides built-in help information for a specific command.
- While `command -h` or `command --help` are more common with third-party command-line programs.

→ `cls` - Clears the Command Prompt screen.

## SHUTDOWN AND RESTART COMMANDS
→ `shutdown /s` - Shuts down the computer.
→ `shutdown /r` - Restarts the computer.
→ `shutdown /a` - Cancels a pending shutdown or restart. (`/a` stands for abort.)

## NETWORK CONFIGURATION
The command line provides several tools for viewing network configuration and troubleshooting connectivity problems.  

→ `ipconfig` - Displays basic network configuration.
Information includes:
- IP address
- Subnet mask
- Default gateway

→ `ipconfig /all` - For more detailed information.
This can also display:
- Physical (MAC) address
- DNS servers
- DHCP configuration
- DHCP lease information

## NETWORK TROUBLESHOOTING
→ `ping` - Tests whether another host can be reached over the network.

Sends **ICMP Echo Request packets** to the target and waits for replies.
It can help determine:
- Whether the target is reachable
- Approximate response time
- Whether packets are being lost

💡 A failed ping does not always mean the host is offline because ICMP traffic may be blocked by a firewall.

→ `tracert (trace route)` - Traces the network path packets take toward a destination.  

- Discovers intermediate routers by sending packets with increasing Time-To-Live (TTL) values.  
- Each router decreases the TTL by 1, and when it reaches 0, that router responds, allowing tracert to identify each hop along the path.

💡 TTL = a limit on how many routers (hops) a packet can pass through.
💡 Useful for identifying where network connectivity or routing problems occur.

## MORE NETWORK COMMANDS
→ `nslookup` - Queries DNS to find information about a hostname or domain.

→ `netstat`- Displays active network connections and listening ports.

A particularly useful option is: `netstat -ano`
Where:
- a – Displays all connections and listening ports.
- n – Displays addresses and ports numerically.
- o – Displays the Process ID (PID) associated with each connection.

💡 The PID can be compared with `tasklist` to identify which process is using a network connection or listening port.

## FILE AND DISK MANAGEMENT
Command Prompt can be used to navigate directories and manage files without using File Explorer.

### Working with Directories
→ `cd` - Will display the current directory (Where am I?)
- `cd target_directory` - Will change directories.  
- `cd ..` - To move up one directory level.  

→ `dir` - Displays files and directories in the current location.
- `dir /a` - Displays files with all attributes, including hidden and system files.
- `dir /s` - Displays files in the current directory and all subdirectories.

→ `tree` - Displays the directory structure visually.
- `tree /f`- To also display files. 

→ `mkdir`- Creates a new directory 
- To create a directory use `mkdir directory_name`

→ `rmdir` - Removes a directory.
- To delete an empty directory use `rmdir directory_name`
- To remove a directory and everything inside it: `rmdir /s directory_name` 

⚠️ Be careful with `/s` because it removes the directory, its subdirectories, and its files.

### Working with Files
→ `type` - Displays the contents of a text file directly in the terminal.

→ `more command` - Displays long text output one screen at a time.
Controls:
- `Spacebar` – Move to the next page.
- `Enter` – Move forward one line.

We can use the command more in two ways:
- Display text files: `more file.txt`
- Pipe long output to view it page by page: `some_command | more`

💡 The pipe (|) sends the output of one command into another command.

→ `copy` - Copies files from one location to another.

→ `move` - Moves a file to another location.
💡 It can also be used to rename files.

→ `del` / `erase` - Deletes files.
💡 Both commands perform the same basic function.

### Wildcards
The wildcard character `*` can represent multiple files. 

For example: 
- `copy *.md C:\Markdown` - will copy all files with the extension `md` from the current directory to `C:\Markdown`.
- `del *.txt` - will delete all files ending in `.txt` from the current directory

⚠️ Wildcards should be used carefully with deletion commands.

## TASK AND PROCESS MANAGEMENT
Windows provides command-line tools for viewing and managing running processes and achieves a similar functionality as task manager.

→ `tasklist` - Displays currently running processes.
💡 The output can be very long, some filtering will be required `tasklist /?`  

For example, if we want to search for tasks related to `notepad.exe`: `tasklist /FI "imagename eq notepad.exe`  
💡 /FI is used to set the filter image name equals notepad.exe

Where:
- `/FI` – Applies a filter.
- `IMAGENAME` – Filters by executable name.
- `eq` – Means equals.

→ `taskkill` - Terminates a running process.
- Knowing the Process ID(PID), any process can be terminated: `taskkill /PID target_pid`
- A process can also be forcefully terminated, where `/F` means **force**: `taskkill /PID target_pid /F`

💡 `tasklist` can be used to identify a process and its PID before using `taskkill`.

## 🛠️ Practical Skills Developed
- Navigate Windows using Command Prompt
- Display basic system information
- Check and troubleshoot network configuration
- Manage files and folders
- Check running processes

## 🧰 Tools Used
- TryHackMe platform
- Windows Command Prompt (`cmd.exe`)

## 🔐 Security Relevance
The Windows Command Line is an important tool for system administration and cybersecurity.

It can be used to:

- Quickly gather information about a Windows system.
- Inspect network configuration and connectivity.
- Identify listening ports and active connections.
- Discover running processes.
- Navigate the filesystem and inspect files.
- Troubleshoot systems remotely.
- Automate administrative and security tasks.

Many cybersecurity tools and Windows administration techniques rely heavily on command-line interfaces, making CLI knowledge an important foundation for both defensive and offensive security.

## 📌 Lessons Learned  
💡 The Windows CLI can perform many administrative tasks faster than navigating through graphical menus.  
💡 Built-in help such as command /? is useful when you forget the syntax or available options for a command.  
💡 Networking commands such as ipconfig, ping, tracert, nslookup, and netstat provide different pieces of information when troubleshooting a network.  
💡 Commands such as tasklist and taskkill allow processes to be investigated and managed directly from the terminal.  
💡 Pipes (|), filters, and wildcards (*) make command-line tools much more powerful by allowing commands to work together and process larger amounts of information.  
