# 08 – File Permissions

---

## 🔙 Navigation
⬅️ **Previous:** [07 – Basic Linux Commands](07-basic-linux-commands.md)  
➡️ **Next:** [09 – Users and Groups](09-users-and-groups.md)

---

## 🎯 Objective

After completing this lesson, you will be able to:

- Understand what file permissions are in Linux
- Read and interpret permission symbols
- Use `chmod` and `chown` safely
- Understand why permissions are important
- Answer exam questions on file permissions

---

## 🧠 What Are File Permissions?

File permissions determine **who can do what** with a file or directory.

Linux uses **three types of permissions**:

1️⃣ **Read (r)** – view file contents  
2️⃣ **Write (w)** – modify or delete file  
3️⃣ **Execute (x)** – run file as a program

---

## 👥 Who Gets Permissions?

Permissions are assigned to **three categories of users**:

1️⃣ **Owner (u)** – The user who owns the file  
2️⃣ **Group (g)** – Users in the same group  
3️⃣ **Others (o)** – Everyone else

---

## 🔍 Viewing Permissions

Use the command:

```bash
ls -l
````

Example output:

```bash
-rw-r--r-- 1 user user 1024 Jan 8 12:00 file.txt
```

**Interpretation:**

| Part        | Meaning                       |
| ----------- | ----------------------------- |
| `-`         | File type (`d` for directory) |
| `rw-`       | Owner can read & write        |
| `r--`       | Group can read                |
| `r--`       | Others can read               |
| `user user` | Owner and group               |

---

## ⚙️ Changing Permissions

### `chmod` – Change Mode

#### Symbolic Method

```bash
chmod u+x file.sh   # Add execute permission for owner
chmod g-w file.txt  # Remove write permission from group
chmod o+r file.txt  # Add read permission for others
```

#### Numeric Method

Permissions can also be **numeric**:

| Number | Permission |
| ------ | ---------- |
| 4      | read       |
| 2      | write      |
| 1      | execute    |

Add numbers together:

* `7 = 4+2+1 = rwx`
* `6 = 4+2 = rw-`
* `5 = 4+1 = r-x`

Example:

```bash
chmod 755 file.sh
```

* Owner: rwx
* Group: r-x
* Others: r-x

---

### `chown` – Change Owner

```bash
sudo chown newuser file.txt
```

* Changes file owner
* Group can also be changed:

```bash
sudo chown newuser:newgroup file.txt
```

---

## 📝 Key Exam Notes (Remember This)

* Linux uses `r`, `w`, `x` permissions
* Permissions apply to **owner, group, others**
* `chmod` changes permissions
* `chown` changes ownership
* `ls -l` shows permissions

---

## ❌ Common Beginner Mistakes

❌ Using `chmod 777` on important files
❌ Forgetting to use `sudo` when required
❌ Confusing symbolic and numeric modes
❌ Ignoring group permissions

✅ Always check with `ls -l` before changing

---

## 🧪 Practice Questions (Short Answer)

1. What does `r` mean in Linux permissions?
2. Who is considered "owner" of a file?
3. What command shows file permissions?
4. How do you add execute permission to a file?
5. What does `chmod 644 file.txt` do?

---

## 🧠 MCQs (Exam-Friendly)

### Q1. Which permission allows a file to be run as a program?

A) r
B) w
C) x
D) rw

✅ **Answer:** C

---

### Q2. `ls -l` shows:

A) File type, size, permissions, owner
B) Only file name
C) Only size
D) Only owner

✅ **Answer:** A

---

### Q3. Numeric permission `7` equals:

A) r--
B) rwx
C) r-x
D) --x

✅ **Answer:** B

---

### Q4. Command to change file owner:

A) chmod
B) chown
C) ls
D) mv

✅ **Answer:** B

---

### Q5. Default permissions for a new file usually:

A) rwx for all
B) r-- for owner only
C) rw- for owner, r-- for group/others
D) No permissions

✅ **Answer:** C

---

## 🚀 What’s Next?

In the next lesson, you will learn:

👉 **[09 – Users and Groups](09-users-and-groups.md)**
(Understanding root, normal users, sudo, and Linux groups)

---

Happy Learning 🐧🔒

```
