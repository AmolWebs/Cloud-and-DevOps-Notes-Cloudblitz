# 🐧 Linux Master Notes

## 🛠️ Essential Commands
| Command | Description |
| :--- | :--- |
| `ls -a` | Shows hidden directories |
| `bash` | Use to refresh terminal |
|`sudo - ubuntu`| switch to ubuntu user|
|`sudo - i`| switch to root user|
|`sudo - su`| switch to root user|
|`w`| see all users |
|`whoami`| see current user |

---

## 📅 Day 1

### ☁️ [1.1] AWS Account Creation
1. Create an AWS account.
2. Use the console to launch an EC2 instance.
3. Connect and run commands in the terminal.

### 📂 [1.2] Types of Path
**Example Directory:** `/root/home/code`

| Type | Description | Example Command |
| :--- | :--- | :--- |
| **Absolute Path** | Full path from root | `cd /root/home/code` |
| **Relative Path** | Path from current directory | `cd code` (if in `/home`) |

### ℹ️ [1.3] Get OS Information
- **View OS Info:**
  ```bash
  cat /etc/os-release
  # Alternative: cd / -> cd etc -> cat os-release
  ```
- **View Content:** You can list directory contents without entering them.

### ⚡ Utility Commands
- **[1.4] Root Access:**
  ```bash
  sudo -i
  ```
- **[1.5] Parent Command (Recursive Directory Creation):**
  ```bash
  mkdir -p project/next/live
  ```
  > Creates `project` -> `next` -> `live`. Without `-p`, this fails if parent directories don't exist.

- **[1.6] Tree Command:** *View directory hierarchy*
  ```bash
  apt update -y
  apt install tree -y
  tree
  ```

---

## 📅 Day 2

### 🗓️ [2.1] Calendar (`cal`)
```bash
cal 2026      # Shows entire year 2026
cal 05 2028   # Shows May 2028
```

### 📁 [2.2] Linux Directory System
*There are 19 Default Directories*

| Directory | Description |
| :--- | :--- |
| **`/` (Root)** | The starting point. Use `sudo -i` (*Super User Do*) to access. |
| **`/home`** | Home for normal users (e.g., Ubuntu, Amol). |
| **`/etc`** | Stores configuration files for system and services. |
| **`/bin`** | Stores binary files (common user commands). |
| **`/sbin`** | Stores system binary files (root commands). |
| **`/var`** | Variable data (logs, mail, messages, caches). |
| **`/lib`** | Shared library files (supports 32-bit commands). |
| **`/lib64`** | Shared library files (supports 64-bit commands). |
| **`/boot`** | Stores boot loader information. |
| **`/dev`** | Device files (USB drives, printers). |
| **`/media`** | Mount points for removable media (SD cards, pendrives). |
| **`/sys`** | Kernel system information. |
| **`/proc`** | RAM and CPU information. |
| **`/tmp`** | Temporary files (stored for ~10 days). |
| **`/usr`** | User-related programs and manual pages. |
| **`/srv`** | Service-related data. |
| **`/mnt`** | Mount points for storage devices (e.g., hard disk). |

### ⌨️ [2.3] Common Shortcuts
- **`~` (Tilde):** Represents the user's home directory.
- **Create Alias:**
  ```bash
  alias createfolder='mkdir'
  ```

---