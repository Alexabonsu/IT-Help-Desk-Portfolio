# 07. Microsoft Windows

---

## Installing Windows 11 on VirtualBox

I downloaded **Windows 11 Enterprise** and installed it using **Oracle VirtualBox** (Type 2 Hypervisor).

### Steps to Set Up Windows 11 on VirtualBox
1. Download the Windows 11 Enterprise ISO.
2. Open **VirtualBox** → click **New**.
3. Enter a **Name** (any name of your choice).
4. Leave the **Folder** as default.
5. Under **ISO Image**, load the Windows 11 ISO you downloaded.
6. Check **Skip Unattended Installation** → click **Next**.
7. Configure **Hardware Settings** (recommended: 8 GB RAM and 4 CPUs).
8. Click **Finish**, select the VM, and click **Start** to power it on.
9. Follow on-screen steps:
   - Choose **United States** as region.
   - Select **Domain Join** when prompted to sign in.
   - Uncheck all privacy settings and click **Accept**.

---

## Finalizing the VM Setup (Guest Additions)

1. Log into the Windows 11 VM.
2. From VirtualBox’s top menu → **Devices → Insert Guest Additions CD Image**.
3. If it doesn’t start automatically:
   - Open **File Explorer** inside the VM.
   - Locate the **CD/DVD drive**.
   - Right-click `VBoxWindowsAdditions-amd64` → **Run as Administrator**.
4. Complete installation → **Reboot now**.
5. After restart:
   - Go to **View → Auto-Resize Guest Display**.
   - To enable full-screen mode, press **Right Ctrl + F** (Host Key + F).

---

## Snapshots: Creating & Restoring Backups

### Create a Snapshot
1. In VirtualBox → select **Machine → Take Snapshot**.
2. Name your snapshot → click **OK**.

### Restore a Snapshot
1. Open **VirtualBox**.
2. Right-click the running VM → choose **Power Off**.
3. Go to the **Snapshots** tab.
4. Select a previous snapshot → click **Restore**.
5. Click **Start** to launch the restored VM.

Snapshots are essential for testing — they let you revert to a clean state anytime.

---

## Local and Domain Accounts

### Local Account
- Stored in the **Security Accounts Manager (SAM)** database.
- Credentials verified **locally**.
- Used on standalone PCs or test environments.  
- Format: `.\username`

### Domain Account
- Stored in **Active Directory (AD)** on a **Domain Controller (DC)**.
- Credentials validated by the domain.
- Used in enterprise environments.  
- Format: `domain\username` or `username@domain.com`

---

## Managing User Accounts

### As a Normal User
1. Open **Settings → Accounts**.
2. Edit or manage user accounts.

### As an Administrator
1. Open **Control Panel → User Accounts**.
2. Use dropdowns to make administrative changes.

---

## Using Local Users and Groups (MMC)

### To Open:
1. Press **Windows + R**, type `lusrmgr.msc`, and hit **Enter**.

You can:
- Create or delete users and groups.
- Add or remove users from groups.
- Set password and account policies.

⚠️ **Note:** Only available on **Windows Pro, Enterprise, or Server editions**.

---

## Add a New Local User via MMC
1. Go to **Users** → Right-click → **New User**.
2. Enter username and password.
3. Click **Create**.

### Add User to Administrator Group
1. Right-click the user → **Properties → Member Of**.
2. Click **Add** → type `Administrators`.
3. Click **Check Names → OK**.
4. Click **Apply**.

---

## 🧾 Ticket Interrupt

**Ticket #456786 – Add user to Windows computer**

**Assigned:** Admin  
**Created:** 07/08/2025  
**Status:** Open  

**Comment:**  
> Please create a local user “Richard” with a password reset on first login.  
> Make the user a local administrator.

**Solution:**
- Follow MMC steps above to add the user and grant admin privileges.

---

## Installing & Uninstalling Applications

