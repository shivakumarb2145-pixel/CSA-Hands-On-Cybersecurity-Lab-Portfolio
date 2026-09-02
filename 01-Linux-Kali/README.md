# Linux & Kali Linux Fundamentals

## Overview

Hands-on Linux and Kali Linux exercises completed during CSA training. The sessions focused on Linux system navigation, file management, process monitoring, networking commands, user management, permissions, services, package management, and basic command-line investigation.

## Topics Practiced

- Kali Linux desktop and application navigation
- Linux filesystem structure
- File and directory management
- Process and system monitoring
- Network configuration and connectivity
- Text and file processing
- Searching for files
- Linux users and passwords
- File permissions
- Linux services
- Package management
- Privilege management

## Linux Filesystem

Practiced navigating and understanding common Linux directories:

```text
/
├── root
├── bin
├── usr
├── home
├── sbin
├── etc
├── lib
├── var
├── opt
├── tmp
└── media
System and Process Commands

Commands practiced during the sessions:

whoami
id
hostname
uname -a
ps
ps aux
top
htop

These were used to examine the current user, system information, running processes, and system resource activity.

Network Commands

Practiced basic network configuration and connectivity commands:

ifconfig
ip a
ping
File and Directory Management

Practiced creating, viewing, modifying, copying, moving, and deleting files and directories:

pwd
ls
ls -l
ls -a
cd
cd ..
cd -
touch
cat
cat -n
head
tail
mkdir
cp
mv
rm
rmdir
rm -r
truncate -s 0

Also used:

mousepad
nano

for creating and editing files.

Text Processing

Practiced combining Linux commands for basic text analysis:

sort
uniq
grep
grep -i
cut
awk
wc

Also practiced pipes and output/error redirection.

Example:

command | grep pattern
File Searching

Practiced locating files using:

find
locate
sudo updatedb

Also practiced redirecting unwanted error output to:

/dev/null
Linux Users and Privileges

Practiced basic user-management operations:

adduser
userdel
userdel -r
passwd

Practiced privilege management using:

sudo
sudo su
File Permissions

Studied Linux read, write, and execute permissions for:

User
Group
Others

Practiced modifying permissions using chmod, including symbolic and numeric permission modes.

Services

Practiced controlling Linux services:

service [name] start
service [name] stop
service [name] status
service [name] restart
System Files

Worked with important Linux system files including:

/etc/os-release
/etc/passwd
/etc/shadow
Package Management

Practiced package management using APT:

apt
sudo apt update

Also practiced package removal using:

remove
purge

Learning Outcome 

Developed practical familiarity with the Linux command line and Kali Linux environment, including system administration,
process monitoring, network troubleshooting, file operations, user management, permissions, services,
and basic command-line investigation.
