# Search Skills – TryHackMe 

Platform: TryHackMe    
Skill Level: Beginner / Foundation  
Focus Area: Permissions 101

## 🎯 Objective 
- Understand how Linux permissions control access to files and directories.
- Learn how to view, interpret, and modify permissions.
- Recognise the importance of the Principle of Least Privilege in securing systems.

## 🧠 Core Concepts Learned   
## Linux Permissions 
- Every file and directory in Linux has associated permissions.
- Permissions determine who can **read**, **write**, or **execute** a file.
- Permissions are divided into three categories:
    - User (Owner)
    - Group
    - Others

### Permission Types
- **Read (r)**
    - File: View contents.
    - Directory: List files within the directory.
- **Write (w)**
    - File: Modify or delete contents.
    - Directory: Create, rename, or delete files.
- **Execute (x)**
    - File: Run the file as a program or script.
    - Directory: Enter or access the directory.

### Viewing Permissions
- Linux file permissions can be viewed using `ls -l` command.
- The `-l` switch displays files and directories, providing information such as permissions, ownership, file size, and the date the file was last modified. 

#### 🧪 TryHackMe Lab Example – Breaking Down the Output
**Actions Performed:** 
- Used `ls -l` command to inspect file permissions.
- Analysed the following output:  
`-rwxr-xr-- 1 owner developers 1250 Jun 7 12:30 script.sh`   

| Section       | Meaning                         |
| ------------- | ------------------------------- |
| `-`           | File type (regular file)        |
| `rwx`         | Owner permissions               |
| `r-x`         | Group permissions               |
| `r--`         | Others permissions              |
| `1`           | Number of hard links            |
| `owner`       | Owner of the file               |
| `developers`  | Group associated with the file  |
| `1250`        | File size (in bytes)            |
| `Jun 7 12:30` | Last modification date and time | 
| `script.sh`   | File name                       |  

💡 File type: `-` (Regular file), `d` (Directory), `l` (Symbolic Link)  
💡 `l` (Symbolic Link) - is a shortcut or pointer to another file or directory, similar to desktop shortcuts in Windows.     
💡 The `ln` command is used to create links (`ln -s notes.txt notes_link`)  

**Key Finding:**  
- Incorrect permissions can expose sensitive files or allow unauthorised modifications.

**Key Insight:**  
- Applying only the permissions required for a task helps reduce the attack surface of a system.

### Changing Permissions
- Linux permissions can be modified using either the numeric or symbolic method.
- The numeric method converts symbolic permissions into numbers by adding predefined values together.

| Permission    | Binary | Value |
| ------------- | ------ | ----- |
| Read (`r`)    | `100`  | 4     |
| Write (`w`)   | `010`  | 2     |
| Execute (`x`) | `001`  | 1     |  

💡 Linux uses a binary system to represent permissions.  

#### 🧪 TryHackMe Lab Example – Converting Symbolic Permissions to Numbers
**Actions Performed:** 
1. Output: `-rwxr-xr-- 1 owner developers 1250 Jun 7 12:30 script.sh`
2. Broke the permissions into three groups:
|`rwx`| `r-x`| `r--` |
|Owner| Group| Others|
3. Converted each group into numeric values:
`rwx` = 4 + 2 + 1 = 7  
`r-x` = 4 + 1 = 5   
`r--` = 4     
Result:` rwxr-xr--` = 754    
Equivalent command: `chmod 754 filename`   

⚠️ Avoid using 777 unless absolutely necessary.  
⚠️ Granting full permissions to everyone can expose files to unauthorised modifications or abuse.  

**Key Finding:**
- Symbolic permissions can be converted into numeric values by adding the values of the permissions present in each permission group.

**Key Insight:**
- Understanding both symbolic (rwxr-xr--) and numeric (754) representations makes it easier to interpret existing permissions and apply them efficiently.  

💡 `chmod` (Change Mode) command is used to change the permissions of files and directories in Linux.    
💡 Proper use of this command helps enforce the Principle of Least Privilege.    

#### 🧪 TryHackMe Lab Example – Using Symbolic Permissions
- The symbolic method follows the structure:  
`chmod [who][action][permission] filename`  
`chmod u+x script.sh`  
    - Who? = User/ Owner  
    - Action? = Add  
    - Permission? = Execute    

Who?   
| Symbol | Meaning      |
| ------ | ------------ |
| `u`    | User (owner) |
| `g`    | Group        |
| `o`    | Others       |
| `a`    | All users    |

Actions?  
| Symbol | Meaning              |
| ------ | -------------------- |
| `+`    | Add permission       |
| `-`    | Remove permission    |
| `=`    | Set exact permission |

Permissions?  
| Symbol | Meaning |
| ------ | ------- |
| `r`    | Read    |
| `w`    | Write   |
| `x`    | Execute |  

Example:   
`chmod u+x script.sh` = Add execute permission to the owner.  
`chmod g-w file.txt` = Remove write permission from the group.  
`chmod o+r report.txt` = Give others read permission.  

**Key Finding:**
- Symbolic permissions provide a flexible way to modify specific permissions without recalculating the entire numeric value.

**Key Insight:**
- Understanding the structure `chmod [who][action][permission]` makes it easier to manage permissions efficiently and reduces the risk of accidentally granting excessive access.

### The Differences Between Users & Groups  
👤 **User**
- A user is an individual account on a Linux system.
- Users can log in and perform actions based on the permissions assigned to them.  

👥 **Group** 
- A group is a collection of users.
- Instead of assigning permissions to each user individually, permissions can be assigned to the group.
- Groups simplify permission management by allowing multiple users to share the same access rights.

#### Why Groups Are Important  
**Without groups:**  
- Permissions would need to be managed separately for every user.
- Administration becomes more time-consuming and prone to mistakes.

**With groups:**  
- Access can be granted or removed efficiently.
- Users can collaborate securely on shared resources.
- Organisations can better apply the Principle of Least Privilege.

### Switching Between Users
- The `su` (Substitute User) command is used to switch between user accounts.
- This command requires: 
    - The user account you wish to switch to 
    - The user's password    

Example:  
`su analyst`  
💡 The `whoami` command can be used to identify the currently logged-in user.    

## 🛠️ Practical Skills Developed
- Reading Linux permission strings.
- Determining who has access to files and directories.
- Viewing and interpreting file ownership information.
- Converting symbolic permissions into numeric values.
- Modifying permissions using the chmod command.
- Understanding the relationship between users, groups, and access control.
- Applying the Principle of Least Privilege.

## 🧰 Tools Used 
- TryHackMe platform 
- Linux Terminal

## 🔐 Security Relevance
- Misconfigured permissions are a common cause of security incidents.
- Attackers often search for files that are world-writable or contain sensitive information with overly permissive access.
- Proper permission management helps:
    - Protect confidential data.
    - Prevent unauthorised privilege escalation.
    - Reduce opportunities for lateral movement within a system.
    - Support compliance with security best practices.

## 📌 Lessons Learned 
⚠️ Even small permission mistakes can have significant security consequences.  
⚠️ Granting users more access than necessary increases organisational risk.  
⚠️ Understanding Linux permissions is essential for system administration, incident response, and cybersecurity roles such as SOC Analyst positions.   
⚠️ Applying the Principle of Least Privilege helps minimise security risks by ensuring users only have the access required to perform their tasks.  