**Uninstall:**
1. Open **Control Panel → Programs → Uninstall a program**.
2. Select the program → click **Uninstall** → confirm with **Yes**.

---

## File and Folder Permissions

### To Restrict Access:
1. Open **File Explorer** → select the folder.
2. Right-click → **Properties → Security → Edit**.
3. Click **Advanced → Disable Inheritance**.
4. Remove unwanted entries.
5. Add specific users and assign **Full Control** or **Deny** permissions as needed.

---

## Windows Updates

1. Open **Settings → Windows Update**.
2. Check for updates → install pending patches.

---

## Windows Logs & Event Viewer

**Logs** record system and application events.  
Access via **Event Viewer** (`eventvwr.msc`).

### Main Log Types:
1. **Application Logs** – App errors and crashes.
2. **System Logs** – OS and hardware issues.
3. **Security Logs** – Logins, file access, policy changes.
4. **Setup Logs** – Installation of OS components.
5. **Forwarded Events** – Logs from other computers.

**How to Filter Logs:**
- Open **Event Viewer → Windows Logs → Security**.
- Right-click → **Filter Current Log** → choose severity or time.

---

## Device Manager

1. Open **Device Manager** via Start or **Windows + X**.
2. View hardware devices and drivers.
3. Right-click a device to:
   - Update driver  
   - Uninstall  
   - Scan for hardware changes  

---

## Adding a Network Printer

1. Open **Devices and Printers**.
2. Click **Add a printer**.
3. Let Windows search for network printers.
4. Select and connect.

---

## Windows Task Manager

Shortcut: **Ctrl + Shift + Esc**

Used for:
- Ending frozen apps.
- Viewing system performance.
- Checking resource usage (CPU, RAM, Disk, Network).
- Managing startup programs.

---

## Windows Services

Access via:
- **Start → Services**
- Or **Task Manager → Services tab**

Services handle:
- Networking
- Printing
- Security (Firewall, Windows Defender)
- Updates

Admins use this tool to **start/stop services**, troubleshoot, and monitor system stability.

---

## Windows Registry

- The **Windows Registry** is a database of system and user settings.
- Access via **Start → regedit**.

**Registry Hives:**
- **HKLM** – System-wide settings.
- **HKCU** – Current user settings.
- **HKCR** – File associations.

⚠️ Always back up before editing registry values.

---

## Command Prompt (CMD)

CLI tool for Windows administration.

### Useful Commands
| Command | Description |
|----------|-------------|
| `systeminfo` | View OS version, uptime, and patches. |
| `whoami` | Display logged-in user. |
| `net user` | List all user accounts. |
| `ipconfig /all` | View full network config. |
| `ping <IP>` | Test connectivity. |
| `netstat -ano` | View active connections and process IDs. |
| `tasklist` | List running processes. |
| `taskkill /PID <pid> /F` | Kill a process. |

**Run CMD as Admin:**
- Search “cmd” → Right-click → **Run as administrator**.

---

## Task Scheduler

Used to **automate repetitive tasks**.

**Launch:** Search **Task Scheduler** in Start Menu.

**Key Components:**
- **Task:** The action performed.
- **Trigger:** Event or time that starts the task.
- **Action:** What it executes.
- **Conditions:** Optional limits (e.g., on AC power).
- **History:** Success/failure logs.

### Example Practice:
Created a task for **Disk Cleanup**:
1. **General tab:** “Run a disk cleanup of temporary files.”
2. **Triggers tab:** Set to run daily.
3. **Actions tab:** Command: `cleanmgr`  
   Argument: `/SAGERUN:n`

---

## Knowledge Base (KB)
Example: **KB5020044** — a Microsoft Knowledge Base article for a Windows update or fix.

---

> 💡 *Windows administration is a cornerstone of IT support and SOC analysis — understanding how to configure, secure, and troubleshoot the system forms the base of all advanced cybersecurity operations.*

