# Linux – TryHackMe 

Platform: TryHackMe    
Skill Level: Beginner / Foundation  
Focus Area: Terminal Text Editors

## 🎯 Objective 
- Understand what terminal text editors are.
- Learn how to create and modify files without a graphical interface.
- Become familiar with common Linux text editors.

## 🧠 Core Concepts Learned   

## What is a Terminal Text Editor?
- A terminal text editor allows users to create, view, and modify text files directly from the command line.

- These editors are commonly used by:
1. System administrators
2. Developers
3. Cybersecurity professionals
4. Linux users working on remote systems

- Unlike graphical editors, terminal editors work entirely within the terminal window.

## Common Terminal Text Editors 
### `nano`
- A simple and beginner-friendly text editor.
- Often recommended for beginners because its commands are displayed at the bottom of the screen.
- To create or open a file: `nano example.txt`
- Nano has features that are easy to remember and covers the most common tasks you would want from a text editor, including:
    - Searching for text
    - Copying and pasting
    - Jumping to a line number
    - Finding out what line number you are on

- Useful shortcuts:
| Shortcut    | Action      |
| ----------  | ----------- |
| Ctrl(^) + O | Save file   |
| Ctrl(^) + X | Exit editor |
| Ctrl(^) + K | Cut line    |
| Ctrl(^) + U | Paste line  |
| Ctrl(^) + R | Read file   |
| Ctrl(^) + \ | Replace     |
| Ctrl(^) + _ | Go to line  |
| Ctrl(^) + W | Where is    |

### `vim`
- A powerful and widely used text editor.
- Vim is more advanced but is extremely efficient once mastered.
- Open a file: `vim example.txt`

- Basic commands:
| Command | Action              |
| ------- | ------------------- |
| i       | Enter insert mode   |
| Esc     | Exit insert mode    |
| :w      | Save                |
| :q      | Quit                |
| :wq     | Save and quit       |
| :q!     | Quit without saving |

- VIM's benefits:
    - Customisable - users can modify settings, key mappings, plugins, and appearance to suit their workflow.
    - Syntax Highlighting - useful when writing or maintaining code, making it a popular choice for software developers.
    - Widely Available – Vim is installed on many Linux systems where Nano may not be available.
    - Extensive Learning Resources – there are many tutorials, guides, and cheatsheets available for learning Vim.

## 🛠️ Practical Skills Developed
- Creating and editing text files directly from the Linux terminal.
- Navigating and using the Nano text editor.
- Saving, exiting, searching, and modifying text within a file.
- Understanding the basic workflow of the Vim editor.
- Learning common keyboard shortcuts used in terminal-based text editors.
- Editing files on systems where a graphical interface is unavailable.

## 🧰 Tools Used 
- TryHackMe platform 
- Linux Terminal

## 🔐 Security Relevance
- Configuration files on Linux systems are often edited using terminal text editors.
- Security professionals frequently use editors such as Nano or Vim when connected to remote systems via SSH.
- Many cybersecurity tools generate log files, scripts, and configuration files that require manual editing.
- Understanding terminal text editors is essential when working in server environments where graphical interfaces are not available.

## 📌 Lessons Learned 
💡 Terminal text editors allow files to be created and modified without a graphical interface.   
💡 Nano is a beginner-friendly editor that provides visible keyboard shortcuts and simple navigation.   
💡 Vim offers greater flexibility and efficiency but requires learning different modes and commands.   
💡 Knowing how to use terminal text editors is an important skill for Linux administration, scripting, and cybersecurity tasks.    
💡 Being comfortable with at least one terminal editor makes it easier to manage files on remote Linux systems.    