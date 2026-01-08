# 12 – Networking Basics

---

## 🔙 Navigation
⬅️ **Previous:** [11 – Processes and System Info](11-processes-and-system-info.md)  
➡️ **Next:** [13 – Archives and Compression](13-archives-and-compression.md)

---

## 🎯 Objective

After completing this lesson, you will be able to:

- Understand basic networking concepts in Linux  
- Check IP addresses and network interfaces  
- Test network connectivity  
- Monitor open ports and connections  
- Answer exam questions on Linux networking  

---

## 🧠 Basic Networking Concepts

- **IP Address** – Unique address of a device in a network  
- **Subnet Mask** – Defines network portion of IP  
- **Gateway** – Router that connects to the internet  
- **DNS** – Resolves domain names to IP addresses  

---

## 🖥 Viewing Network Interfaces

### 1️⃣ Using `ip` (Recommended)
```bash
ip addr
````

* Shows all network interfaces and their IPs

---

### 2️⃣ Using `ifconfig` (Older method)

```bash
ifconfig
```

* May need installation: `sudo apt install net-tools` (Ubuntu)

---

## 🔌 Testing Network Connectivity

### 1️⃣ `ping` – Check if host is reachable

```bash
ping google.com
```

* Press `Ctrl + C` to stop

---

### 2️⃣ `traceroute` – Path to a host

```bash
traceroute google.com
```

* Shows routers between you and destination
* May need installation: `sudo apt install traceroute`

---

### 3️⃣ `nslookup` – DNS Lookup

```bash
nslookup google.com
```

* Shows IP address of a domain

---

## 📡 Monitoring Network Connections

### 1️⃣ `netstat` – View open connections

```bash
netstat -tuln
```

* `-t` TCP, `-u` UDP, `-l` Listening, `-n` Numeric

---

### 2️⃣ `ss` – Modern alternative to netstat

```bash
ss -tuln
```

* Displays sockets and ports in use

---

### 3️⃣ `curl` – Test URL connectivity

```bash
curl https://www.google.com
```

* Fetches webpage content (basic test)

---

## 📝 Key Exam Notes (Remember This)

* `ip addr` shows IP addresses
* `ping` checks connectivity
* `netstat` / `ss` monitor network connections
* `nslookup` checks DNS resolution
* Linux uses both command-line and GUI tools for networking

---

## ❌ Common Beginner Mistakes

❌ Forgetting `sudo` for some commands
❌ Confusing `ip` and `ifconfig`
❌ Ignoring firewall restrictions
❌ Overusing `ping` on unknown hosts

✅ Always use commands safely

---

## 🧪 Practice Questions (Short Answer)

1. Which command shows network interfaces and IPs?
2. How do you test if google.com is reachable?
3. Which command checks DNS resolution?
4. Name two commands to check open network connections.
5. What does `ping` do?

---

## 🧠 MCQs (Exam-Friendly)

### Q1. Command to view IP addresses in modern Linux:

A) ifconfig
B) ip addr
C) netstat
D) ping

✅ **Answer:** B

---

### Q2. Command to check if a host is reachable:

A) traceroute
B) nslookup
C) ping
D) curl

✅ **Answer:** C

---

### Q3. `netstat -tuln` shows:

A) CPU usage
B) Open network connections
C) Installed packages
D) Disk usage

✅ **Answer:** B

---

### Q4. Command to check DNS resolution:

A) ip addr
B) nslookup
C) curl
D) top

✅ **Answer:** B

---

### Q5. Which command is a modern replacement for netstat?

A) ss
B) ip
C) ping
D) traceroute

✅ **Answer:** A

---

## 🚀 What’s Next?

In the next lesson, you will learn:

👉 **[13 – Archives and Compression](13-archives-and-compression.md)**
(Learn to create and extract `.tar`, `.zip`, and `.gz` files)

---

Happy Learning 🐧🌐

```
