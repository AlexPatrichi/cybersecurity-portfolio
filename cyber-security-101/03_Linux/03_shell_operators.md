# Linux - TryHackMe and Solent University Cybersecurity Coursework 

Platform: TryHackMe  
Skill Level: Beginner / Foundation  
Focus Area: Shell Operators

## 🎯 Objective
- Understand how shell operators control command execution
- Learn how to run commands in the background
- Combine commands using logical operators
- Redirect command output into files

## 🧠 Core Concepts Learned 
## Shell Operators  
Shell operators are special characters used in the terminal to control how commands behave  

They can be used to:
- Run commands in the background
- Combine multiple commands
- Redirect command output
- Append output to existing files

### → "&" Operator
- Runs a command in the background
- Allows the terminal to stay available while the command continues running

**Example:** `cp large_file.zip /backup/ &`   

💡 This is useful when running a command that may take a long time

### → "&&" Operator
- Make a list of commands to run
- Runs the second command only if the first command succeeds

**Example:** `mkdir test && cd test`  

### → ">" Operator
- Known as an **output redirector**
- Redirects command output into a file
- Creates the file if it does not exist
- Overwrites the file if it already exists

**Example:** `echo "Hello Linux" > message.txt`  

⚠️ This operator can overwrite existing file content

### → ">>" Operator
- Adds command output to the end of a file
- Does not overwrite existing content

**Example:** `echo "Second line" >> message.txt`  

💡 Useful for adding logs, notes, or command results to an existing file

## 🛠️ Practical Skills Developed
- Used basic shell operators in the terminal  
- Ran commands in the background using `&`  
- Combined commands using `&&`  
- Saved command output into files  
- Added output to existing files without deleting previous content  

## 🧰 Tools Used
- Solent University Cybersecurity Coursework
- TryHackMe platform
- Linux (terminal environment)
- Bash shell

## 🔐 Security Relevance
- Shell operators are commonly used in Linux administration and cybersecurity tasks
- Output redirection is useful for saving command results, logs, and investigation notes
- Understanding overwrite and append behaviour helps prevent accidental data loss
- Chaining commands helps automate basic security and system tasks safely

## 📌 Lessons Learned
⚠️ `>` overwrites file content, while `>>` adds new content to the end of the file  
⚠️ `&&` ensures the next command only runs if the previous one succeeds

💡 Shell operators make Linux commands more powerful by allowing automation, redirection, and better workflow control.