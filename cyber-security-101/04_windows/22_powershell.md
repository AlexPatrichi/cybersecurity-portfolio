# Windows – TryHackMe

Platform: TryHackMe     
Skill Level: Beginner / Foundation     
Focus Area: Windows PowerShell

## 🎯 Objective
- Learn what PowerShell is and its capabilities.
- Understand the basic structure of PowerShell's language.
- Learn and run basic PowerShell commands.
- Navigate and manage the file system using PowerShell.
- Understand pipelines, filtering, and sorting.
- Retrieve system and network information.
- Understand the basics of PowerShell scripting.
- Understand PowerShell's applications in cybersecurity.

## 🧠 Core Concepts Learned
## WHAT IS POWERSHELL? 
**PowerShell** is a command-line shell and scripting language developed by Microsoft for system administration, automation, and configuration management.  

It combines:
- A **Command-Line Interface (CLI)** for executing commands.
- A **scripting language** for creating scripts and automating repetitive tasks.
- The **.NET platform**, which provides access to system components and functionality.

💡 .NET is Microsoft's development platform that provides PowerShell with built-in functionality for interacting with files, processes, networks, and other system components.  

💡 PowerShell was originally developed for Windows, but modern versions are cross-platform and can run on Windows, Linux, and macOS.  

### PowerShell vs Command Prompt
💡 Unlike the traditional Windows Command Prompt (`cmd.exe`), **which mainly works with text, PowerShell works with objects.**  

In programming, an **object** represents an item with **properties** (characteristics) and **methods** (actions).  

For example, a `Car` object could have:  
```text
Properties:
Color
Model
FuelLevel

Methods:
Drive()
Honk()
Refuel()
```
Similarly, PowerShell works with objects that represent things such as **files, processes, services, and users**.  

For example, a **File** object can have properties such as:
```text
Properties:
FileName
Length
CreationTime

Methods:
Delete()
CopyTo()
MoveTo()
```
💡 Properties describe an object, while methods define what can be done with it.  

Because PowerShell passes structured objects between commands instead of only plain text, information can be **filtered, sorted, selected, and manipulated more easily**.  

## POWERSHELL BASICS
### Launching PowerShell
**PowerShell** can be launched in several ways:
- **Start Menu** → Search for `PowerShell`.
- **Run Dialog** → Press `Win + R`, type `powershell`, and press `Enter`.
- **File Explorer** → Type `powershell` in the address bar to open PowerShell in the current directory.
- **Command Prompt** (`cmd.exe`) → Type: `powershell`

💡 Once PowerShell is running, the command prompt begins with `PS`:
`PS C:\Users\captain>`  
💡 PS indicates that we are currently using PowerShell rather than Command Prompt.

### Windows PowerShell vs PowerShell
There are two versions commonly encountered:

- **Windows PowerShell 5.1** → Older version included with Windows and based on the .NET Framework.
- **PowerShell 7+** → Modern, cross-platform version based on modern .NET and installed separately.

They use different executables:
- Windows PowerShell 5.1 → powershell.exe
- PowerShell 7+          → pwsh.exe

## POWERSHELL COMMANDS
Powershell commands are known as `cmdlets`(pronounced `command-lets`).    
**Cmdlets** are designed to perform specific tasks and work with objects, allowing data to be easily filtered, sorted, and manipulated.  

### Basic Syntax 
Cmdlets follow a consistent **Verb-Noun** naming convention.  
The **Verb** describes the action, and the **Noun** specifies the object on which action is performed.    
  
Examples: 
- **Get-Content** → Retrieves (gets) the content of a file and displays it in the console.
- **Set-Location** → Changes (sets) the current working directory.
- **Get-Process** → Retrieves running processes.
- **Stop-Process** → Stops a running process.

### Helpful Commands

→ `Get-Command` 
Used to discover available PowerShell commands.  

It can search for specific commands using wildcards `*`:  
`Get-Command *Process*` → Displays commands containing `Process`.  

It can also search by verb:  
`Get-Command -Verb Remove` → Displays commands that use the `Remove` verb.  

→ `Get-Help`
Displays information about how to use a command.  
Example: `Get-Help Get-Process`  

It can show information such as:
- Command description
- Syntax
- Parameters
- Examples  
  
Example: 
- `Get-Help Get-Process -Examples` → Displays examples of how `Get-Process` can be used.
- `Get-Help Get-Process -Full` → Displays more detailed help.

