# 🐧 Linux Command Cheat Sheet
### Quick Revision Guide for DevOps Engineers

A clean and practical **Linux command reference** for daily usage, DevOps tasks, and interview revision.

---

# 📌 Linux File System Structure

```
/
├── bin      Essential binaries
├── boot     Boot loader files
├── dev      Device files
├── etc      Configuration files
├── home     User directories
├── lib      Shared libraries
├── media    External media
├── mnt      Mount points
├── opt      Optional packages
├── proc     Process information
├── root     Root user home
├── run      Runtime data
├── sbin     System binaries
├── tmp      Temporary files
├── usr      User programs
└── var      Logs and variable files
```

---

# 📂 File & Directory Commands

| Command | Description |
|------|-------------|
| pwd | Print current directory |
| ls | List files |
| ls -l | Detailed list |
| ls -a | Show hidden files |
| cd directory | Change directory |
| cd .. | Move one level up |
| cd ~ | Go to home directory |
| mkdir dir | Create directory |
| rmdir dir | Remove empty directory |
| rm file | Delete file |
| rm -r dir | Delete directory |
| rm -rf dir | Force delete directory |

---

# 📄 File Operations

| Command | Description |
|------|-------------|
| touch file.txt | Create file |
| cp file1 file2 | Copy file |
| cp -r dir1 dir2 | Copy directory |
| mv file newfile | Rename file |
| mv file dir/ | Move file |
| cat file | Display file |
| less file | Scroll file |
| head file | First lines |
| tail file | Last lines |
| tail -f log | Live log monitoring |

---

# 🔎 Search Commands

| Command | Description |
|------|-------------|
| find / -name file.txt | Find file |
| find . -type f | Find files |
| find . -type d | Find directories |
| grep word file | Search word |
| grep -i word file | Ignore case |
| grep -r word dir | Recursive search |
| locate filename | Fast search |

---

# 📊 Disk & System Information

| Command | Description |
|------|-------------|
| df -h | Disk usage |
| du -sh * | Folder size |
| free -m | Memory usage |
| top | Process monitor |
| htop | Advanced monitor |
| uptime | System uptime |
| uname -a | OS details |

---

# 👥 User Management

| Command | Description |
|------|-------------|
| whoami | Current user |
| id | User information |
| adduser username | Create user |
| passwd username | Change password |
| userdel username | Delete user |
| groupadd groupname | Create group |
| groups | Show groups |

---

# 🔐 File Permissions

Example permission:

```
-rwxr-xr--
```

| Symbol | Meaning |
|------|------|
| r | Read |
| w | Write |
| x | Execute |

Numeric permissions:

| Number | Permission |
|------|-------------|
| 7 | rwx |
| 6 | rw- |
| 5 | r-x |
| 4 | r-- |

Examples:

```
chmod +x script.sh
chmod 755 script.sh
chmod 644 file.txt
chown user file
chown user:group file
```

---

# 📦 Package Management

### Ubuntu / Debian

```
sudo apt update
sudo apt upgrade
sudo apt install nginx
sudo apt remove nginx
```

### RedHat / CentOS

```
sudo yum install nginx
sudo yum remove nginx
sudo dnf install nginx
```

---

# 🌐 Networking Commands

| Command | Description |
|------|-------------|
| ip a | Show IP address |
| ping google.com | Test connectivity |
| curl url | Fetch webpage |
| wget url | Download file |
| netstat -tulnp | Show ports |
| ss -tulnp | Modern netstat |
| traceroute google.com | Network path |

---

# ⚙️ Process Management

| Command | Description |
|------|-------------|
| ps | Show processes |
| ps aux | Detailed process list |
| top | Live monitoring |
| kill PID | Kill process |
| kill -9 PID | Force kill |
| pkill name | Kill by name |
| bg | Resume background |
| fg | Bring to foreground |

---

# 📦 Archive & Compression

| Command | Description |
|------|-------------|
| tar -cvf file.tar dir | Create archive |
| tar -xvf file.tar | Extract archive |
| tar -czvf file.tar.gz dir | Compress |
| tar -xzvf file.tar.gz | Extract gzip |
| zip file.zip file | Create zip |
| unzip file.zip | Extract zip |

---

# 📜 Log Monitoring (DevOps Important)

```
tail -f /var/log/syslog
```

```
journalctl -u nginx
```

```
journalctl -xe
```

---

# ⚡ Terminal Shortcuts

| Shortcut | Description |
|------|-------------|
| Ctrl + C | Stop process |
| Ctrl + Z | Pause process |
| Ctrl + A | Start of line |
| Ctrl + E | End of line |
| Ctrl + R | Search command |

---

# 📜 Command History

```
history
```

Run command again

```
!10
```

Search history

```
history | grep docker
```

---

# 🚀 DevOps Useful Commands

Monitor disk usage every 2 seconds

```
watch -n 2 df -h
```

Monitor containers

```
watch docker ps
```

Check port usage

```
lsof -i :8080
```

Run process in background

```
nohup command &
```

---

# ⭐ Pro Tips

Create alias

```
alias ll="ls -la"
```

Reload shell

```
source ~/.bashrc
```

---

# 🎯 Linux Interview Revision Checklist

- [ ] File system navigation
- [ ] File permissions
- [ ] Process management
- [ ] Networking commands
- [ ] Disk monitoring
- [ ] Package installation
- [ ] Log monitoring
- [ ] User management
- [ ] File search

---

# 🧠 DevOps Tip

Before mastering:

- Docker
- Kubernetes
- CI/CD
- Terraform
- AWS

You must master **Linux fundamentals first**.

---

🔥 Golden Rule

> Strong Linux knowledge = Strong DevOps Engineer