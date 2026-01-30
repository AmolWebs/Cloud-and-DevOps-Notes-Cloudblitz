

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


### 📅 29 Jan 2026

#### 🔄 File Concatenation
```bash
cat file1 file2 file3 > file4
```

#### 📦 Package Managers
| Manager | Description | OS / Distro |
| :--- | :--- | :--- |
| `apt` | Advanced Package Tool | Ubuntu |
| `yum` | Yellowdog Updater, Modified | Amazon Linux |
| `dnf` | Dandified YUM | Fedora, Amazon Linux |

#### 🛠️ Editor & Viewing Commands
| Command | Description |
| :--- | :--- |
| `nano <filename>` | Open Nano Editor (Save/Exit: `Ctrl+x` → `y` → `Enter`) |
| `head -n <num> <file>` | Shows first `<num>` of lines |
| `tail -n <num> <file>` | Shows last `<num>` of lines |


### 📅 30 Jan 2026

#### 🛠️ Utility Commands
| Command | Description | Details |
| :--- | :--- | :--- |
| `du -sh <filename>` | Check file size | *Disk Usage* - `s` (Summarize), `h` (Human Readable) |
| `wget <url>` | Download file | Download content from a specific URL |

#### 👥 Types of Users
1. **Root User:** Super User (Home: `/root`)
2. **Normal User:** Local User (Home: `/home`)

#### 📂 Linux File System Hierarchy
**19 Default Directories:**

| Directory | Description |
| :--- | :--- |
| `/root` | Home directory of **Root User** |
| `/home` | Home directory of **Normal User** |
| `/bin` | **Binary** directory (Normal User commands) |
| `/sbin` | **System Binary** directory (Root User commands) |
| `/boot` | **Boot** directory (Boot loader info) |
| `/dev` | **Device** directory (Device info) |
| `/etc` | **Etc** directory (Configuration files, e.g., `os-release`) |
| `/lib` | **Library** directory (Shared library files) |
| `/media` | **Media** directory (Mount point for removable media) |
| `/mnt` | **Mount** directory (Temporary mount points) |
| `/opt` | **Optional** directory (Optional software packages) |
| `/proc` | **Process** directory (System process info) |
| `/run` | **Run** directory (Runtime information) |
| `/srv` | **Service** directory (Data for services provided by system) |
| `/sys` | **System** directory (Kernel & hardware info) |
| `/tmp` | **Temporary** directory (Temp files) |
| `/usr` | **User** directory (User utilities & applications) |
| `/var` | **Variable** directory (Variable files like logs) |
| `/lost+found` | **Lost+Found** directory (Recovered corrupted files) |

note : swap memory : it is a part of RAM which is used as a virtual memory.
