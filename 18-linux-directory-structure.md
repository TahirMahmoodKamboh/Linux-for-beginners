# 18 – Linux Directory Structure

---

## 🔙 Navigation
⬅️ **Previous:** [17 – Logs and Monitoring](17-logs-and-monitoring.md)  
➡️ **Next:** [19 – Common Linux Mistakes](19-common-linux-mistakes.md)

---

## 🎯 Objective

After completing this lesson, you will be able to:

- Understand the Linux filesystem hierarchy  
- Identify the purpose of common directories  
- Navigate and explore directories safely  
- Answer exam questions on Linux directory structure  

---

## 🧠 Linux Filesystem Hierarchy

Linux uses a **single-rooted hierarchical directory structure**, starting from `/` (root).

- `/` → Root directory  
- All other directories are subdirectories under `/`  

---

## 📂 Important Directories

| Directory | Purpose |
|-----------|---------|
| `/bin` | Essential command binaries (e.g., `ls`, `cp`) |
| `/sbin` | System binaries (admin commands like `ifconfig`, `shutdown`) |
| `/boot` | Boot loader files, kernel images |
| `/dev` | Device files (hardware like `/dev/sda`, `/dev/tty`) |
| `/etc` | System configuration files (e.g., `passwd`, `hosts`) |
| `/home` | Users’ home directories (e.g., `/home/rocky`) |
| `/root` | Home directory of the root user |
| `/lib` | Essential shared libraries |
| `/usr` | User programs and utilities (`/usr/bin`, `/usr/lib`) |
| `/usr/local` | Locally compiled and installed programs |
| `/var` | Variable files like logs, spool, databases |
| `/tmp` | Temporary files |
| `/opt` | Optional add-on software packages |
| `/media` | Mount points for removable media (USB, CD) |
| `/mnt` | Temporary mount points for filesystems |
| `/srv` | Data for services (web server, FTP, etc.) |

---

## 🔍 Navigating the Directory Structure

### 1️⃣ View Current Directory
```bash
pwd
````

### 2️⃣ List Contents

```bash
ls
ls -l
ls -a
```

### 3️⃣ Change Directory

```bash
cd /etc
cd ~         # Go to home
cd -         # Go to previous directory
```

### 4️⃣ Explore Directories Safely

```bash
ls /bin
ls /usr/bin
ls /var/log
```

---

## 📝 Key Exam Notes (Remember This)

* `/` → root
* `/bin` and `/sbin` → essential binaries
* `/home` → regular users’ home
* `/etc` → system configuration
* `/var` → logs, spool, variable files
* `/tmp` → temporary files
* `/usr` → user programs, `/usr/local` → locally installed programs
* `/boot` → boot files
* `/dev` → devices

---

## ❌ Common Beginner Mistakes

❌ Modifying system files in `/etc` without backup
❌ Deleting files in `/bin` or `/sbin`
❌ Confusing `/root` with `/home/root`
❌ Storing permanent files in `/tmp`

✅ Always check directory purpose before making changes

---

## 🧪 Practice Questions (Short Answer)

1. What is the root directory in Linux?
2. Where are user home directories stored?
3. Which directory contains system configuration files?
4. Where are log files usually stored?
5. Difference between `/usr` and `/usr/local`?

---

## 🧠 MCQs (Exam-Friendly)

### Q1. Which directory contains essential user commands like `ls` and `cp`?

A) /usr
B) /bin
C) /etc
D) /var

✅ **Answer:** B

---

### Q2. Where is the root user’s home directory?

A) /home/root
B) /root
C) /usr/root
D) /etc/root

✅ **Answer:** B

---

### Q3. Which directory stores system configuration files?

A) /etc
B) /var
C) /opt
D) /tmp

✅ **Answer:** A

---

### Q4. Where should temporary files be stored?

A) /tmp
B) /var
C) /home
D) /usr/local

✅ **Answer:** A

---

### Q5. `/usr/local` is used for:

A) Kernel modules
B) Locally compiled programs
C) System logs
D) Device files

✅ **Answer:** B

---

## 🚀 What’s Next?

In the next lesson, you will learn:

👉 **[19 – Common Linux Mistakes](19-common-linux-mistakes.md)**
(Learn the pitfalls beginners often encounter and how to avoid them)

---

Happy Learning 🐧📁

```
