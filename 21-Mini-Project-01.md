# Project 01 – Basic Linux File and Directory Management

---

## 🔙 Navigation
⬅️ **Previous:** [20 – Practice Exercises](20-practice-exercises.md)  
➡️ **Next:** [22 – Mini Project 02](22-Mini-Project-02.md)

---

## 🎯 Objective

This project will help you practice **basic file and directory commands** in Linux.  
By the end of this project, you will be able to:

- Create directories and files  
- Navigate directories  
- Copy, move, and delete files  
- Understand file permissions  
- Use basic commands safely  

---

## 📂 Project Setup

1. Open your terminal  
2. Create a project directory:
```bash
mkdir ~/mini-project-01
cd ~/mini-project-01
````

---

## 🛠 Tasks

### Task 1 – Create Directories

* Create the following directory structure:

```bash
mkdir -p Documents Scripts Logs
```

* Verify with:

```bash
ls -l
```

---

### Task 2 – Create Files

* Inside `Documents`, create three text files:

```bash
cd Documents
touch file1.txt file2.txt file3.txt
ls
```

---

### Task 3 – Write Content to Files

* Use `echo` or `nano` to add content:

```bash
echo "This is file 1" > file1.txt
echo "This is file 2" > file2.txt
echo "This is file 3" > file3.txt
```

* Verify content with:

```bash
cat file1.txt
cat file2.txt
cat file3.txt
```

---

### Task 4 – Copy and Move Files

* Copy `file1.txt` to `Scripts` directory:

```bash
cp file1.txt ../Scripts/
```

* Move `file2.txt` to `Scripts` directory:

```bash
mv file2.txt ../Scripts/
```

* Verify both directories:

```bash
ls ../Scripts
ls
```

---

### Task 5 – Delete Files and Directories

* Delete `file3.txt`:

```bash
rm file3.txt
```

* Delete an empty directory (optional):

```bash
rmdir Logs
```

* Verify deletion:

```bash
ls
ls ../Scripts
```

---

### Task 6 – Check Permissions

* View permissions:

```bash
ls -l
```

* Change permissions to make `file1.txt` executable:

```bash
chmod +x ../Scripts/file1.txt
ls -l ../Scripts/
```

---

### Task 7 – Explore Commands

* Explore these commands with `--help` or `man`:

```bash
ls --help
cp --help
mv --help
rm --help
chmod --help
```

---

## ✅ Expected Outcomes

* Directories `Documents` and `Scripts` exist
* Files `file1.txt` and `file2.txt` moved/copied correctly
* `file3.txt` deleted
* Permissions updated for `file1.txt`
* You can navigate, copy, move, and remove files safely

---

## 📝 Notes / Tips

* Use `pwd` to check your current directory
* Use `ls -l` to view file permissions and ownership
* Always double-check paths before deleting files
* Experiment safely; you can always remove the `mini-project-01` directory if needed

---

## 🎯 Learning Outcomes

By completing this project, you will have **practical experience** with:

* Linux file and directory structure
* Basic file management commands (`mkdir`, `touch`, `cp`, `mv`, `rm`)
* Navigating directories (`cd`, `pwd`, `ls`)
* File permissions and modification (`chmod`)

