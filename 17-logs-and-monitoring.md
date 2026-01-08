# 17 – Logs and Monitoring

---

## 🔙 Navigation
⬅️ **Previous:** [16 – Environment Variables](16-environment-variables.md)  
➡️ **Next:** [18 – Linux Directory Structure](18-linux-directory-structure.md)

---

## 🎯 Objective

After completing this lesson, you will be able to:

- Understand Linux log files and their purpose  
- Locate important logs in `/var/log`  
- View and filter logs using standard commands  
- Monitor system resources in real-time  
- Answer exam questions on Linux logs and monitoring  

---

## 🧠 Why Are Logs Important?

Linux logs are **crucial for system monitoring, troubleshooting, and security**:

- Track system activity and errors  
- Detect security breaches or unauthorized access  
- Diagnose hardware or software problems  
- Monitor services and applications  

Most important logs are in `/var/log` and its subdirectories.

---

## 📂 Core System Logs

| Log File | Description | Distribution |
|----------|-------------|--------------|
| `/var/log/syslog` | Global system activity data and non-kernel errors | Debian/Ubuntu |
| `/var/log/messages` | Similar to syslog, contains general messages | RHEL/CentOS |
| `/var/log/kern.log` | Kernel events, errors, and warnings | Debian/Ubuntu |
| `dmesg` | Kernel ring buffer (similar to kern.log) | All |
| `/var/log/boot.log` | Messages produced during system startup | All |

---

## 🔒 Security and Authentication Logs

| Log File | Description |
|----------|-------------|
| `/var/log/auth.log` | Security events, user logins, root actions (Debian/Ubuntu) |
| `/var/log/secure` | Security events (RHEL/CentOS) |
| `/var/log/faillog` | Failed login attempts |
| `/var/log/wtmp` | Binary file maintaining login/logout history (`who` or `last` command to view) |

---

## ⚙ Service and Application Logs

| Log File / Directory | Description |
|---------------------|-------------|
| `/var/log/cron.log` or `/var/log/cron` | Scheduled tasks (cron jobs) |
| `/var/log/mail.log` or `/var/log/maillog` | Mail server logs (Postfix, Sendmail) |
| `/var/log/httpd/` or `/var/log/apache2/` | Web server access and error logs |
| `/var/log/mysql/` or `/var/log/mariadb/` | Database server logs |

---

## 🖥 Modern Linux Systems (`systemd`)

- Logs managed by `journald` in **binary format**  
- Primary tool: `journalctl`  
- Provides **powerful filtering capabilities** for recent events  
- Traditional `/var/log` files are still accessible  

---

## 🔍 How to View Logs

### 1️⃣ `cat` – View entire file
```bash
cat /var/log/syslog
````

### 2️⃣ `less` / `more` – Scrollable view

```bash
less /var/log/syslog
more /var/log/syslog
```

### 3️⃣ `tail` – Last few lines

```bash
tail /var/log/syslog
tail -f /var/log/syslog  # Real-time monitoring
```

### 4️⃣ `grep` – Search within logs

```bash
grep "error" /var/log/syslog
```

### 5️⃣ `journalctl` – View systemd logs

```bash
journalctl                # All logs
journalctl -u ssh.service # Logs for specific service
journalctl -b             # Logs from current boot
journalctl -f             # Real-time updates (like tail -f)
```

---

## 📈 Monitoring System Resources

### 1️⃣ `top` – Real-time process and resource monitor

```bash
top
```

* Displays CPU, memory, and active processes
* Press `q` to exit

### 2️⃣ `htop` – Interactive process monitor (optional)

```bash
sudo apt install htop
htop
```

### 3️⃣ `dmesg` – Kernel messages

```bash
dmesg
dmesg | less
```

* Useful for hardware and driver troubleshooting

---

## 📝 Key Exam Notes (Remember This)

* Logs are mainly in `/var/log`
* Core logs: syslog/messages, kern.log, boot.log
* Security logs: auth.log / secure, faillog, wtmp
* Service logs: cron, mail, web server, database
* Commands: `cat`, `less`, `more`, `tail`, `grep`, `journalctl`
* Monitoring: `top`, `dmesg`

---

## ❌ Common Beginner Mistakes

❌ Ignoring log permissions (some logs require `sudo`)
❌ Modifying logs directly
❌ Using `tail` without `-f` for real-time monitoring
❌ Forgetting to check service-specific logs

✅ Always read logs safely and use filtering commands

---

## 🧪 Practice Questions (Short Answer)

1. Where are most Linux logs stored?
2. Command to view the last 10 lines of a log?
3. Which log tracks failed login attempts?
4. Command to view kernel messages?
5. How do you monitor active processes in real-time?

---

## 🧠 MCQs (Exam-Friendly)

### Q1. Which directory stores most Linux logs?

A) /etc
B) /var/log
C) /home
D) /usr/log

✅ **Answer:** B

---

### Q2. Command to view real-time updates of syslog:

A) tail -f /var/log/syslog
B) cat /var/log/syslog
C) less /var/log/syslog
D) grep error /var/log/syslog

✅ **Answer:** A

---

### Q3. Command to view systemd journal logs:

A) journalctl
B) dmesg
C) top
D) env

✅ **Answer:** A

---

### Q4. Which log records SSH login attempts (Debian/Ubuntu)?

A) /var/log/syslog
B) /var/log/auth.log
C) /var/log/kern.log
D) /var/log/boot.log

✅ **Answer:** B

---

### Q5. Which command shows CPU and memory usage in real-time?

A) dmesg
B) top
C) journalctl
D) cat

✅ **Answer:** B

---

## 🚀 What’s Next?

In the next lesson, you will learn:

👉 **[18 – Linux Directory Structure](18-linux-directory-structure.md)**
(Learn the purpose of common Linux directories like `/etc`, `/usr`, `/home`, `/var`, etc.)

---

Happy Learning 🐧📊

```
