# 24 – Mini Project 04 – Process Management & System Monitoring

---

## 🔙 Navigation
⬅️ **Previous:** [23 – Mini Project 03](23-Mini-Project-03.md)  
➡️ **Next:** [25 – Mini Project 05](25-Mini-Project-05.md)

---

## 🎯 Objective

This project will help you practice **process management and system monitoring** in Linux.  
By the end of this project, you will be able to:

- View running processes  
- Check CPU and memory usage  
- Monitor system resources in real-time  
- Manage processes safely (kill, stop, or check status)  

---

## 📂 Project Setup

1. Open your terminal  
2. Create a project directory:
```bash
mkdir ~/mini-project-04
cd ~/mini-project-04
````

---

## 🛠 Tasks

### Task 1 – View Running Processes

1. Use `ps` to see current processes:

```bash
ps aux
```

2. Filter processes for your user:

```bash
ps -u $USER
```

3. Display top 10 processes by memory:

```bash
ps aux --sort=-%mem | head -n 10
```

---

### Task 2 – Monitor System in Real-Time

1. Use `top` to monitor CPU, memory, and processes:

```bash
top
```

* Press `q` to exit
* Press `M` to sort by memory usage
* Press `P` to sort by CPU usage

2. Use `htop` if installed for a better interface:

```bash
htop
```

---

### Task 3 – Check Memory and Disk Usage

1. Check memory usage:

```bash
free -h
```

2. Check disk usage:

```bash
df -h
```

3. Check directory size:

```bash
du -sh ~/
```

---

### Task 4 – Kill or Stop Processes

1. Find process ID (PID) of a command, e.g., `sleep`:

```bash
sleep 300 &
ps aux | grep sleep
```

2. Kill the process:

```bash
kill <PID>
```

3. Force kill if it doesn’t stop:

```bash
kill -9 <PID>
```

4. Stop a process temporarily:

```bash
kill -STOP <PID>
kill -CONT <PID>   # resume
```

---

### Task 5 – System Logs and Messages

1. View boot messages:

```bash
dmesg | less
```

2. View recent logs:

```bash
tail -n 20 /var/log/syslog    # Debian/Ubuntu
tail -n 20 /var/log/messages  # RHEL/CentOS
```

3. Filter for errors:

```bash
grep -i error /var/log/syslog
```

4. Monitor logs in real-time:

```bash
tail -f /var/log/syslog
```

---

### Task 6 – Explore Commands

* Explore `ps`, `top`, `free`, `df`, `du`, `kill`, `dmesg` using `--help` or `man`:

```bash
man ps
ps --help
man top
top --help
```

---

## ✅ Expected Outcomes

By the end of this project, you should be able to:

* List and filter running processes
* Monitor CPU, memory, and disk usage in real-time
* Kill or stop processes safely
* Read system logs for errors and information
* Understand and use basic system monitoring commands

---

## 📝 Notes / Tips

* `ps` shows snapshots of processes; `top` shows dynamic, real-time info
* Use `kill` carefully; do not kill critical system processes
* `free -h` provides a human-readable overview of memory
* Logs in `/var/log` are critical for troubleshooting

---

## 🎯 Learning Outcomes

By completing this project, you will:

* Gain confidence managing processes and resources
* Learn to monitor CPU, memory, and disk usage efficiently
* Understand system logs and their importance
* Be ready for more advanced Linux administration tasks
