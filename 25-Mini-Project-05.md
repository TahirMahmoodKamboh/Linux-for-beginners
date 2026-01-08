# 25 – Mini Project 05 – Networking Basics & SSH

---

## 🔙 Navigation
⬅️ **Previous:** [24 – Mini Project 04](24-Mini-Project-04.md)  
➡️ **Next:** [26 – Mini Project 06](26-Mini-Project-06.md)

---

## 🎯 Objective

This project will help you practice **basic networking commands and SSH** in Linux.  
By the end of this project, you will be able to:

- Check network configuration and connectivity  
- Test connectivity to other machines  
- Use SSH to connect to remote servers  
- Monitor network ports and traffic  

---

## 📂 Project Setup

1. Open your terminal  
2. Create a project directory:
```bash
mkdir ~/mini-project-05
cd ~/mini-project-05
````

---

## 🛠 Tasks

### Task 1 – Check Network Configuration

1. View network interfaces and IP addresses:

```bash
ip addr
```

2. Check routing table:

```bash
ip route
```

3. View DNS servers:

```bash
cat /etc/resolv.conf
```

---

### Task 2 – Test Connectivity

1. Ping a host to check connectivity:

```bash
ping -c 4 google.com
```

2. Test traceroute to see network path:

```bash
traceroute google.com
```

3. Check open ports and listening services:

```bash
ss -tuln
```

---

### Task 3 – SSH Connection to Remote Server

> ⚠️ If you don’t have a remote server, you can SSH to localhost for practice: `ssh $USER@localhost`

1. Connect to remote server:

```bash
ssh username@remote_server_ip
```

2. Exit SSH session:

```bash
exit
```

3. Copy files to remote server using `scp`:

```bash
scp file.txt username@remote_server_ip:~
```

4. Copy files from remote server:

```bash
scp username@remote_server_ip:~/file.txt .
```

---

### Task 4 – Check Network Status

1. View current network connections:

```bash
netstat -tuln
```

2. Monitor live network activity:

```bash
sudo tcpdump -i lo
```

> Tip: Use `Ctrl + C` to stop monitoring

3. Display IP routing and connectivity:

```bash
ping -c 2 8.8.8.8
```

---

### Task 5 – Explore Commands

* Explore network commands using `--help` or `man`:

```bash
man ip
ip --help
man ping
man traceroute
man ssh
man scp
```

---

## ✅ Expected Outcomes

By the end of this project, you should be able to:

* View network interfaces, IP addresses, and routing
* Ping hosts and perform traceroute
* Connect to remote servers using SSH
* Copy files securely between local and remote machines
* Monitor network ports and traffic

---

## 📝 Notes / Tips

* `ssh` is used for secure remote connections
* `scp` is used for secure file transfer
* `ping` checks connectivity; `traceroute` shows the path
* `netstat` and `ss` show open ports and connections
* Always verify IP addresses and network interface names before running commands

---

## 🎯 Learning Outcomes

By completing this project, you will:

* Gain confidence using Linux networking commands
* Learn to test connectivity and troubleshoot network issues
* Connect and manage remote servers securely
* Be ready for more advanced Linux networking and server administration tasks