→ `Get-Member`  
Displays the properties and methods of an object.   
Example: `Get-Process | Get-Member` → This shows the properties and methods available on the objects returned by `Get-Process`.

💡 The pipe `|` passes the objects produced by `Get-Process` to `Get-Member`.  

💡Mental Model  
`Get-Command` → What commands can I use?  
`Get-Help`    → How do I use a command?  
`Get-Member`  → What does this object contain?  
 
## WORKING WITH THE FILE SYSTEM
PowerShell provides several cmdlets for **navigating the file system and managing files and directories.**

→ `Get-ChildItem`  
Lists the files and directories in a specified location.     
It is similar to `dir` in Command Prompt and `ls` in Unix/Linux Systems.    
Example: `Get-ChildItem -Path C:\Users -Recurse`    

Useful parameters: 
- **-Path** → Specifies the location to explore.
- **-Recurse** → Also searches through all subdirectories.
- **-Force** → Includes hidden items.

→ `Set-Location`  
Changes the current working directory, similar to the `cd` in Command Prompt.  
Example: `Set-Location -Path C:\Users`    

💡 PowerShell also supports `cd` as an alias for `Set-Location`.

→ `New-Item`
Creates a new item, such as a file or directory.  
Create a **file**: `New-Item -Path notes.txt -ItemType File`    
Create a **directory**: `New-Item -Path C:\Test -ItemType Directory`    

→ `Remove-Item`  
Removes files and directories.    
Example: `Remove-Item -Path notes.txt`    

To remove a directory and everything inside it:  
`Remove-Item -Path C:\Test -Recurse`   
⚠️ Be careful when using `-Recurse`, as it can remove all files and subdirectories within the specified directory.

→ `Copy-Item`   
Copies files or directories to another location.  
Example: `Copy-Item -Path notes.txt -Destination C:\Backup`  

For directories and their contents:
`Copy-Item -Path C:\Test -Destination C:\Backup -Recurse`

→ `Move-Item`  
Moves a file or directory to another location.  
Example: `Move-Item -Path notes.txt -Destination C:\Backup`  

💡 `Move-Item` can also be used to **rename an item** by moving it to a new name in the same directory.  

→ `Get-Content`  
Read and display the contents of a file.  
Example: `Get-Content -Path notes.txt`  

## PIPING, FILTERING, AND SORTING DATA
### Pipeline `|`
Allows the output of one command to be passed as input to another command.  

In PowerShell, pipelines are especially powerful because they pass objects rather than just plain text. These objects retain their properties and methods.  

Example: `Get-Process | Get-Member`  
💡 `Get-Process` retrieves process objects and passes them through the pipeline (|) to `Get-Member`.

### Where-Object → Which objects do I want?
Filters objects based on specified conditions.

Example: `Get-Process | Where-Object {$_.CPU -gt 10}`   
💡 Displays processes that have used more than 10 seconds of total CPU time.

Here:
- `$_` → Represents the current object passing through the pipeline.
- `.CPU` → Accesses its CPU property.
- `-gt 10` → Checks whether the value is greater than 10.

### Comparison Operators
**Comparison operators** are commonly used with `Where-Object` to define filtering conditions.
| Operator   | Meaning                           |
| ---------- | --------------------------------- |
| `-eq`      | Equal to                          |
| `-ne`      | Not equal to                      |
| `-gt`      | Greater than                      |
| `-ge`      | Greater than or equal to          |
| `-lt`      | Less than                         |
| `-le`      | Less than or equal to             |
| `-like`    | Matches a pattern using wildcards |
| `-notlike` | Does not match a pattern          |

Example: `Get-Process | Where-Object {$_.Name -like "power*"}`   
💡 Displays processes whose `Name` property begins with `power`.  
💡 The `*` wildcard represents zero or more characters.  

### Select-Object → Which properties do I want?
Used to select specific **properties** from objects.  

Example: `Get-Process | Select-Object Name, Id, CPU`     
💡 Instead of displaying every available property, this displays only: Name, Id, CPU.  

### Sort-Object → In what order do I want them?  
**Sorts** objects based on a specified property.  

Example: `Get-Process | Sort-Object CPU`   
💡 Sorts processes by their `CPU` property.  

To reverse the order: `Get-Process | Sort-Object CPU -Descending`  

### Select-String → What text am I looking for?
**Searches** for text patterns within strings and files.

Example: `Select-String -Path logfile.txt -Pattern "error"`   
💡 Searches `logfile.txt` for lines containing error.

