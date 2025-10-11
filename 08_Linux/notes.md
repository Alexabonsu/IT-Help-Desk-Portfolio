# Linux Fundamentals  
**Completion Date:** October 9, 2025  
**Status:** Completed  
**Course:** TCM Security Help Desk to SOC Analyst Pathway  

---

## Overview  
This section covers the fundamentals of GNU/Linux, including system setup, command-line navigation, file permissions, user management, and scripting.  

Linux is an open-source operating system built on two main parts:
- **GNU tools** (provide user commands and utilities)  
- **Linux kernel** (controls hardware and system processes)  

It is widely used in cybersecurity, server management, and cloud environments because it is stable, secure, and customizable.

---

## Topics Covered  

### 1. GNU/Linux and Distributions  
- **GNU/Linux** = combination of the GNU project tools and the Linux kernel.  
- **Distributions (Distros)** are complete OS packages built on Linux, e.g.:  
  - **Ubuntu** – user-friendly and ideal for beginners.  
  - **Debian** – highly stable, often used for servers.  
  - **Fedora** – modern features, cutting-edge updates.  
  - **Kali Linux** – security-focused, used in ethical hacking.  

Each distro includes a **package manager** (e.g., `apt`, `yum`, `dnf`) for installing and updating software.

---

### 2. Installing Ubuntu Linux on a Virtual Machine  
- Downloaded **Ubuntu ISO** from [ubuntu.com](https://ubuntu.com)  
- Installed using **Oracle VirtualBox**  
- Configured:
  - 2 GB RAM, 2 CPU cores  
  - Virtual hard disk (20 GB)  
  - NAT network mode for internet access  
- After installation, ran updates:
  ```bash
  sudo apt update && sudo apt upgrade -y
Basic Linux Commands

Familiarized with core terminal commands:

Function	Command	Description
Print current directory	pwd	Shows current working path
List files	ls -la	Lists hidden and visible files
Change directory	cd /path	Moves between directories
Create file	touch filename	Creates an empty file
Create directory	mkdir foldername	Creates a new folder
Delete file/folder	rm file, rm -r folder	Removes files/folders
View file contents	cat, less	Displays file text
Copy/Move files	cp, mv	Copies or moves files
Manual help	man command	Displays command documentation
4. Linux File Permissions

Linux uses Owner–Group–Others structure.
Each file has three types of permissions:

r (read) – view file contents

w (write) – modify or delete

x (execute) – run a file or enter a directory

Example:

chmod 755 script.sh


Gives owner full permissions, group/others read+execute.

5. User Management and Sudo

Created users:

sudo adduser alex
sudo usermod -aG sudo alex


Sudo (Superuser Do): allows limited admin access.

Practiced switching users:

su - alex

6. File System Hierarchy

Common directories:

Path	Description
/home	User directories
/etc	System configuration files
/var	Log files, variable data
/bin	Core system commands
/root	Root user’s home directory
/tmp	Temporary files
7. Bash Scripting

Created a simple automation script:

#!/bin/bash
echo "System update in progress..."
sudo apt update && sudo apt upgrade -y
echo "Update complete!"


Made script executable: chmod +x update.sh

Scheduled automatic execution with cron:

crontab -e
# 0 2 * * * /home/alex/update.sh

8. Package Management

Installed, upgraded, and removed software using apt:

sudo apt install nmap
sudo apt remove nmap
sudo apt autoremove

Practice Record
Date	Task Practiced	Notes
Oct 5, 2025	Installed Ubuntu VM	Verified boot and network setup
Oct 6, 2025	Learned basic terminal commands	Practiced directory navigation
Oct 7, 2025	Configured users and permissions	Tested sudo privileges
Oct 8, 2025	Wrote and scheduled Bash script	Confirmed cron execution
Reflection

I can now:

Navigate and manage Linux file systems confidently

Perform basic administrative tasks

Automate updates and maintenance using scripts

Troubleshoot user and permission issues

This hands-on experience has given me a strong foundation for SOC analyst and IT support roles where Linux is essential.


---

#### 🧩 File 2: `README.md`
```markdown
# Linux Fundamentals

This folder contains my study and practice materials for the **Linux Fundamentals** module, part of the TCM Security Help Desk to SOC Analyst Pathway.

**Topics covered include:**
- Installing Ubuntu Linux in a virtual environment  
- Command-line navigation and file management  
- User administration and file permissions  
- Bash scripting and cron jobs  
- Software package management and updates  

**Objective:**  
To build hands-on Linux administration skills applicable to IT support, SOC, and 
