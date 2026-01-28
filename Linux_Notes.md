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

## 🚀 New Batch Notes

### 📅 23 Jan 2026
- **Shell Differences:**
  - `sh`: Displays a minimal prompt (`$` or `#`).
  - `bash`: Displays full context (e.g., `root@ip-172-31-40-2:~#`).

### 📅 24 Jan 2026
#### 🔌 EC2 Connection Steps
1. **EC2 Instance Connect** (Browser).
2. **PowerShell / SSH:**
   - Copy the "SSH Client" link.
   - Open PowerShell in the key's directory.
   - Paste command.

#### 🖥️ Linux Prompt Explanation
`root@ip-172-31-40-2:~#`
- **User:** `root`
- **Host:** `ip-blah-blah`
- **Path:** `~` (Home)
- **Privilege:** `#` (Root) vs `$` (User)

#### 📝 Daily Commands
| Command | Description |
| :--- | :--- |
| `pwd` | Print Present Working Directory |
| `ls` | List files/dirs (*Blue=Dir, White=File*) |
| `sudo -i` | Switch to Root user |
| `sudo su` | Switch to Root (maintain current shell env) |
| `touch filename` | Create an empty file |
| `touch file{1..5}`| Create multiple files |
| `clear` | Clear terminal screen |
| `init 0` | Shutdown system |

### 📅 27 Jan 2026
> **Tip:** Manage Payment Preferences
> *Billing and Cost Management -> Preferences -> Payment Preferences*

#### 🆕 Commands
| Command | Description |
| :--- | :--- |
| `mkdir` | Create an empty directory |
| `history` | View command history |
| `history -c` | Clear history |
| `ctrl + c` | Cancel/Kill process |
| `q` | Quit viewer |
| `ls -l` | Long detailed list |
| `ls -a` | Show hidden files |
| `mkdir .<name>` | Create hidden directory (is used for all other means for `touch` and multi file or directory creation) |
| `lsblk` | View block devices (hard disk info) |
| `df -h` | View disk space usage (human readable) |
| `free` | View memory information |
| `free -h` | View RAM info (human readable) |
| `free -m` | View RAM info in MB |
| `free -g` | View RAM info in GB |
| `free -k` | View RAM info in KB |
| `man <command>` | View manual for a command |

#### ⚠️ Remove & Delete Commands
**Flags Explained:**
- **`-r`**: Recursive (creates/deletes inside directories).
- **`-f`**: Forcefully (no confirmation).
- **`-v`**: Verbose (shows action details).

| Command | Description |
| :--- | :--- |
| `rmdir <dirname>` | Remove directory |
| `rm` | Remove Empty File |
| `rm -r` | Remove Non-empty Directory or file |
| `rm -rf` | Remove Non-empty Directory or file forcefully |
| `rm -rf /*` | **DANGER:** Remove all files and directories (Do not use) |
| `rm -f` | Remove file forcefully |
| `mkdir directory -v` | Create directory with verbose output |

> **Note on Navigation:**
> If you do `ls -a` you will see first 2 list items as `. ..`.
> - `.` : Current directory
> - `..` : Previous directory path

#### 🧱 Command Syntax
**Structure:** `Command` + `Argument` + `Option`

**Example:**
```bash
> ls -l
```
- **Command:** `ls`
- **Argument:** `-`
- **Option:** `l`

> *Always syntax is made up of command, argument and option.*


### 📅 28 Jan 2026

#### 📂 Path in Linux
- **1) Absolute Path:** Full path from root.
  - *Example:* `/root/home/code`
- **2) Relative Path:** Path from current directory.
  - *Example:* `code`

#### 📝 File Operations
| Command | Description |
| :--- | :--- |
| `cat` | Concatenate files and print on the standard output |
| `cat > filename` | Create a file |
| `cat >> filename` | Append to a file |
| `cat < filename` | Read a file |
| `cat < filename > newfilename` | Copy a file |
| `echo "hello it is text" > filename` | Create a file and append text to it |
| `echo "hello it is text" >> filename` | Append to a file |
| `echo "hello it is text" < filename` | Read a file |
| `echo "hello it is text" < filename > newfilename` | Copy a file |
| `cp <source> <destination>` | Copy a file |
| `mv <source> <destination>` | Use for move and rename file |
| `mv <oldname> <newname>` | Rename file |

#### ⚙️ System Information
| Command | Description |
| :--- | :--- |
| `lscpu` | View CPU information |
| `hostname` | View hostname |
| `hostname <newname>` | Set hostname temporary |
| `hostnamectl` | View hostname and other information |
