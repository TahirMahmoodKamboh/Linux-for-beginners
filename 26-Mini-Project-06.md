# 26 – Mini Project 06 – Package Management & System Updates

---

## 🔙 Navigation
⬅️ **Previous:** [25 – Mini Project 05](25-Mini-Project-05.md)  
➡️ **Next:** [27 – Mini Project 07](27-Mini-Project-07.md)

---

## 🎯 Objective

This project will help you practice **package management and system updates** in Linux.  
By the end of this project, you will be able to:

- Update the system safely  
- Install, remove, and upgrade packages  
- Search for packages and check installed versions  
- Understand differences between package managers on various distributions  

---

## 📂 Project Setup

1. Open your terminal  
2. Create a project directory:
```bash
mkdir ~/mini-project-06
cd ~/mini-project-06
````

---

## 🛠 Tasks

### Task 1 – Update System Packages

1. Update package list (Debian/Ubuntu):

```bash
sudo apt update
```

2. Upgrade all packages:

```bash
sudo apt upgrade -y
```

3. For Red Hat/CentOS/Fedora systems:

```bash
sudo yum check-update
sudo yum update -y
```

✅ Expected Outcome:

* System package lists are updated, and all packages are upgraded

---

### Task 2 – Search for Packages

1. Search for a package (example: `vim`):

```bash
apt search vim       # Debian/Ubuntu
yum search vim       # RHEL/CentOS/Fedora
```

2. Check if a package is installed:

```bash
dpkg -l | grep vim   # Debian/Ubuntu
rpm -qa | grep vim   # RHEL/CentOS/Fedora
```

---

### Task 3 – Install Packages

1. Install a package (example: `curl`):

```bash
sudo apt install curl -y   # Debian/Ubuntu
sudo yum install curl -y   # RHEL/CentOS/Fedora
```

2. Verify installation:

```bash
curl --version
```

---

### Task 4 – Remove Packages

1. Remove a package (example: `curl`):

```bash
sudo apt remove curl -y    # Debian/Ubuntu
sudo yum remove curl -y    # RHEL/CentOS/Fedora
```

2. Clean unused packages (optional):

```bash
sudo apt autoremove -y     # Debian/Ubuntu
sudo yum autoremove -y     # RHEL/CentOS/Fedora
```

---

### Task 5 – Upgrade Specific Packages

1. Upgrade a single package (example: `vim`):

```bash
sudo apt install --only-upgrade vim -y   # Debian/Ubuntu
sudo yum update vim -y                    # RHEL/CentOS/Fedora
```

2. Verify upgraded version:

```bash
vim --version
```

---

### Task 6 – Explore Package Manager Commands

* Explore package manager options using `--help` or `man`:

```bash
apt --help
man apt
yum --help
man yum
dpkg --help
rpm --help
```

---

## ✅ Expected Outcomes

By the end of this project, you should be able to:

* Update system package lists and upgrade packages safely
* Search for, install, and remove software
* Upgrade specific packages individually
* Understand the difference between Debian-based and RHEL-based package managers
* Explore and use package manager commands confidently

---

## 📝 Notes / Tips

* Always run `update` before installing or upgrading packages
* Use `autoremove` to clean unnecessary packages and save disk space
* Check package versions before and after upgrades
* Package manager commands differ between Debian/Ubuntu (`apt`, `dpkg`) and Red Hat/CentOS/Fedora (`yum`, `rpm`)

---

## 🎯 Learning Outcomes

By completing this project, you will:

* Gain practical experience managing Linux software
* Understand how to keep your system up-to-date and secure
* Be able to install and remove packages safely
* Build a foundation for advanced Linux administration tasks
