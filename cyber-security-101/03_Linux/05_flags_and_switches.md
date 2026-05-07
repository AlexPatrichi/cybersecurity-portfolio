# Linux - TryHackMe and Solent University Cybersecurity Coursework 

Platform: TryHackMe  
Skill Level: Beginner / Foundation  
Focus Area: Flags and Switches 

## 🎯 Objective
- Understand what flags and switches are in Linux commands
- Learn how command behaviour can be modified
- Recognise commonly used Linux command options

## 🧠 Core Concepts Learned 
## Linux Flags and Switches
- Flags and switches are additional **options** added to commands
- They modify how a command behaves
- Usually written after the command using:
    -  `-` for short options
    - `--` for long options

💡 Flags make Linux commands more powerful and flexible

**Example**  
    - `ls` command → performs its default behaviour  
    - Adding `-a` as an argument (short for `--all`) displays more files and folders, including hidden ones

- Flags and switches can often be combined
**Example**
- `ls -la`
    - `-l` → long listing format
    - `-a` → show hidden files

## Short vs Long Options
| Short Option | Long Option | Purpose        |
| ------------ | ----------- | -------------- |
| `-h`         | `--help`    | Display help   |
| `-v`         | `--version` | Show version   |
| `-a`         | `--all`     | Show all items |

## How to Find Command Options
### The `--help` Option
- The `--help` option: 
    - prints a list with all the possible options that the command accepts
    - provides a brief description and usage examples 

**Example**
- `ls --help`
💡 `--help` is a quick way to learn how a command works

### The Man Page (Manual)
- A great source of information for Linux system commands and applications
- Contains detailed documentation about: Syntax, Options, Usage Examples, Behaviour of Commands

**Example** 
- `man ls`
💡 `man` is one of the most useful learning tools in Linux

## 🛠️ Practical Skills Developed
- Using command-line options effectively
- Reading Linux manual pages
- Combining command flags for advanced functionality
- Understanding safe vs dangerous command options

## 🧰 Tools Used
- Solent University Cybersecurity Coursework
- TryHackMe platform
- Linux (terminal environment)
- Bash Shell

## 🔐 Security Relevance
- Linux administrators and cybersecurity professionals rely heavily on command-line options
- Many security tools use flags to control scanning, logging, verbosity, and automation
- Incorrect use of destructive flags can damage systems or delete important data

## 📌 Lessons Learned
- Flags and switches extend command functionality
- Linux commands become more efficient when combined with options
- Understanding command syntax is essential for Linux system administration and cybersecurity work