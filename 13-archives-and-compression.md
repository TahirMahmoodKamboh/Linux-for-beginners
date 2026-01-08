# 13 – Archives and Compression

---

## 🔙 Navigation
⬅️ **Previous:** [12 – Networking Basics](12-networking-basics.md)  
➡️ **Next:** [14 – Editors: Nano & Vim](14-editors-nano-vim.md)

---

## 🎯 Objective

After completing this lesson, you will be able to:

- Understand archives and compression in Linux  
- Create and extract `.tar`, `.gz`, `.zip` files  
- Use safe commands to compress and decompress  
- Answer exam questions on archives and compression  

---

## 🧠 What Are Archives and Compression?

- **Archive:** Combines multiple files into one file (no compression)  
- **Compression:** Reduces file size  
- Often combined: Archive + Compress → `.tar.gz`  

---

## 📦 Common Archive Formats

| Format       | Description                  | Command Example          |
|--------------|-----------------------------|-------------------------|
| `.tar`       | Archive (no compression)     | `tar -cf archive.tar file1 file2` |
| `.tar.gz`    | Archive + gzip compression   | `tar -czf archive.tar.gz folder/` |
| `.zip`       | Zip archive                  | `zip archive.zip file1 file2` |
| `.gz`        | Single file compression      | `gzip file.txt` |

---

## 🏗 Creating Archives

### 1️⃣ `tar` – Archive Files or Folders

**Create a `.tar` archive:**
```bash
tar -cf archive.tar file1.txt file2.txt
````

**Create a `.tar.gz` archive (compressed):**

```bash
tar -czf archive.tar.gz folder/
```

**Options explained:**

* `c` → create archive
* `f` → filename
* `z` → gzip compression

---

### 2️⃣ `zip` – Zip Files

```bash
zip archive.zip file1.txt file2.txt
```

Add a folder recursively:

```bash
zip -r archive.zip folder/
```

---

## 🏗 Extracting Archives

### 1️⃣ Extract `.tar` files

```bash
tar -xf archive.tar
```

### 2️⃣ Extract `.tar.gz` files

```bash
tar -xzf archive.tar.gz
```

### 3️⃣ Extract `.zip` files

```bash
unzip archive.zip
```

---

## 🔄 Checking Archive Contents Without Extracting

### `tar -tf archive.tar`

* Lists files in `.tar` archive

### `zipinfo archive.zip`

* Lists files in `.zip` archive

---

## 📝 Key Exam Notes (Remember This)

* `.tar` → archive only
* `.tar.gz` → archive + gzip
* `.zip` → archive format, widely used
* `tar -cf` → create, `tar -xf` → extract
* `gzip` compresses single files

---

## ❌ Common Beginner Mistakes

❌ Forgetting `-f` option with tar
❌ Confusing compress vs archive
❌ Overwriting files accidentally
❌ Not using `-r` to include folders in zip

✅ Always check files with `ls` or `tar -tf` first

---

## 🧪 Practice Questions (Short Answer)

1. Difference between archive and compression?
2. Command to create a `.tar` archive?
3. Command to extract `.tar.gz` file?
4. How do you zip a folder recursively?
5. Which command lists archive contents without extracting?

---

## 🧠 MCQs (Exam-Friendly)

### Q1. Which command creates a compressed `.tar.gz` archive?

A) tar -xf archive.tar.gz
B) tar -czf archive.tar.gz folder/
C) zip archive.zip file1.txt
D) gzip file.txt

✅ **Answer:** B

---

### Q2. Command to extract a `.tar` file:

A) tar -cf archive.tar
B) tar -xf archive.tar
C) unzip archive.tar
D) gzip -d archive.tar

✅ **Answer:** B

---

### Q3. To zip a folder including subfolders, which option is needed?

A) -f
B) -r
C) -x
D) -z

✅ **Answer:** B

---

### Q4. `.gz` files are:

A) Archive only
B) Compressed single file
C) Executable file
D) Network file

✅ **Answer:** B

---

### Q5. Command to list contents of `.tar` without extracting:

A) tar -xf
B) tar -tf
C) unzip
D) ls

✅ **Answer:** B

---

## 🚀 What’s Next?

In the next lesson, you will learn:

👉 **[14 – Editors: Nano & Vim](14-editors-nano-vim.md)**
(Editing files safely and efficiently in Linux)

---

Happy Learning 🐧📦

```
