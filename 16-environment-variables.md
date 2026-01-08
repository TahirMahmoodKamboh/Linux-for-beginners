# 16 – Environment Variables

---

## 🔙 Navigation
⬅️ **Previous:** [15 – Basic Shell Scripting](15-basic-shell-scripting.md)  
➡️ **Next:** [17 – Logs and Monitoring](17-logs-and-monitoring.md)

---

## 🎯 Objective

After completing this lesson, you will be able to:

- Understand what environment variables are  
- Learn common environment variables in Linux  
- View, create, modify, and delete environment variables  
- Answer exam questions on environment variables  

---

## 🧠 What Are Environment Variables?

Environment variables are **dynamic values** that affect the behavior of the shell and programs.

- Accessible to the shell and child processes  
- Store information like paths, usernames, editors, terminal types  

---

## 📌 Common Environment Variables

| Variable | Description |
|----------|-------------|
| `PATH` | Colon-separated list of directories where the shell looks for executable commands and programs |
| `HOME` | Absolute path to the current user’s home directory |
| `USER` | Username of the currently logged-in user |
| `SHELL` | Path to the current user’s shell program (e.g., `/bin/bash`) |
| `PWD` | Current working directory (Present Working Directory) |
| `EDITOR` | Default text editor used by programs like git or visudo |
| `LANG` / `LC_*` | Language and locale settings, including character encoding and time formats |
| `MAIL` | Location of the user’s mail spool (typically `/var/spool/mail/USER`) |
| `HOSTNAME` | Name of the computer system |
| `TERM` | Type of terminal being emulated |
| `PS1` | Format and contents of the primary shell prompt |
| `HISTSIZE` / `HISTFILESIZE` | Number of command history lines stored in memory and in the history file |

---

## 🔍 Viewing Environment Variables

### 1️⃣ `printenv` – Display Variables
```bash
printenv
````

* Shows all environment variables

```bash
printenv PATH
```

* Shows value of a specific variable

### 2️⃣ `echo` – Display Specific Variable

```bash
echo $HOME
echo $USER
```

### 3️⃣ `env` – List All Variables

```bash
env
```

---

## ⚙ Managing Environment Variables

### 1️⃣ `export` – Make Variable Available to Child Processes

```bash
MY_VAR="Hello"
export MY_VAR
echo $MY_VAR
```

### 2️⃣ `unset` – Remove a Variable

```bash
unset MY_VAR
echo $MY_VAR   # Will show nothing
```

---

## 📝 Key Exam Notes (Remember This)

* Environment variables store info about shell, user, and system
* `$PATH` is crucial for running commands without full paths
* `$HOME` is your home directory
* `$USER` shows your username
* Use `printenv`, `env`, or `echo $VARIABLE` to check values
* Use `export` to make variables available to child processes
* `unset` deletes variables

---

## ❌ Common Beginner Mistakes

❌ Forgetting the `$` when referencing variables
❌ Changing `$PATH` carelessly (can break command execution)
❌ Using `export` unnecessarily for temporary variables
❌ Unsetting important system variables

✅ Always double-check variable values before modifying

---

## 🧪 Practice Questions (Short Answer)

1. What is an environment variable?
2. Command to display all environment variables?
3. How do you view the current user using a variable?
4. Command to create an environment variable for child processes?
5. How do you remove an environment variable?

---

## 🧠 MCQs (Exam-Friendly)

### Q1. What does `$PATH` store?

A) Current directory
B) List of directories to search for commands
C) User’s home directory
D) Default text editor

✅ **Answer:** B

---

### Q2. Command to list all environment variables:

A) echo $VARIABLE
B) printenv
C) export
D) unset

✅ **Answer:** B

---

### Q3. How to display the current user's username?

A) echo $USER
B) echo $HOME
C) printenv PATH
D) env PWD

✅ **Answer:** A

---

### Q4. Command to make a variable available to child processes:

A) unset
B) export
C) echo
D) env

✅ **Answer:** B

---

### Q5. Command to remove a variable from current session:

A) delete
B) unset
C) remove
D) export

✅ **Answer:** B

---

## 🚀 What’s Next?

In the next lesson, you will learn:

👉 **[17 – Logs and Monitoring](17-logs-and-monitoring.md)**
(Learn to view system logs, monitor services, and troubleshoot Linux)

---

Happy Learning 🐧📂

```
