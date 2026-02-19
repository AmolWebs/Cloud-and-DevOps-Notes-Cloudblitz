Note : To see text in colored format use `| jq` at the end of command

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


### 📅 10 Feb 2026 (Day 12)

#### 🔐 User Permissions & Scripts
- **User Permission**
- **Shell Script:** Create file with `.sh` extension and run it using `./filename.sh`

#### 🔗 [VIMP] Link File
**Types:**
1. **Hard Link**
2. **Soft Link**

**Definitions:**
| Type | Description |
| :--- | :--- |
| **Hard Link** | Copies all content of the file and creates a new file with the same content. Increases link count. |
| **Soft Link (Symbolic Link)** | Creates a shortcut to the file. Doesn't change link count. |

> **Assignment:** What is Inode number?

#### 🛡️ Sudoers
`sudoers`: Used for local users to run any command as a root user. It is a file which contains the list of users who can run any command as a root user.

---

### 🔙 Backlog - Day 7: Vim

---

### 📅 Linux Revision (Day 13)

---

### 📅 Linux: Day 14

#### 🔍 Search and Utilities
- `sort`: Command used to sort text files on the basis of ASCII.

| Command | Description |
| :--- | :--- |
| `sort -r <filename>` | Sort in **descending** order |
| `grep <pattern> <filename>` | Search pattern in a file |
| `history \| grep setuser` | Show commands in history containing "setuser" |

---

### 📅 Linux: Day 15

#### ⚙️ Process Management
**Definition:** Process means an execution of a program by CPU.

| Command | Description |
| :--- | :--- |
| `sleep <seconds>` | Sleep PC for specified seconds |
| `ps -elf` | Show all processes in long format |
| `&` | Run process in background (e.g., `sleep 100 &`) |

#### ⚖️ Priority (Nice & Renice)
> **Interview Question:** What is nice and renice value?

- **Nice Value:** Ranges from `-20` to `19`.
  - `-20`: Higher Priority
  - `19`: Lower Priority
- **Renice:** Used to change priority of existing process by changing its nice value.

#### 🛑 Kill Commands
`kill`: Used to stop process.

| Command | Description |
| :--- | :--- |
| `kill -9 <pid>` | Kill process **forcefully** |
| `kill -1 <pid>` | Kill process **gracefully** |
| `kill 15 <pid>` | Kill process **gracefully** |

#### 📊 Monitoring
| Command | Description |
| :--- | :--- |
| `top` | Shows task manager information |
| `htop` | Shows information in color |

---

### 📅 Linux Revision (Day 16)

#### 👤 Users and Permissions in Linux
- **`useradd`**: To create user.
- **Note:** When you create a user, a group of that name is also created.

**UID ranges:**
- **Root User:** `0`
- **System User:** `1` to `999`
- **Normal User:** `1000` to `65535` (GID is same as UID)

**User & Group Information:**
| Command | Description |
| :--- | :--- |
| `cat /etc/passwd` | See all **users** of the system |
| `cat /etc/group` | See all **groups** of the system |
| `cat /etc/shadow` | See **password** of user |
| `cat /etc/gshadow` | See **group password** |

**User Creation Options:**
| Flag | Description |
| :--- | :--- |
| `-m` | Create home directory |
| `-c` | Add comment |
| `-s` | Specify shell |
| `-a` | Append user in existing group |

**Examples:**
```bash
# Create user by root
useradd -m username
passwd username

# Change password (by self)
passwd

# Change password (by root)
passwd username
```

#### 👥 Groups
1.  **Primary Group:** Created automatically with user creation.
    -   Custom Primary Group: `useradd -u <customUserid> -g <groupid> username` or `useradd -m -g <groupname> username`
2.  **Secondary Group:**

**Group Management:**
| Command | Description |
| :--- | :--- |
| `usermod` | Add user to group |
| `gpasswd -d <username> <groupname>` | Delete user from group |
| `userdel <username>` | Delete user |
| `userdel -r <username>` | Delete user with home directory |

#### 🏠 Normal User Home Default Directory files
(Visible with `ls -l` in home)
- `.bashrc`: user can't login
- `.bash_profile`: user won't give environment to run commands
- `.bash_logout`: user won't give logout commands
- `.profile`: user won't give login and environment commands

> **Note:** Refer no.9 PPT for group specification.

#### 📦 Archive and Compression

**1. Archive (`tar`)**
- Tool: `tar` (Take Archive) to create tar compression.

| Command | Description |
| :--- | :--- |
| `tar -cvf <filename.tar> <files...>` | **Create** archive |
| `tar -xvf <filename.tar>` | **Extract** archive |
| `tar -xvf <filename.tar> -C <path>` | Extract to specific location |
| `du -sh <filename.tar>` | Check storage size |

*Flags:* `c` (create), `x` (extract), `v` (verbose), `f` (file), `C` (change dir)

**2. Compression**
Used to save files in lower size.

