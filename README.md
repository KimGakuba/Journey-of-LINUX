# NGABONZIZA Kim Gakuba
---
This covers:

* Bash scripting
* Permissions & ownership
* Data storage
* Cybersecurity in Linux
* Users & groups management

---

# 🟢 LEVEL 1 — Beginner (Foundations)

Focus: Understand basic Linux commands and simple scripting.

---

## 1️⃣ Bash Scripting – Basics

### Learn:

* `echo`
* `pwd`
* `ls`
* `cd`
* `mkdir`
* `rm`
* `touch`
* Variables
* Simple input (`read`)
* Basic `if` statement

### Example Script:

```bash
#!/bin/bash

echo "Enter your name:"
read name
echo "Hello $name"
```

### GitHub Project Idea:

📁 `01-basic-bash`

* hello.sh
* calculator.sh (basic 2-number addition)
* system-info.sh (print date, user, hostname)

---

## 2️⃣ Permissions & Ownership – Basics

### Learn:

* `ls -l`
* `chmod`
* `chown`
* Permission types:

  * `r` = read
  * `w` = write
  * `x` = execute
* Numeric permissions:

  * 7 = rwx
  * 6 = rw-
  * 5 = r-x
  * 4 = r--

### Practice:

```bash
chmod 755 script.sh
```

### Mini Project:

Create a script that:

* Creates a directory
* Sets it to `700`
* Explains why only owner can access it

Push as:
📁 `02-permissions-basics`

---

## 3️⃣ Users & Groups – Basics

### Learn:

* `adduser`
* `useradd`
* `groupadd`
* `usermod`
* `/etc/passwd`
* `/etc/group`

### Practice:

* Create user `developer`
* Create group `projectteam`
* Add user to group

```bash
sudo useradd developer
sudo groupadd projectteam
sudo usermod -aG projectteam developer
```

Push:
📁 `03-users-groups-basics`

---

## 4️⃣ Data Storage – Basics

### Learn:

* `df -h`
* `du -sh`
* `lsblk`
* `mount`
* `umount`

### Concept:

* Filesystem
* Partition
* Block device

Mini Practice:

* Create a loop device
* Mount it to `/mnt/test`

Push:
📁 `04-storage-basics`

---

## 5️⃣ Linux Cybersecurity – Basics

### Learn:

* `whoami`
* `who`
* `history`
* `passwd`
* SSH basics
* Disable root SSH login

Edit:

```
/etc/ssh/sshd_config
```

Push:
📁 `05-linux-security-basics`

---

# 🟡 LEVEL 2 — Intermediate (Real System Management)

Now we combine concepts.

---

## 1️⃣ Bash – Intermediate

### Learn:

* Loops (`for`, `while`)
* Functions
* Exit codes
* Arguments (`$1`, `$2`)
* Case statement
* Cron jobs

Example:

```bash
#!/bin/bash

if [ $# -ne 1 ]; then
    echo "Usage: $0 filename"
    exit 1
fi

if [ -f $1 ]; then
    echo "File exists"
else
    echo "File not found"
fi
```

Mini Project:
📁 `06-backup-script`

* Backup folder daily
* Save with timestamp
* Log output to file

---

## 2️⃣ Permissions – Advanced

### Learn:

* SUID
* SGID
* Sticky bit
* `umask`

Example:

```bash
chmod +s file
chmod 1777 /shared
```

Mini Project:
📁 `07-secure-shared-directory`

* Create shared folder
* Only owner can delete files
* Group can write

---

## 3️⃣ Users & Groups – Advanced

### Learn:

* Password policies
* `/etc/shadow`
* Expiring accounts
* Lock/unlock users

Commands:

```bash
passwd -l username
chage -l username
```

Mini Project:
📁 `08-user-management-system`
Create script:

* Add user
* Assign group
* Set password expiration
* Force password change

---

## 4️⃣ Data Storage – Intermediate

### Learn:

* LVM (Logical Volume Manager)
* `pvcreate`
* `vgcreate`
* `lvcreate`
* Resize partitions
* Swap management

Mini Project:
📁 `09-lvm-project`

* Create physical volume
* Create volume group
* Create logical volume
* Resize it

---

## 5️⃣ Linux Cybersecurity – Intermediate

### Learn:

* `iptables` / `ufw`
* Fail2ban
* SSH key authentication
* Disable password login
* File integrity tools

Mini Project:
📁 `10-server-hardening`

* Enable firewall
* Configure SSH keys
* Install fail2ban
* Log suspicious activity

---

# 🔴 LEVEL 3 — Advanced (Junior SysAdmin / Security Engineer Level)

Now we move to real-world automation and security.

---

## 1️⃣ Bash – Advanced Automation

### Learn:

* Parsing logs
* Monitoring services
* Error handling
* Trap signals
* Systemd services
* JSON parsing (`jq`)

Mini Project:
📁 `11-monitoring-system`
Script:

* Check CPU usage
* Check disk usage
* Check memory
* Send alert if > 80%
* Log everything

---

## 2️⃣ Advanced Permissions & Security

### Learn:

* ACL (Access Control Lists)
* `setfacl`
* `getfacl`
* SELinux / AppArmor basics

Mini Project:
📁 `12-acl-security`

* Give user access to file without changing group
* Restrict others
* Document explanation

---

## 3️⃣ Data Storage – Advanced

### Learn:

* RAID concepts
* `mdadm`
* Filesystem tuning
* Disk encryption (`LUKS`)
* `cryptsetup`

Mini Project:
📁 `13-encrypted-storage`

* Create encrypted partition
* Mount at boot
* Secure it with passphrase

---

## 4️⃣ Linux Cybersecurity – Advanced

### Learn:

* Auditd
* Log analysis
* Brute force detection
* Rootkit detection
* File permissions auditing

Mini Project:
📁 `14-security-audit-tool`
Create script:

* Find world-writable files
* Detect users with UID 0
* Check SUID binaries
* Export report

---

## 5️⃣ Complete Final Project (Portfolio Level)

📁 `15-linux-mini-enterprise-server`

Build:

* Create users for departments
* Create groups
* Secure shared directories
* Setup firewall
* Enable SSH keys only
* Daily automated backup
* Monitoring script
* Log auditing
* LVM storage
* Encrypted backup partition


---

---
