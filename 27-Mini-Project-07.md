# 27 – Mini Project 07 – Cron Jobs & Task Automation

---

## 🔙 Navigation
⬅️ **Previous:** [26 – Mini Project 06](26-Mini-Project-06.md)  
➡️ **Next:** [28 – Mini Project 08](28-Mini-Project-08.md)

---

## 🎯 Objective

This project will help you practice **automating tasks using cron jobs** in Linux.  
By the end of this project, you will be able to:

- Understand the cron scheduling system  
- Create and manage cron jobs  
- Automate repetitive tasks using scripts  
- Verify and troubleshoot scheduled tasks  

---

## 📂 Project Setup

1. Open your terminal  
2. Create a project directory:
```bash
mkdir ~/mini-project-07
cd ~/mini-project-07
````

---

## 🛠 Tasks

### Task 1 – Create a Simple Script

1. Create a script `backup.sh`:

```bash
nano backup.sh
```

2. Add the following content:

```bash
#!/bin/bash
# This script creates a backup of the Documents directory
DATE=$(date +%F_%H-%M-%S)
mkdir -p ~/backup
cp -r ~/Documents ~/backup/Documents_$DATE
echo "Backup completed at $DATE"
```

3. Save and exit, then make it executable:

```bash
chmod +x backup.sh
```

4. Test the script:

```bash
./backup.sh
```

✅ Expected Outcome:

* A backup folder is created with a timestamped copy of `~/Documents`

---

### Task 2 – View Current Cron Jobs

1. List current user cron jobs:

```bash
crontab -l
```

2. If no jobs exist, it will say “no crontab for <user>”

---

### Task 3 – Schedule a Cron Job

1. Open crontab for editing:

```bash
crontab -e
```

2. Add a job to run `backup.sh` every day at 2 AM:

```cron
0 2 * * * /home/<your_username>/mini-project-07/backup.sh
```

3. Save and exit the editor

4. Verify scheduled job:

```bash
crontab -l
```

---

### Task 4 – Test Cron Job Manually

* Simulate cron job execution by running:

```bash
bash ~/mini-project-07/backup.sh
```

✅ Expected Outcome:

* Backup is created with timestamp
* Output message confirms completion

---

### Task 5 – Redirect Output to Log File

1. Edit cron job to log output:

```cron
0 2 * * * /home/<your_username>/mini-project-07/backup.sh >> /home/<your_username>/mini-project-07/backup.log 2>&1
```

2. Check log file:

```bash
cat ~/mini-project-07/backup.log
```

✅ Expected Outcome:

* Cron job output and errors are logged for review

---

### Task 6 – Explore Commands

* Explore cron and scheduling commands:

```bash
man crontab
crontab --help
man cron
```

* Check running cron service:

```bash
systemctl status cron       # Debian/Ubuntu
systemctl status crond      # RHEL/CentOS/Fedora
```

---

## ✅ Expected Outcomes

By the end of this project, you should be able to:

* Write scripts for automated tasks
* Schedule cron jobs to run at specific times
* Verify, test, and troubleshoot cron jobs
* Log output and errors from automated tasks

---

## 📝 Notes / Tips

* Cron uses the format: `minute hour day month weekday command`
* Use absolute paths in scripts to avoid errors in cron
* Always test scripts manually before scheduling
* Logs help troubleshoot why cron jobs may not run as expected

---

## 🎯 Learning Outcomes

By completing this project, you will:

* Gain practical experience in task automation
* Learn to schedule recurring tasks with cron
* Understand the interaction between scripts and cron
* Build a foundation for system maintenance and automation tasks
