# Linux Notes

## Commands
- > ls -a `shows hidden directories`
- > bash `use to refresh terminal`


### Day 1
[1.1]AWS Account Creation : Create an AWS account and use console to make ec2 instance and there run this below commands in terminal.


[1.2]Types of Path => 
ex. directory path 
> /root/home/code
- consider you are in /home and want to go in /code directory
- [1.21]1] Absolute Path 
    > cd /root/home/code
- [1.22]2] Relative Path 
    > cd code

***
### [1.3]Get OS Information 
- [1.31]To see OS Information of a system use cmd -> cat /etc/os-release
- another way to go there -> cd / -> cd etc -> cat os-release



### Without cd we can see the content inside the directory refer [1.31]

### Some Commands
- [1.4] Root Access Command 
- > sudo -i

- [1.5] Parent Command => 
- > mkdir -p project/next/live 

- It creates directory inside directory and if you "ls" this it gives "project" directory. without -p it is not possible.

- [1.6] Tree Command : It is use to see the heirarchy of the directores.
To install : 
- > apt update -y
- > apt install tree -y
- > tree

 ### Day 2
 [2.1] **cal command** => This command use to see calender -> syntax :
 - > cal 2026 `This cmd shows entire year's calender`
 - > cal 05 2028 `This shows calender of month 5 of 2028`

[2.2] **Linux Directory System**
- *There is 19 Default Directories*
- [2.21] Root Directory(/) :
    - To go in this directory : use cmd 
         > sudo -i `user called root user. full form of sudo : super user do`
- [2.22] Home Directory(/home) :
    - it shows normal user ex. Ubuntu, Amol, Hp, etc.
    > sudo su `su for switch user. You can change user which in inside root directory. It took you to home directory of that local user`
- [2.23] /etc 
    - It stores all configurations files of system and services.

- [2.24] /bin
    - It stores binary files, binary file means nothing but our commands(local user commands)

- [2.25] /sbin
    - Stores binary executable files, commands (root user commands)

- [2.26] /var
    - it stores variables data such as mail, logs, messages, caches, etc.

- [2.27] /lib
    - library file information, support 32 bit commands

- [2.28] /lib64
    - support 64 bit cmds.

- [2.29] /boot 
    - stores info about boot loader

- [2.210] /dev
    - stores info about usb drives, printer

- [2.211]  /media
    - stores info about removable devices, card reader, pendrive, floopy disk

- [2.212] /sys
    - stores kernel information

- [2.213] /proc
    - RAM and CPU info

- [2.214] /tmp
    - stores temp files for 10 days

- [2.215] /usr
    - user relates information. also stores manual pages.

- [2.216] /srv
    - service related info

- [2.217] /mnt
    - stores mount point for storage devices. ex- hard disk

- [2.218] 
- [2.219]

### [2.3]Common Shortcuts

[2.31] ~ 
[2.32] Create alias of any command : 
> alias createfolder='mkdir'

    