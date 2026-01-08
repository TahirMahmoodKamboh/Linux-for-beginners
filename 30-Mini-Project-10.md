# 30 – Mini Project 10 – Text Processing & Data Extraction

---

## 🔙 Navigation
⬅️ **Previous:** [29 – Mini Project 09](29-Mini-Project-09.md)  
➡️ **Next:** [31 – Mini Project 11](31-Mini-Project-11.md)

---

## 🎯 Objective

This project will help you practice **text processing and data extraction** in Linux.  
By the end of this project, you will be able to:

- Search for patterns in files using `grep`  
- Extract and manipulate text using `awk` and `sed`  
- Filter and format log or text data  
- Automate text processing tasks with simple commands  

---

## 📂 Project Setup

1. Open your terminal  
2. Create a project directory:
```bash
mkdir ~/mini-project-10
cd ~/mini-project-10
````

3. Create a sample log file `system.log`:

```bash
nano system.log
```

4. Add the following content:

```
Jan 8 10:00:01 server1 sshd[1234]: Accepted password for user1 from 192.168.1.2
Jan 8 10:05:12 server1 sshd[1235]: Failed password for user2 from 192.168.1.3
Jan 8 10:10:45 server1 cron[2345]: Job backup.sh started
Jan 8 10:15:33 server1 sshd[1236]: Accepted password for user3 from 192.168.1.4
Jan 8 10:20:00 server1 systemd[1]: Session closed for user1
```

---

## 🛠 Tasks

### Task 1 – Search for Text Patterns with `grep`

1. Find all SSH login attempts:

```bash
grep sshd system.log
```

2. Find failed login attempts:

```bash
grep "Failed" system.log
```

3. Count the number of cron jobs:

```bash
grep cron system.log | wc -l
```

4. Search case-insensitively:

```bash
grep -i "password" system.log
```

---

### Task 2 – Extract Columns with `awk`

1. Display only usernames from SSH entries:

```bash
grep sshd system.log | awk '{print $9}'
```

2. Display date and time of all entries:

```bash
awk '{print $1, $2, $3}' system.log
```

3. Count occurrences of each username:

```bash
grep sshd system.log | awk '{print $9}' | sort | uniq -c
```

---

### Task 3 – Replace Text Using `sed`

1. Replace "user1" with "admin" in a file:

```bash
sed 's/user1/admin/g' system.log
```

2. Delete lines containing "cron":

```bash
sed '/cron/d' system.log
```

3. Save changes to a new file:

```bash
sed 's/user2/guest/g' system.log > system_modified.log
```

---

### Task 4 – Combine Commands

1. Find failed SSH attempts and extract usernames:

```bash
grep "Failed" system.log | awk '{print $9}'
```

2. Find all SSH attempts and count per user:

```bash
grep sshd system.log | awk '{print $9}' | sort | uniq -c
```

3. Replace a username and save output:

```bash
grep sshd system.log | sed 's/user3/guest/g' > ssh_modified.log
```

---

### Task 5 – Explore Commands

* Explore `grep`, `awk`, `sed` using `--help` or `man`:

```bash
man grep
grep --help
man awk
awk --help
man sed
sed --help
```

---

## ✅ Expected Outcomes

By the end of this project, you should be able to:

* Search and filter text in files using `grep`
* Extract specific columns or fields using `awk`
* Replace, delete, or modify text using `sed`
* Combine commands to automate text processing tasks

---

## 📝 Notes / Tips

* `grep` is ideal for searching patterns
* `awk` is powerful for field-based extraction
* `sed` is useful for in-place text editing or transformations
* Combine commands using pipes (`|`) for efficient data processing
* Always test on sample files before modifying important system files

---

## 🎯 Learning Outcomes

By completing this project, you will:

* Gain confidence in Linux text processing commands
* Learn to extract, format, and manipulate log or text data
* Be able to automate simple text analysis tasks
* Build a foundation for log analysis, scripting, and automation
