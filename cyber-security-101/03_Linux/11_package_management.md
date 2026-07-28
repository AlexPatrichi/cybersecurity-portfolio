# Linux – TryHackMe 

Platform: TryHackMe    
Skill Level: Beginner / Foundation  
Focus Area: Maintaining your System - Package Management

## 🎯 Objective 
- Understand what software packages are in Linux.
- Learn how package repositories work.
- Understand how Ubuntu's APT package manager installs, updates, and removes software.
- Learn how to add and remove third-party repositories safely.
- Understand the purpose of GPG keys in verifying software authenticity.

## 🧠 Core Concepts Learned   
## What Are Packages?
- A package is a compressed archive that contains:
    - The application itself
    - Configuration files
    - Libraries and dependencies
    - Metadata (version, author, etc.)

- Package management systems make installing, updating, and removing software simple without manually downloading individual files.

## Software Repositories
- A repository (repo) is an online collection of software packages maintained by an operating system vendor or software developer.
- Instead of downloading software from random websites, Linux retrieves packages from trusted repositories.
- Benefits include:
    - Easy software installation
    - Automatic updates
    - Dependency management
    - Improved security through package verification
- Ubuntu uses repositories listed in: `/etc/apt/sources.list`
- Additional repositories are usually stored as separate files inside: `/etc/apt/sources.list.d/`
- Keeping third-party repositories in separate files makes them easier to manage or remove later.

## APT (Advanced Package Tool)
- Ubuntu uses APT (Advanced Package Tool) as its package management system.
- APT can:
    - Install software
    - Remove software
    - Upgrade installed packages
    - Search for packages
    - Download dependencies automatically
    - Update package lists from repositories
- Common commands include:
    - `sudo apt update` - Downloads the latest package lists from all configured repositories.                  
    - `sudo apt upgrade` - Upgrades installed packages to their newest available versions.                       
    - `sudo apt install <package>` - Installs the specified package along with any required dependencies.                  
    - `sudo apt remove <package>` - Removes the specified package but usually keeps its configuration files.             
    - `sudo apt purge <package>` - Completely removes the package, including its configuration files.                   
    - `sudo apt autoremove` - Removes unused packages that were installed as dependencies but are no longer needed. 

## Adding Third-Party Repositories
- Not every application exists in Ubuntu's official repositories.
- Software vendors often provide their own repositories so users can install and receive updates directly from them.
- One way to add a repository is with:
    - `sudo add-apt-repository <repository>`
- Repositories can also be added manually by creating a new `.list` file inside:
    - `sudo nano /etc/apt/sources.list.d/sublime-text.list`

## GPG Keys
- Before trusting software from a repository, Linux verifies that it comes from the expected developer.
- This is done using GPG (GNU Privacy Guard) keys.
- A GPG key:
    - Verifies the repository's identity
    - Ensures packages haven't been modified
    - Protects against tampered or malicious software
- Example: 
`wget -qO - https://download.sublimetext.com/sublimehq-pub.gpg | sudo apt-key add -`

## Updating Package Lists
- Whenever a new repository is added or removed, APT must refresh its package database.
- Example: `sudo apt update`
- It simply downloads the newest package information from every configured repository.

## 🛠️ Practical Skills Developed
- Managing software with APT.
- Understanding the purpose of software repositories.
- Adding trusted third-party repositories.
- Importing GPG keys to verify software authenticity.
- Updating package lists.
- Installing and removing software packages.
- Understanding the difference between official and community repositories.

## 🧰 Tools Used
- TryHackMe platform
- Linux Terminal

## 🔐 Security Relevance
- Install software only from trusted repositories to reduce the risk of malware.
- GPG keys verify that packages originate from the legitimate developer and have not been altered.
- Regularly updating packages helps patch known security vulnerabilities.
- Third-party repositories should be added only when necessary, as they introduce software maintained outside the official Ubuntu repositories.
- Removing unused repositories reduces the system's attack surface and simplifies maintenance.

## 📌 Lessons Learned
💡 Linux package management is designed to make software installation, updates, and removal both efficient and secure.  
💡 APT automatically installs any required dependencies, so you don't have to install everything manually.  
💡 Repositories act as trusted software sources, while GPG keys ensure the authenticity and integrity of downloaded packages.  
💡 Running apt update refreshes the list of available packages, while apt upgrade installs newer versions of already installed packages.  
💡 Keeping software up to date through trusted repositories is one of the simplest and most effective ways to maintain a secure Linux system.  





