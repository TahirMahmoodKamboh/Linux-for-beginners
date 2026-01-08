# 28 – Mini Project 08 – Users, Groups & Permissions

---

## 🔙 Navigation
⬅️ **Previous:** [27 – Mini Project 07](27-Mini-Project-07.md)  
➡️ **Next:** [29 – Mini Project 09](29-Mini-Project-09.md)

---

## 🎯 Objective

This project will help you practice **user and group management, and file permissions** in Linux.  
By the end of this project, you will be able to:

- Create and manage users and groups  
- Assign users to groups  
- Set and modify file and directory permissions  
- Use `chmod`, `chown`, and `chgrp` safely  

---

## 📂 Project Setup

1. Open your terminal  
2. Create a project directory:
```bash
mkdir ~/mini-project-08
cd ~/mini-project-08
````

> ⚠️ You will need `sudo` privileges for some tasks

---

## 🛠 Tasks

### Task 1 – Create Users

1. Create a new user `user1`:

```bash
sudo adduser user1
```

2. Create another user `user2`:

```bash
sudo adduser user2
```

3. Verify users:

```bash
cat /etc/passwd | grep user
```

---

### Task 2 – Create Groups

1. Create a new group `developers`:

```bash
sudo groupadd developers
```

2. Add `user1` and `user2` to the group:

```bash
sudo usermod -aG developers user1
sudo usermod -aG developers user2
```

3. Verify group membership:

```bash
groups user1
groups user2
```

---

### Task 3 – Create Files and Set Ownership

1. Create a test directory and files:

```bash
mkdir project_files
cd project_files
touch file1.txt file2.txt
```

2. Change ownership to `user1` and group to `developers`:

```bash
sudo chown user1:developers file1.txt
sudo chown user2:developers file2.txt
```

3. Verify ownership:

```bash
ls -l
```

---

### Task 4 – Set Permissions

1. Set read/write for owner, read-only for group, no permissions for others:

```bash
chmod 640 file1.txt
chmod 640 file2.txt
```

2. Verify permissions:

```bash
ls -l
```

3. Set execute permission for scripts:

```bash
chmod +x some_script.sh
```

---

### Task 5 – Change Permissions Recursively

1. Create subdirectories:

```bash
mkdir -p project_files/subdir
touch project_files/subdir/file3.txt
```

2. Set permissions recursively for owner read/write, group read, others none:

```bash
chmod -R 640 project_files
```

3. Verify:

```bash
ls -lR project_files
```

---

### Task 6 – Explore Commands

* Explore the following commands using `--help` or `man`:

```bash
man adduser
man usermod
man groupadd
man chown
man chgrp
man chmod
```

---

## ✅ Expected Outcomes

By the end of this project, you should be able to:

* Create and manage users and groups
* Assign users to groups correctly
* Set and modify file and directory permissions
* Verify ownership and permissions
* Apply permissions recursively when needed

---

## 📝 Notes / Tips

* Always use `sudo` for administrative tasks
* Use `ls -l` to verify file ownership and permissions
* `chmod 640` means: owner can read/write, group can read, others have no access
* Be careful with `chown` and `chmod` on system files

---

## 🎯 Learning Outcomes

By completing this project, you will:

* Gain practical experience managing users and groups
* Understand Linux file and directory permissions
* Learn to secure files by setting proper permissions
* Build a foundation for Linux system administration and security