| Tool | Skill | Speed | Extension | Example Ratio | Extraction Command |
| :--- | :--- | :--- | :--- | :--- | :--- |
| `gzip` | Low | Fast | `.gz` | 100MB -> 80MB | `gunzip filename.gz` |
| `bzip2` | Medium | Medium | `.bz2` | 100MB -> 50MB | `bunzip2 filename.bz2` |
| `xz` | High | Slow | `.xz` | 100MB -> 20MB | `unxz filename.xz` |

**Combined Commands (Archive + Compress):**
| Format | Command |
| :--- | :--- |
| **gzip** | `tar -cvzf filename.tar.gz file1 file2...` |
| **bzip2** | `tar -cvjf filename.tar.bz2 file1 file2...` |
| **xz** | `tar -cvJf filename.tar.xz file1 file2...` |

#### ⏲️ Crontab
Tool used for automation and job scheduling.

**Setup:**
- `crontab -e`: Set cron tab
- `timedatectl`: See system time
- `timedatectl set-ntp false`: Change it
- `timedatectl set-time '12:00:00'`: Set current time

**Syntax:** `* * * * * command`
1.  **Minute** (0-59)
2.  **Hour** (0-23)
3.  **Day of Month** (1-31)
4.  **Month** (1-12)
5.  **Day of Week** (0-6)

#### 🏗️ Linux Architecture
**4 Layers:**
`Hardware` -> `Kernel` -> `Shell` -> `Application`

**Recap Topics:**
- Archive & Compression
- Linux Architecture
- Nice & Renice
- Process
- User Creation & Permission Management

---

### 📅 Linux: Day 17 (Networking)

#### 🌐 Networking Basics
- **Types of Network:** LAN, WAN, MAN

**Address Types:**
| Type | Full Form | Characteristics |
| :--- | :--- | :--- |
| **Physical** | MAC (Media Access Control) | Hexadecimal, 128 bit, Unique, Non-changeable |
| **Logical** | IP (Internet Protocol) | Unique, Changeable |

**Concepts:**
- **Intranet:** Private Net
- **Backbone Cable:** Used for different Bus Topological Arrangements (e.g., Star, Ring)

**Devices:**
- **HUB:**
    - Unicast (1 to 1), Multicast (1 to many), Broadcast (1 to all).
    - Simplex, Half Duplex, Full Duplex.
- **Switch:**
    - Intelligent device.
    - Initially broadcasts "hello" message to all connected devices.
    - One time broadcast, then unicast.

**IPv4 Structure:**
- Classfull: A, B, C (for us), D (multicasting), E (for R & D, ex. NASA, ISRO).
- Format: `0.0.0.0` (4 Octets, 8 bits each).

---

### 📅 17 Feb 2026 (Day 18)

#### 🔢 IP Classes & Ranges
| Class | Format | Example | Note |
| :--- | :--- | :--- | :--- |
| **A** | `Net : Host : Host : Host` | `10.255.255.255` | - |
| **B** | `Net : Network : Host : Host` | `172.16.255.255` | Here second network value can change upto 15. |
| **C** | `Net : Network : Network : Host` | `192.168.1.255` | Here either third or fourth value can be Network. |
| **D** | - | - | Multicasting |
| **E** | - | - | R & D |

*Notes from text:*
- `0.0.0.0/0`: Anywhere Internet Path.
- `127.0.0.0` - `127.255.255.255`: Loopback Address.

**Public vs Private IP:**
| Public | Private | Public |
| :--- | :--- | :--- |
| `10.0.0.0` | `10.0.0.0` | `10.0.0.0` |
| `172.16.0.0` | `172.16.0.0` | `172.16.0.0` |
| `192.168.0.0` | `192.168.0.0` | `192.168.0.0` |

> Remaining: IP Subnetting.

#### 📶 TCP/IP Model
**4 Layers:**
1.  **Application Layer**
2.  **Transport Layer**
3.  **Internet Layer**
4.  **Network Access Layer**

#### 🏗️ OSI Model
*(1984 by ISO - International Organization for Standardization)*
`(Source/Receiver) 💻 ------- 💻 (Destination/Receiver)`

1.  **Physical Layer:** Hardware
2.  **Data Link Layer:** Error Handling, Framing, MAC Address Matching, Flow Control, Access Control (Hardware)
3.  **Network Layer:** Routing, Logical Addressing, Path Determination (Hardware)
4.  **Transport Layer:** Heart of the model
5.  **Session Layer**
6.  **Presentation Layer:** Software
7.  **Application Layer**

> **Assignment:**
> 1. All imp ports and protocols for cloud computing.
> 2. What is Firewall and how it works.

**Utility:**
`ifconfig`: To see all information about IP, Loopback Address.


### Day 19 (18 Feb 2026) 
Basic introduction about 'what is cloud and it's benefits'


### 📅 Day 20 (19 Feb 2026)

- **Cloud Services:** IaaS, PaaS, SaaS
- **Deployment Models:** Public, Private, Hybrid (combination of public and private cloud), Community Cloud

#### 🌍 AWS Global Infrastructure

1. **Region:** An AWS Region is a geographically separate location that contains multiple Availability Zones where AWS resources are deployed.
   - There are total 39 regions in world out of which 4 regions takeen by china and usa for their internal governemnt activity.
   - 17 regions needs permissions from AWS to access.
   - 18 regions are publically available.