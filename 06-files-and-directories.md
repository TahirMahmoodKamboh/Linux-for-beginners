# 06 – Files and Directories

---

## 🔙 Navigation
⬅️ **Previous:** [05 – Terminal Basics](05-terminal-basics.md)  
➡️ **Next:** [07 – Basic Linux Commands](07-basic-linux-commands.md)

---

## 🎯 Objective

After completing this lesson, you will be able to:

- Understand what files and directories are in Linux
- Navigate the Linux file system using terminal
- Understand paths in Linux
- Use basic navigation commands
- Answer exam questions related to Linux files and directories

---

## 🧠 What Is a File in Linux?

A **file** is used to store data.

Examples of files:
- Text files (`.txt`)
- Scripts (`.sh`)
- Images (`.png`)
- Configuration files

📌 In Linux, **everything is treated as a file**.

---

## 📁 What Is a Directory?

A **directory** is a container that holds:
- Files
- Other directories

📌 Directory = Folder (Windows term)

---

## 🌳 Linux Directory Structure (Basic Idea)

Linux has a **tree-like structure**.

- `/` → Root directory (top level)
- `/home` → User home directories
- `/etc` → Configuration files
- `/var` → Logs and variable data

📌 You will study this in detail later.

---

## 📍 Understanding Paths (Very Important)

A **path** shows the location of a file or directory.

### Absolute Path
- Starts from root `/`
- Example:
```bash
/home/user/Documents
````

### Relative Path

* Starts from current location
* Example:

```bash
Documents
```

---

## 🏠 Home Directory

Each user has a **home directory**.

* Path: `/home/username`
* Shortcut: `~`

Example:

```bash
cd ~
```

---

## 🧭 Navigation Commands

### 1️⃣ `pwd` – Show Current Location

```bash
pwd
```

---

### 2️⃣ `ls` – List Files & Directories

```bash
ls
ls -l
ls -a
```

---

### 3️⃣ `cd` – Change Directory

```bash
cd Documents
cd /home/user
cd ..
cd ~
```

---

## 🔄 Special Directory Symbols

| Symbol | Meaning           |
| ------ | ----------------- |
| `.`    | Current directory |
| `..`   | Parent directory  |
| `~`    | Home directory    |
| `/`    | Root directory    |

---

## 📂 Creating Directories

### `mkdir` – Make Directory

```bash
mkdir test
mkdir my_folder
```

---

## 📄 Creating Files

### `touch` – Create Empty File

```bash
touch file1.txt
```

---

## 📝 Key Exam Notes (Remember This)

* `/` is the root directory
* Linux uses **forward slash `/`**
* `~` represents home directory
* Absolute path starts with `/`
* Relative path does not start with `/`

---

## ❌ Common Beginner Mistakes

❌ Confusing `/` with `\`
❌ Forgetting current directory
❌ Using wrong case in names
❌ Running commands in wrong location

✅ Always check with `pwd`

---

## 🧪 Practice Questions (Short Answer)

1. What is a file?
2. What is a directory?
3. What does `/` represent?
4. Difference between absolute and relative path?
5. What does `~` mean?

---

## 🧠 MCQs (Exam-Friendly)

### Q1. Root directory in Linux is:

A) home
B) root
C) /
D) ~

✅ **Answer:** C

---

### Q2. Which command changes directory?

A) ls
B) pwd
C) cd
D) mkdir

✅ **Answer:** C

---

### Q3. Home directory shortcut is:

A) /
B) ..
C) .
D) ~

✅ **Answer:** D

---

### Q4. Which path is absolute?

A) Documents/file.txt
B) ./file.txt
C) ../file.txt
D) /home/user/file.txt

✅ **Answer:** D

---

### Q5. Command to create a directory is:

A) touch
B) mkdir
C) cd
D) rm

✅ **Answer:** B

---

## 🚀 What’s Next?

In the next lesson, you will learn:

👉 **[07 – Basic Linux Commands](07-basic-linux-commands.md)**
(File management commands like `cp`, `mv`, `rm`, `cat`)

---

Happy Learning 🐧📂

```
