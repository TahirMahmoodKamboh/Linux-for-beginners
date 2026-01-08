# 11 – Processes and System Info

---

## 🔙 Navigation
⬅️ **Previous:** [10 – Package Management](10-package-management.md)  
➡️ **Next:** [12 – Networking Basics](12-networking-basics.md)

---

## 🎯 Objective

After completing this lesson, you will be able to:

- Understand what processes are in Linux
- Monitor running processes
- Check system information like CPU, memory, uptime
- Use basic process management commands
- Answer exam questions related to Linux processes

---

## 🧠 What Is a Process?

A **process** is a program or task that is running on your computer.

- Each process has a **PID (Process ID)**  
- Processes can run in **foreground** or **background**  
- Linux is **multi-tasking**, so many processes run simultaneously

---

## 🔍 Viewing Running Processes

### 1️⃣ `ps` – Process Status
```bash
ps
````

* Shows processes running in the current terminal

```bash
ps aux
```

* Shows **all processes** on the system

---

### 2️⃣ `top` – Real-Time Process Monitoring

```bash
top
```

* Displays CPU, memory usage, and active processes
* Press `q` to quit

---

### 3️⃣ `htop` – Interactive Process Viewer (Optional)

```bash
sudo apt install htop   # Ubuntu/Debian
htop
```

* Easier to read than `top`
* Navigate using arrows

---

## 🖥 System Information Commands

### 1️⃣ `uname` – Kernel and System Info

```bash
uname -a
```

### 2️⃣ `uptime` – System Running Time

```bash
uptime
```

### 3️⃣ `free` – Memory Usage

```bash
free -h
```

* `-h` shows human-readable format

### 4️⃣ `df` – Disk Space Usage

```bash
df -h
```

### 5️⃣ `du` – Directory Space Usage

```bash
du -sh /home/user
```

---

## 📝 Key Exam Notes (Remember This)

* `ps` shows processes
* `top` monitors CPU/memory usage in real-time
* `htop` is an interactive alternative
* `uname -a` shows system/kernel info
* `uptime` shows how long the system has been running
* `free -h` shows RAM usage
* `df -h` shows disk usage

---

## ❌ Common Beginner Mistakes

❌ Running commands without understanding
❌ Closing important processes accidentally
❌ Ignoring CPU/memory usage
❌ Confusing `df` with `du`

✅ Always check carefully before taking action

---

## 🧪 Practice Questions (Short Answer)

1. What is a process?
2. Which command shows running processes in the current terminal?
3. How can you monitor processes in real-time?
4. Which command shows memory usage?
5. What command shows disk space usage?

---

## 🧠 MCQs (Exam-Friendly)

### Q1. Which command shows all processes on the system?

A) ps aux
B) top
C) free
D) df

✅ **Answer:** A

---

### Q2. Command to monitor CPU and memory in real-time:

A) uname
B) top
C) ps
D) du

✅ **Answer:** B

---

### Q3. Which command shows how long the system has been running?

A) uptime
B) free
C) df
D) uname

✅ **Answer:** A

---

### Q4. Command to check RAM usage in human-readable format:

A) df -h
B) free -h
C) du -sh
D) ps aux

✅ **Answer:** B

---

### Q5. What is a PID?

A) Process Index Data
B) Program Input Data
C) Process ID
D) Partition ID

✅ **Answer:** C

---

## 🚀 What’s Next?

In the next lesson, you will learn:

👉 **[12 – Networking Basics](12-networking-basics.md)**
(Checking IP, network connections, and basic network commands)

---

Happy Learning 🐧⚡

```
