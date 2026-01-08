# 07 – Basic Linux Commands

---

## 🔙 Navigation
⬅️ **Previous:** [06 – Files and Directories](06-files-and-directories.md)  
➡️ **Next:** [08 – File Permissions](08-file-permissions.md)

---

## 🎯 Objective

After completing this lesson, you will be able to:

- Understand commonly used Linux commands
- Create, copy, move, and delete files
- View file contents safely
- Use command options
- Answer exam questions on basic Linux commands

---

## 🧠 What Is a Linux Command?

A **Linux command** is an instruction given to the system to perform a task.

General syntax:
```bash
command options arguments
````

Example:

```bash
ls -l /home
```

---

## 📄 File & Directory Management Commands

### 1️⃣ `touch` – Create a File

```bash
touch file.txt
```

---

### 2️⃣ `mkdir` – Create a Directory

```bash
mkdir myfolder
```

---

### 3️⃣ `cp` – Copy Files or Directories

Copy a file:

```bash
cp file1.txt file2.txt
```

Copy a directory:

```bash
cp -r dir1 dir2
```

---

### 4️⃣ `mv` – Move or Rename Files

Rename a file:

```bash
mv old.txt new.txt
```

Move a file:

```bash
mv file.txt /home/user/
```

---

### 5️⃣ `rm` – Remove Files or Directories ⚠️

Remove a file:

```bash
rm file.txt
```

Remove a directory:

```bash
rm -r myfolder
```

📌 **Be careful** — deleted files cannot be recovered easily.

---

## 👀 Viewing File Contents

### 6️⃣ `cat` – Display File Content

```bash
cat file.txt
```

---

### 7️⃣ `less` – View Large Files Safely

```bash
less file.txt
```

* Scroll with arrow keys
* Press `q` to quit

---

### 8️⃣ `head` – View Beginning of File

```bash
head file.txt
```

---

### 9️⃣ `tail` – View End of File

```bash
tail file.txt
```

---

## 🔍 Helpful Commands

### 🔹 `file` – Show File Type

```bash
file file.txt
```

---

### 🔹 `wc` – Word Count

```bash
wc file.txt
```

---

## 📝 Key Exam Notes (Remember This)

* `cp` is used to copy files
* `mv` is used to move or rename files
* `rm` deletes files permanently
* `less` is safer than `cat` for large files
* `-r` option means recursive

---

## ❌ Common Beginner Mistakes

❌ Using `rm -r` carelessly
❌ Confusing `cp` and `mv`
❌ Viewing large files with `cat`
❌ Forgetting command options

✅ Always double-check commands

---

## 🧪 Practice Questions (Short Answer)

1. Which command is used to copy files?
2. How do you rename a file in Linux?
3. What command removes a directory?
4. Which command is safest to view large files?
5. What does `-r` option do?

---

## 🧠 MCQs (Exam-Friendly)

### Q1. Which command is used to copy files?

A) mv
B) rm
C) cp
D) ls

✅ **Answer:** C

---

### Q2. Command used to rename a file is:

A) mv
B) cp
C) rm
D) touch

✅ **Answer:** A

---

### Q3. Which command deletes files?

A) del
B) erase
C) rm
D) remove

✅ **Answer:** C

---

### Q4. Which command is best for viewing large files?

A) cat
B) less
C) touch
D) pwd

✅ **Answer:** B

---

### Q5. What does `rm -r` do?

A) Removes files only
B) Removes directories recursively
C) Renames directories
D) Reads files

✅ **Answer:** B

---

## 🚀 What’s Next?

In the next lesson, you will learn:

👉 **[08 – File Permissions](08-file-permissions.md)**
(Understanding `r`, `w`, `x`, `chmod`, and Linux security basics)

---

Happy Learning 🐧📜

```
