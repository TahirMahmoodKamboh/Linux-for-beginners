# 29 – Mini Project 09 – Archives, Compression & Backups

---

## 🔙 Navigation
⬅️ **Previous:** [28 – Mini Project 08](28-Mini-Project-08.md)  
➡️ **Next:** [30 – Mini Project 10](30-Mini-Project-10.md)

---

## 🎯 Objective

This project will help you practice **creating, compressing, and managing backups** in Linux.  
By the end of this project, you will be able to:

- Create and extract archive files (`.tar`, `.zip`)  
- Compress and decompress files (`gzip`, `bzip2`)  
- Automate backups using scripts  
- Understand different compression formats and their usage  

---

## 📂 Project Setup

1. Open your terminal  
2. Create a project directory:
```bash
mkdir ~/mini-project-09
cd ~/mini-project-09
````

---

## 🛠 Tasks

### Task 1 – Create Sample Files

1. Create a directory and some files:

```bash
mkdir my_project
cd my_project
touch file1.txt file2.txt file3.txt
```

2. Add sample content:

```bash
echo "Hello World" > file1.txt
echo "Linux is fun!" > file2.txt
echo "Backup practice" > file3.txt
```

---

### Task 2 – Create a TAR Archive

1. Go to parent directory:

```bash
cd ..
```

2. Create a tar archive of `my_project`:

```bash
tar -cvf my_project.tar my_project
```

3. Verify archive:

```bash
ls -l my_project.tar
```

---

### Task 3 – Extract a TAR Archive

1. Extract the archive to a new directory:

```bash
mkdir extracted
tar -xvf my_project.tar -C extracted
```

2. Verify extraction:

```bash
ls extracted/my_project
```

---

### Task 4 – Compress Archives

1. Compress using gzip:

```bash
gzip my_project.tar
```

2. Verify:

```bash
ls -l my_project.tar.gz
```

3. Decompress gzip file:

```bash
gunzip my_project.tar.gz
```

4. Compress using bzip2:

```bash
bzip2 my_project.tar
```

5. Decompress bzip2 file:

```bash
bunzip2 my_project.tar.bz2
```

---

### Task 5 – Create a ZIP Archive

1. Create a zip archive:

```bash
zip -r my_project.zip my_project
```

2. Verify archive:

```bash
ls -l my_project.zip
```

3. Extract ZIP archive:

```bash
unzip my_project.zip -d zip_extracted
```

4. Verify extraction:

```bash
ls zip_extracted/my_project
```

---

### Task 6 – Automate Backups with a Script

1. Create a backup script `backup_project.sh`:

```bash
nano backup_project.sh
```

2. Add the following content:

```bash
#!/bin/bash
# Backup my_project directory with timestamp
DATE=$(date +%F_%H-%M-%S)
tar -cvf ~/my_project_backup_$DATE.tar ~/mini-project-09/my_project
gzip ~/my_project_backup_$DATE.tar
echo "Backup created at $DATE"
```

3. Save, exit, and make it executable:

```bash
chmod +x backup_project.sh
```

4. Run the script:

```bash
./backup_project.sh
```

✅ Expected Outcome:

* A timestamped compressed backup is created in your home directory

---

### Task 7 – Explore Commands

* Explore archive and compression commands using `--help` or `man`:

```bash
man tar
tar --help
man gzip
gzip --help
man bzip2
bzip2 --help
man zip
zip --help
```

---

## ✅ Expected Outcomes

By the end of this project, you should be able to:

* Create and extract `.tar` and `.zip` archives
* Compress and decompress files using `gzip` and `bzip2`
* Automate backups with shell scripts
* Understand timestamped backups and best practices

---

## 📝 Notes / Tips

* `tar -cvf` creates an archive, `-xvf` extracts it
* `gzip` and `bzip2` compress files
* `zip` is widely used for cross-platform compression
* Always test backup scripts to ensure files are saved correctly

---

## 🎯 Learning Outcomes

By completing this project, you will:

* Gain practical experience with file archiving and compression
* Learn to automate backups safely
* Understand different compression formats and their benefits
* Be ready to handle Linux file backups and restoration tasks

Do you want me to do that next?
```
