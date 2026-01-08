# 10 – Package Management

---

## 🔙 Navigation
⬅️ **Previous:** [09 – Users and Groups](09-users-and-groups.md)  
➡️ **Next:** [11 – Processes and System Info](11-processes-and-system-info.md)

---

## 🎯 Objective

After completing this lesson, you will be able to:

- Understand what a package manager is
- Install, update, and remove software safely
- Learn basic commands for Ubuntu/Debian and Fedora
- Answer exam questions related to package management

---

## 🧠 What Is a Package Manager?

A **package manager** is software that:

- Installs, updates, and removes programs
- Handles dependencies automatically
- Keeps your system organized

Examples:

- `apt` → Ubuntu/Debian  
- `dnf` → Fedora  
- `yum` → CentOS/RHEL  
- `pacman` → Arch Linux

---

## 🟢 Ubuntu / Debian: `apt`

### 1️⃣ Update Package Index
```bash
sudo apt update
````

* Downloads latest package information

### 2️⃣ Upgrade Installed Packages

```bash
sudo apt upgrade
```

* Upgrades outdated packages

### 3️⃣ Install a Package

```bash
sudo apt install package_name
```

Example:

```bash
sudo apt install vim
```

### 4️⃣ Remove a Package

```bash
sudo apt remove package_name
```

### 5️⃣ Search for a Package

```bash
apt search package_name
```

---

## 🔵 Fedora / CentOS: `dnf` / `yum`

### 1️⃣ Install Package

```bash
sudo dnf install package_name   # Fedora
sudo yum install package_name   # CentOS
```

### 2️⃣ Remove Package

```bash
sudo dnf remove package_name
```

### 3️⃣ Update System

```bash
sudo dnf update
```

---

## 📦 Key Points About Package Management

* Always run `update` before installing packages
* `install` adds software
* `remove` deletes software
* Use `search` to find packages
* Use **sudo** when modifying system software

---

## 📝 Key Exam Notes (Remember This)

* Ubuntu/Debian uses **apt**
* Fedora uses **dnf**
* CentOS uses **yum**
* Update first, then install
* Package managers handle dependencies

---

## ❌ Common Beginner Mistakes

❌ Forgetting `sudo`
❌ Using wrong package manager
❌ Not updating package index before install
❌ Installing unnecessary packages

✅ Always update, then install, and remove safely

---

## 🧪 Practice Questions (Short Answer)

1. What is a package manager?
2. Which command updates packages in Ubuntu?
3. How do you install Vim using apt?
4. Which command removes a package?
5. Name Fedora’s package manager.

---

## 🧠 MCQs (Exam-Friendly)

### Q1. Ubuntu uses which package manager?

A) yum
B) apt
C) pacman
D) dnf

✅ **Answer:** B

---

### Q2. Command to update package index in Ubuntu:

A) sudo apt install
B) sudo apt update
C) sudo apt upgrade
D) sudo apt remove

✅ **Answer:** B

---

### Q3. Fedora uses which package manager?

A) apt
B) yum
C) dnf
D) pacman

✅ **Answer:** C

---

### Q4. Command to remove a package safely:

A) rm package
B) sudo apt remove package_name
C) sudo rm package_name
D) sudo apt delete package_name

✅ **Answer:** B

---

### Q5. Why do we update package index first?

A) To remove old files
B) To see latest package versions
C) To uninstall software
D) To clear memory

✅ **Answer:** B

---

## 🚀 What’s Next?

In the next lesson, you will learn:

👉 **[11 – Processes and System Info](11-processes-and-system-info.md)**
(Understanding running programs, CPU usage, and memory)

---

Happy Learning 🐧📦

```
