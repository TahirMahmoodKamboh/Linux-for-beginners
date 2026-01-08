# 19 – Common Linux Mistakes

---

## 🔙 Navigation
⬅️ **Previous:** [18 – Linux Directory Structure](18-linux-directory-structure.md)  
➡️ **Next:** [20 – Practice Exercises](20-practice-exercises.md)

---

## 🎯 Objective

After completing this lesson, you will be able to:

- Identify common mistakes Linux beginners make  
- Understand the consequences of these mistakes  
- Learn best practices to avoid errors  
- Answer exam questions on Linux pitfalls  

---

## 🧠 Common Beginner Mistakes

### 1️⃣ Running Commands as Root Unnecessarily
- Mistake: Using `sudo` for every command  
- Risk: Can modify system files accidentally  
- Best Practice: Only use `sudo` when required  

### 2️⃣ Ignoring File Permissions
- Mistake: Modifying files without checking permissions  
- Risk: Breaks system or causes security issues  
- Best Practice: Use `ls -l` to check permissions, `chmod` carefully  

### 3️⃣ Confusing Relative and Absolute Paths
- Mistake: Using `cd bin` instead of `/bin`  
- Risk: End up in wrong directory, run wrong commands  
- Best Practice: Know your current directory (`pwd`)  

### 4️⃣ Editing System Files Without Backup
- Mistake: Editing `/etc/passwd` or `/etc/hosts` directly  
- Risk: System misconfiguration or boot failure  
- Best Practice: Always backup files before editing  
```bash
cp /etc/hosts /etc/hosts.bak
````

### 5️⃣ Misusing Package Managers

* Mistake: Installing unnecessary packages, ignoring updates
* Risk: Conflicts or system bloat
* Best Practice: Use `apt update && apt upgrade` (Debian/Ubuntu) or `yum update` (RHEL/CentOS) carefully

### 6️⃣ Ignoring Logs

* Mistake: Not checking `/var/log` or `journalctl`
* Risk: Missed errors, security breaches
* Best Practice: Monitor logs regularly

### 7️⃣ Deleting Important Files

* Mistake: Using `rm -rf /` or similar commands
* Risk: Irreversible system damage
* Best Practice: Double-check paths before deleting, use `--dry-run` or test on safe directories

### 8️⃣ Forgetting Command Options

* Mistake: Running commands like `cp` or `tar` without proper options
* Risk: Data loss or incomplete tasks
* Best Practice: Read `man` pages (`man cp`) or use `--help`

### 9️⃣ Not Using Tab Completion

* Mistake: Typing full file or directory names manually
* Risk: Typos and errors
* Best Practice: Use `Tab` key for auto-completion

### 🔟 Ignoring Shell History

* Mistake: Not reviewing previous commands (`history`)
* Risk: Repeating mistakes, inefficiency
* Best Practice: Use `history` to learn from past commands

---

## 📝 Key Exam Notes (Remember This)

* Use `sudo` **only when necessary**
* Always check file permissions before editing
* Backup important files before modifying
* Monitor logs and system messages
* Use `man` and `--help` to understand commands
* Practice safe deletion with `rm`
* Tab completion and history are your friends

---

## 🧪 Practice Questions (Short Answer)

1. Why is it dangerous to use `sudo` unnecessarily?
2. How can you avoid breaking system files?
3. What is the importance of checking logs?
4. How can you safely remove files or directories?
5. Which tools help prevent typos while typing file names?

---

## 🧠 MCQs (Exam-Friendly)

### Q1. Which practice is safest when editing system files?

A) Edit directly without backup
B) Backup the file first
C) Use `sudo` blindly
D) Ignore permissions

✅ **Answer:** B

---

### Q2. Which command helps you read the manual of a command?

A) help
B) man
C) info
D) guide

✅ **Answer:** B

---

### Q3. What is the risk of using `rm -rf /` accidentally?

A) Deletes home directory only
B) Deletes entire filesystem, system may fail
C) Creates a backup
D) Only removes temporary files

✅ **Answer:** B

---

### Q4. Which key helps prevent typing mistakes in filenames?

A) Esc
B) Tab
C) Ctrl + C
D) Enter

✅ **Answer:** B

---

### Q5. Which command shows your previous commands?

A) tail
B) history
C) echo
D) ps

✅ **Answer:** B

---

## 🚀 What’s Next?

In the next lesson, you will learn:

👉 **[20 – Practice Exercises](20-practice-exercises.md)**
(Hands-on exercises to reinforce Linux fundamentals)

---

Happy Learning 🐧⚠️
