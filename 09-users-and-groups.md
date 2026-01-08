# 09 – Users and Groups

---

## 🔙 Navigation
⬅️ **Previous:** [08 – File Permissions](08-file-permissions.md)  
➡️ **Next:** [10 – Package Management](10-package-management.md)

---

## 🎯 Objective

After completing this lesson, you will be able to:

- Understand Linux users and groups
- Identify root vs normal users
- Learn basic user management commands
- Understand sudo and its importance
- Answer exam questions on users and groups

---

## 🧠 What Are Users in Linux?

Linux is a **multi-user operating system**, which means:

- Multiple people can use the system at the same time
- Each user has a **username** and **home directory**
- Each user has a **UID** (User ID)

---

### 1️⃣ Root User

- Superuser with **full permissions**
- Can do anything (install, remove, change ownership)
- Symbol: `#` in terminal prompt

**Be careful:** Root can **delete important files**  

---

### 2️⃣ Normal Users

- Limited permissions
- Can access own files and directories
- Symbol: `$` in terminal prompt

---

## 👥 What Are Groups?

A **group** is a collection of users.

- Allows sharing files and permissions
- Users can belong to multiple groups
- Each group has a **GID** (Group ID)

---

## 🔍 Viewing Users and Groups

### 1️⃣ Current User
```bash
whoami
````

### 2️⃣ Current Groups

```bash
groups
```

### 3️⃣ All Users

```bash
cat /etc/passwd
```

### 4️⃣ All Groups

```bash
cat /etc/group
```

---

## ⚙️ Basic User Management Commands

> **Safe commands for beginners**

### 1️⃣ Add User

```bash
sudo adduser username
```

### 2️⃣ Delete User

```bash
sudo deluser username
```

### 3️⃣ Add User to Group

```bash
sudo usermod -aG groupname username
```

---

## 🛡️ What Is Sudo?

* Stands for **“SuperUser Do”**
* Allows normal user to run commands as **root**
* Example:

```bash
sudo apt update
```

📌 Requires entering your password

---

## 📝 Key Exam Notes (Remember This)

* Linux is **multi-user**
* Root = superuser, `$` = normal user
* Groups allow permission sharing
* Sudo allows temporary root privileges
* `/etc/passwd` lists users, `/etc/group` lists groups

---

## ❌ Common Beginner Mistakes

❌ Using root unnecessarily
❌ Giving sudo to everyone
❌ Deleting important system users
❌ Forgetting to check groups

✅ Always verify with `whoami` and `groups`

---

## 🧪 Practice Questions (Short Answer)

1. What is the root user?
2. What is a normal user?
3. What is a group in Linux?
4. Which file lists all users?
5. What does `sudo` do?

---

## 🧠 MCQs (Exam-Friendly)

### Q1. Symbol for root user prompt:

A) $
B) %
C) #
D) &

✅ **Answer:** C

---

### Q2. Command to find current user:

A) whoami
B) groups
C) ls
D) id

✅ **Answer:** A

---

### Q3. Where are all groups listed?

A) /etc/passwd
B) /etc/group
C) /home
D) /var

✅ **Answer:** B

---

### Q4. Command to add a new user:

A) adduser
B) deluser
C) chmod
D) mkdir

✅ **Answer:** A

---

### Q5. Purpose of `sudo`:

A) Delete files
B) Run commands as root temporarily
C) Create groups
D) Change directory

✅ **Answer:** B

---

## 🚀 What’s Next?

In the next lesson, you will learn:

👉 **[10 – Package Management](10-package-management.md)**
(Installing, updating, and removing software on Linux safely)

---

Happy Learning 🐧👥

```
