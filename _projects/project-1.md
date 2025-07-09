---
layout: project
title: "PowerShell backup"
description: "Guide to backup files with PowerShell and robocopy."
---

### Overview

This project demonstrates how to back up and restore important data using PowerShell and robocopy.
Screenshots are provided for each step to make the process easy to follow.

### Why Backups Matter

Backups are a really important part of keeping your digital information safe, but they’re often ignored. No matter if you’re a student, a developer, or running a business, data loss can happen at any time and usually without any warning. Data loss can happen for a number of reasons:

- Hardware failure (e.g., a dying hard drive)
- Ransomware or malware attacks
- Accidental deletion or overwriting
- Software bugs
- Natural disasters (flood, fire, etc.)

### Without a backup:
- You risk losing personal files, years of work, or critical business data.
- Recovery may be impossible or extremely costly.
- Even cloud storage isn’t immune — it can be deleted, hacked, or misconfigured.

### How to Backup

Before starting, here are the important data folders we want to protect:

![Important data folders](/assets/images/1.png)

The backup folder is currently empty:

![Empty backup folder](/assets/images/2.png)

---

### Performing the Backup

We use the following PowerShell command to back up the data:

```powershell
robocopy C:\ImportantData D:\Backup /MIR
```

Here’s the command being executed:

![Running robocopy backup](/assets/images/3.png)

After running the command, the backup folder now contains the important data:

![Backup folder with data](/assets/backup-folder-with-data.png)

---

### Simulating Data Loss

Suppose the original data is lost or deleted:

![Data loss screenshot](/assets/images/5.png)

---

### Restoring from Backup

To restore the data, we use this PowerShell command:

```powershell
robocopy D:\Backup C:\ImportantData /MIR
```

Here’s the restore command being executed:

![Running robocopy restore](/assets/images/6.png)

After restoring, the important data folders are back in their original location.

---