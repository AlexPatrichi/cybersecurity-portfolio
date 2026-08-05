# Windows – TryHackMe

Platform: TryHackMe     
Skill Level: Beginner / Foundation     
Focus Area: Registry Editor

## 🎯 Objective
- Understand the purpose of the Windows Registry.
- Learn how the Registry stores system and application settings.
- Understand why the Registry is important to Windows.

## 🧠 Core Concepts Learned
## What is the Windows Registry?
The **Windows Registry** is a hierarchical database that stores configuration settings for the operating system, hardware, user profiles, and installed applications.

Windows continuously reads from the Registry during startup and while the system is running to determine how the operating system and applications should behave.

> Incorrect changes to the Registry can cause system instability or prevent Windows from functioning correctly. Always back up the Registry or create a restore point before making changes.

## Registry Editor
The **Registry Editor (`regedit`)** is the built-in Windows tool used to view and modify the Registry.

Launch it by:
- Start Menu → **Registry Editor**
- **Win + R** → `regedit`

> Administrator privileges may be required to modify certain registry keys.

## Registry Structure
The Registry is organized like a folder structure consisting of: 
- **Hives** are like the main folders.
- **Keys**  - are like folders.
- **Subkeys** - are folders inside other folders.
- **Values** - store the actual settings.

**Example:**

```text
HKEY_CURRENT_USER
└── Control Panel
    └── Desktop
        ├── Wallpaper = C:\wallpaper.jpg
        ├── ScreenSaveActive = 1
        └── WallpaperStyle = 10
```

In this example:
- **HKEY_CURRENT_USER** is the **hive**.
- **Control Panel** is a **key**.
- **Desktop** is a **subkey**.
- **Wallpaper**, **ScreenSaveActive**, and **WallpaperStyle** are **values** that store Windows settings.

## Common Registry Hives
- **HKEY_CURRENT_USER (HKCU)** – Settings for the currently logged-in user.
- **HKEY_LOCAL_MACHINE (HKLM)** – Settings that apply to the entire computer.
- **HKEY_CLASSES_ROOT (HKCR)** – File associations and program information.
- **HKEY_USERS (HKU)** – Settings for all user accounts.
- **HKEY_CURRENT_CONFIG (HKCC)** – Information about the current hardware profile.

## 🛠️ Practical Skills Developed
- Opened and navigated the Registry Editor.
- Explored registry hives, keys, and values.
- Located configuration settings for users and the operating system.
- Learned safe practices for viewing and modifying registry entries.

## 🧰 Tools Used
- Registry Editor (`regedit`)
- TryHackMe platform

## 🔐 Security Relevance
The Windows Registry is frequently targeted during cyber attacks because it can be used to:
- Establish persistence by creating startup entries.
- Store malicious configuration data.
- Disable security features.
- Hide malware execution.

Security analysts often inspect the Registry during forensic investigations to identify persistence mechanisms and signs of compromise.

## 📌 Lessons Learned
💡 The Windows Registry is one of the most important components of Windows. Understanding its structure helps with system administration, troubleshooting, malware analysis, and digital forensics, but changes should always be made carefully.