It can also be used in a pipeline: `Get-Content logfile.txt | Select-String "error"`

### Why PowerShell pipelines are useful
Example:
 `Get-Process | Where-Object {$_.CPU -gt 10} | Sort-Object CPU -Descending | Select-Object Name, CPU`  

The data flows through several stages:  
                   `Get-Process`
                       │
                       ▼
              Gets all running processes
                       │
                       ▼
                  `Where-Object`
                       │
                       ▼
        Filters processes with more than
            10 seconds of CPU time
                       │
                       ▼
                   `Sort-Object`
                       │
                       ▼
           Sorts them by CPU time from
               highest to lowest
                       │
                       ▼
                  `Select-Object`
                       │
                       ▼
           Displays only the Name and
                CPU properties

## SYSTEM AND NETWORK INFORMATION
PowerShell provides several `cmdlets` for retrieving information about the **system, users, and network configuration.**

### Get-ComputerInfo
Retrieves detailed information about the computer.

Information can include:
- Operating system
- Hardware
- BIOS
- Windows version
- Computer name
- System configuration

### Get-LocalUser 
Lists all the **local user accounts** on the system.  
Essential for managing user accounts and understanding the machine’s security configuration.  

It can display information such as:
- Username
- Whether the account is enabled
- Account description
- Password-related information

### Get-NetIPConfiguration 
Displays an overview of the system's network configuration.  

Information can include:
- Network interfaces
- IP addresses
- Default gateway
- DNS servers

💡 Similar in purpose to `ipconfig`, but returns structured PowerShell objects.

### Get-NetIPAddress
Displays detailed information about the **IP addresses assigned to network interfaces**.

### Get-NetTCPConnection
Displays current TCP connections and listening ports.  

It can show information such as:
- Local IP address and port
- Remote IP address and port
- Connection state
- Owning process

## SCRIPTING
A **PowerShell script** is a text file containing a sequence of PowerShell commands that can be executed together.

PowerShell scripts use the `.ps1` file extension.
Example: `script.ps1`

Scripts are commonly used to:
- Automate repetitive tasks
- Perform multiple commands in sequence
- Manage systems and users
- Gather and process system information
- Automate administrative and security tasks

### Simple Script
Example `SystemInfo.ps1`: 
```powershell
Write-Output "Computer Information"
Get-ComputerInfo

Write-Output "Local Users"
Get-LocalUser

Write-Output "Network Configuration"
Get-NetIPConfiguration
```
Run the script with:
`.\SystemInfo.ps1`

💡 `.\` tells PowerShell to execute the script located in the current directory.

### Variables
Variables store values that can be reused later.  
PowerShell variables begin with `$`:
```powershell
$name = "Alex"
Write-Output "Hello, $name"
```
💡 PowerShell variables begin with $ and can store values such as text, numbers, or objects.

### Comments
Comments allow notes or explanations to be added to a script without being executed.
Single-line comment:
```powershell
# Get all running processes
Get-Process
```
### Execution Policy
PowerShell uses an execution policy that controls the conditions under which scripts can run.

View the current policies with: `Get-ExecutionPolicy -List`

💡 Execution Policy is a safety feature designed to help prevent accidental execution of untrusted scripts, but it is not a security boundary.

## 🛠️ Practical Skills Developed
- Navigate and manage Windows using PowerShell.
- Discover commands and access built-in help.
- Manage files and directories.
- Use pipelines to filter, sort, and select data.
- Retrieve system, user, and network information.
- Create and run basic PowerShell scripts.

## 🧰 Tools Used
- TryHackMe platform
- Windows PowerShell

## 🔐 Security Relevance
PowerShell is a powerful tool for **system administration, automation, and cybersecurity.**

It can be used to:

Gather system, user, and network information.
Inspect processes and network connections.
Search and analyse files and logs.
Automate administrative and security tasks.

💡 PowerShell is used by both **security professionals and attackers**, making it important to understand for system investigation and defence.

## 📌 Lessons Learned  
💡 PowerShell works with objects, which contain properties and methods.  
💡 Cmdlets generally follow the Verb-Noun naming convention.  
💡 Pipelines (|) allow objects to be passed between commands.  
💡 PowerShell makes it easy to filter, sort, select, and search data.  
💡 PowerShell scripts (.ps1) can automate repetitive tasks.  
💡 PowerShell is a powerful tool for Windows administration and cybersecurity.    