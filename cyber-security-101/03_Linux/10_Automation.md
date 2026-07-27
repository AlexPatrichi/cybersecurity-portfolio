# Linux – TryHackMe 

Platform: TryHackMe    
Skill Level: Beginner / Foundation  
Focus Area: Maintaining your System: Automation

## 🎯 Objective 
- Understand what task automation is in Linux.
- Learn how the `cron` service schedules recurring tasks.
- Understand how to create, edit, and manage user cron jobs using `crontab`.
- Learn the structure and syntax of cron schedules.

## 🧠 Core Concepts Learned   
## Cron and Crontabs
- **Cron** is a background service (**daemon**) that continuously checks for scheduled tasks and executes commands or scripts at the specified times.
- The `cron` daemon checks scheduled jobs every minute and executes any whose schedule matches the current time.
- It is commonly used to automate repetitive system administration tasks such as backups, log rotation, maintenance, and monitoring.
- **Crontab** (Cron Table) is the configuration file that stores scheduled jobs for a user.
- Each user can have their own crontab, allowing them to schedule personal tasks without affecting other users.

### What is a Daemon?
- A **daemon** is a program or process that runs in the background rather than being controlled directly by a user. Daemons typically start automatically when the system boots and continue running until the system shuts down.  

- Common examples include:
    - Scheduling tasks (`cron`)
    - Managing network connections (`sshd`)
    - Logging system events (`rsyslog`)
    - Printing services (`cups`)

- Unlike interactive programs, daemons do not require a user to keep them running.  

## Cron Job Syntax
- A **crontab** is a configuration file that the `cron` daemon reads to determine when commands should be executed.
- Each line in a crontab contains **six fields**: five scheduling fields followed by the command to execute.  

- **Syntax:**   
```text
* * * * * command_to_run
│ │ │ │ │
│ │ │ │ └── Day of the week (0-7)
│ │ │ └──── Month (1-12)
│ │ └────── Day of the month (1-31)
│ └──────── Hour (0-23)
└────────── Minute (0-59)
```

## Wildcards and Step Values
- Cron supports special characters that make scheduling more flexible.

### Wildcards
- The asterisk (`*`) represents **every possible value** for a field.
- **Examples:**
    - `*` in the minute field = every minute.
    - `*` in the month field = every month.

### Step Values
- A forward slash (`/`) specifies intervals.
- **Example:**
```text
*/30 * * * * command
```
- This runs the command **every 30 minutes**.

## Managing Crontabs

| Command | Purpose |  
|---------|---------|  
| `crontab -l` | List the current user's cron jobs. |  
| `crontab -e` | Create or edit the current user's crontab. |  
| `crontab -r` | Remove the current user's crontab. |  
| `systemctl status cron` | Check if the cron service is running. |  
| `sudo systemctl restart cron` | Restart the cron service. |  

## 🛠️ Practical Skills Developed
- Identify the purpose of the `cron` service.
- Explain the difference between `cron` and `crontab`.
- Interpret cron scheduling syntax.
- Read and understand common cron job schedules.
- Recognise common locations used for scheduled tasks.

## 🧰 Tools Used
- TryHackMe platform
- Linux Terminal
- `cron`
- `crontab`

## 🔐 Security Relevance
- Automated tasks are commonly used for backups, log rotation, maintenance, and monitoring.
- Attackers may abuse cron jobs to establish persistence by scheduling malicious scripts.
- Security professionals often inspect cron jobs during incident response and penetration testing.
- Misconfigured cron jobs can introduce privilege escalation or security risks if they execute insecure scripts.

## 📌 Lessons Learned
💡 Cron is the Linux scheduling service, while **crontab** is the configuration used to define scheduled jobs.    
💡 Understanding cron syntax makes it easy to automate repetitive administrative tasks.   
💡 Wildcards (`*`) and step values (`/`) allow flexible scheduling without creating multiple entries.    
💡 Checking cron jobs is an important step during security assessments because they may reveal persistence mechanisms, maintenance scripts, or privilege escalation opportunities.  






