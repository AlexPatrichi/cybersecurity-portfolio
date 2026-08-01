# Windows – TryHackMe

Platform: TryHackMe    
Skill Level: Beginner / Foundation   
Focus Area: Settings and the Control Panel

## 🎯 Objective
- Understand the purpose of the Windows Settings app and Control Panel.
- Learn when to use each interface for system configuration.
- Learn how to locate installed applications and common system settings.

### Settings vs Control Panel
Windows provides two main interfaces for configuring the operating system:

- **Settings**
  - Modern configuration interface introduced in **Windows 8**.
  - Designed to be user-friendly and touch-screen compatible.
  - Primary location for most everyday system settings in Windows 10 and later.

- **Control Panel**
  - Traditional Windows management interface.
  - Provides access to more advanced and legacy configuration options.
  - Still required for certain administrative tasks.

💡 Some configuration tasks begin in **Settings** but redirect to the **Control Panel** to access advanced options.

### Installed Applications
Installed software can be viewed through:

```text
Control Panel → Programs → Programs and Features
```

This displays information such as:
- Application name
- Publisher
- Version

This is useful for verifying what software is installed on a system.

### Finding Settings
Both **Settings** and **Control Panel** can be opened from the **Start Menu**.

Instead of manually navigating menus, Windows Search can quickly locate specific settings by searching for keywords (e.g., *wallpaper*, *network*, *printers*).

## 🛠️ Practical Skills Developed
- Navigated both the Settings app and Control Panel.
- Located installed programs using **Programs and Features**.
- Observed how some Settings options open Control Panel windows.
- Used the Start Menu search to quickly find configuration options.

## 🧰 Tools Used
- TryHackMe platform
- Windows Settings
- Control Panel
- Programs and Features
- Start Menu Search

## 🔐 Security Relevance
- Reviewing installed applications helps identify unauthorized or potentially unwanted software.
- Knowing where system settings are located enables administrators to configure security-related options efficiently.
- Many legacy administrative and security settings are still managed through the Control Panel.

## 📌 Lessons Learned
💡 Windows uses both the **Settings** app and the **Control Panel** to manage system configuration. Settings is the modern interface for everyday tasks, while the Control Panel remains essential for advanced and legacy system management.