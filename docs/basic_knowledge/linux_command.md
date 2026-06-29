## What is Linux?

Linux is a free, open-source operating system (like Windows or macOS) initially created in 1991 by Linus Torvalds. It manages computer hardware and software resources. Because anyone can modify its code, it powers everything from smart devices and Android phones to global servers and supercomputers


## What are Linux commands?

**Linux commands** are simple text instructions used to control and operate the Linux system through the terminal.

Instead of clicking with a mouse, you type commands to:

* open files
* manage folders
* check system info
* monitor network
* analyze logs


## Why Linux basic commands are important

Linux commands are very important because:

* 🖥️ **Most servers run on Linux**
* 🔐 **SOC analysts use Linux for log analysis and investigations**
* 🌐 **Cybersecurity tools mostly work on Linux**
* 📁 **System files and logs are easily accessible in Linux**
* ⚡ **Faster control than GUI (graphical interface)**


## Simple examples

* `ls` → see files in a folder
* `cd` → change directory
* `cat` → read a file
* `ps` → check running processes
* `netstat` → check network connections


## SOC Analyst point of view

In SOC (Security Operations Center), Linux is used to:

* analyze server logs
* detect suspicious activity
* monitor network traffic
* investigate attacks


## One-line definition

> **Linux commands are text-based instructions used to operate and manage a Linux system efficiently, especially important in servers and cybersecurity environments.**

---
Here are some **basic Linux commands** every beginner should know:

## 📁 File & Directory Commands

* `ls -alh` → list all files (hidden + permissions + human readable)
* `pwd` → show current directory path
* `cd -` → go to previous directory
* `cd ~` → go to home directory
* `mkdir -p dir1/dir2` → create nested directories
* `tree /path` → show directory structure

---

## 📄 File Operations

* `touch file.txt` → create empty file
* `cp -a file1 file2` → copy with permissions preserved
* `mv file1 file2` → move or rename file
* `rm -rf folder` → force delete file/folder
* `rsync -av source/ dest/` → sync files safely

---

## 📖 View Files

* `cat file.txt` → show file content
* `less file.txt` → view file page by page
* `head -n 20 file.txt` → first 20 lines
* `tail -n 50 file.txt` → last 50 lines
* `tail -f /var/log/syslog` → live log monitoring

---

## 🔍 System Info

* `whoami` → current user
* `uname -r` → kernel version
* `uname -a` → full system info
* `htop` → real-time process monitoring
* `df -h` → disk usage
* `du -sh *` → folder size details
* `free -h` → memory usage
* `journalctl -b` → system boot logs

---

## 🔐 Permissions

* `chmod 755 file` → change file permissions
* `chmod -R 700 folder` → recursive permission change
* `chown user:group file` → change owner and group
* `ls -l` → check permissions
* `stat file` → detailed file information

---

## 🌐 Network

* `ip a` → show IP address details
* `ifconfig` → network interface info (older command)
* `ping google.com` → test connectivity
* `netstat -tulnp` → show open ports and services
* `ss -tulnp` → modern alternative to netstat
* `curl website.com` → fetch web data
* `curl -I https://example.com` → show HTTP headers
* `nslookup google.com` → DNS lookup
* `tcpdump -i eth0` → capture network packets

---
## 🔍 Search or Find (File or Directory)

* `find / -name file.txt` → search file by name in whole system
* `find /home -type f -name "*.log"` → find all log files
* `find / -type d -name myfolder` → search directory by name
* `find /var/log -type f -mtime -1` → files modified in last 24 hours
* `find / -type f -size +100M` → find large files (>100MB)

---

* `locate file.txt` → fast search using database
* `updatedb` → update locate database

---

* `grep "error" file.txt` → search text inside a file
* `grep -r "failed password" /var/log/` → search text in all files (recursive)
* `grep -i "error" file.txt` → case-insensitive search

---

* `which python` → find location of a command/tool
* `whereis nginx` → find binary, source, and manual location

---

### 🧠 SOC Tip

Linux commands are very important for SOC Analyst because logs, network analysis, and server monitoring are mostly done in Linux systems.
