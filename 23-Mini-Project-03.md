# 23 – Mini Project 03 – Text Manipulation & Log Monitoring

---

## 🔙 Navigation
⬅️ **Previous:** [21 – Mini Project 02](21-Mini-Project-02.md)  
➡️ **Next:** [24 – Mini Project 04](24-Mini-Project-04.md)

---

## 🎯 Objective

This project will help you practice **text file manipulation and system log monitoring** in Linux.  
By the end of this project, you will be able to:

- Read and search files  
- Filter log files using commands  
- Monitor logs in real-time  
- Use basic text processing commands (`grep`, `cat`, `tail`, `less`)  

---

## 📂 Project Setup

1. Open your terminal  
2. Create a project directory:
```bash
mkdir ~/mini-project-03
cd ~/mini-project-03
````

---

## 🛠 Tasks

### Task 1 – Create Sample Log File

1. Create a sample log file `system.log`:

```bash
nano system.log
```

2. Add the following sample content:

```
Jan 8 10:00:01 server1 systemd[1]: Started Session 1 of user root.
Jan 8 10:05:12 server1 sshd[2345]: Accepted password for user1 from 192.168.1.2
Jan 8 10:10:45 server1 cron[3456]: Job `backup.sh` started
Jan 8 10:15:33 server1 sshd[2345]: Failed password for user2 from 192.168.1.3
Jan 8 10:20:00 server1 systemd[1]: Stopped Session 1 of user root.
```

3. Save and exit

---

### Task 2 – View File Content

* Use `cat` to display the file:

```bash
cat system.log
```

* Use `less` for scrollable view:

```bash
less system.log
```

* Use `head` and `tail`:

```bash
head -n 3 system.log   # First 3 lines
tail -n 3 system.log   # Last 3 lines
```

---

### Task 3 – Search Specific Entries

* Find all SSH login attempts:

```bash
grep sshd system.log
```

* Find failed login attempts:

```bash
grep "Failed" system.log
```

* Count the number of SSH entries:

```bash
grep -c sshd system.log
```

---

### Task 4 – Monitor Log File in Real-Time

1. Open a new terminal
2. Use `tail -f` to monitor log entries:

```bash
tail -f system.log
```

3. In the original terminal, append a new log entry:

```bash
echo "Jan 8 10:25:00 server1 sshd[2346]: Accepted password for user3 from 192.168.1.4" >> system.log
```

4. Observe the update in real-time on the monitoring terminal

---

### Task 5 – Filter and Extract Information

* Display only timestamps of failed logins:

```bash
grep "Failed" system.log | awk '{print $1, $2, $3}'
```

* Extract usernames from SSH entries:

```bash
grep sshd system.log | awk '{print $9}'
```

* Count all cron jobs:

```bash
grep cron system.log | wc -l
```

---

### Task 6 – Explore Commands

* Explore these commands using `--help` or `man`:

```bash
grep --help
tail --help
head --help
awk --help
less --help
```

---

## ✅ Expected Outcomes

By the end of this project, you should be able to:

* View and navigate large text files
* Search and filter content efficiently using `grep` and `awk`
* Monitor log files in real-time using `tail -f`
* Extract meaningful information from system logs
* Understand basic log structure

---

## 📝 Notes / Tips

* `grep` searches for patterns in files
* `awk` allows extracting specific fields from text
* `tail -f` is essential for live monitoring of logs
* Always test commands on sample files before using on real system logs

---

## 🎯 Learning Outcomes

By completing this project, you will:

* Gain practical experience with **file viewing and searching**
* Learn **log monitoring techniques** used in real Linux environments
* Understand how to **extract and analyze data** from text files
* Be prepared for more advanced scripting and automation projects

---

Next, we can create **Project 04**, which could focus on **process management, system info, and resource monitoring**, building on the knowledge from Project 03.

---

Happy Learning 🐧📄
