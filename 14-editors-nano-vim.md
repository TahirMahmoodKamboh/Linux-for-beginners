# 14 – Editors: Nano & Vim

---

## 🔙 Navigation
⬅️ **Previous:** [13 – Archives and Compression](13-archives-and-compression.md)  
➡️ **Next:** [15 – Basic Shell Scripting](15-basic-shell-scripting.md)

---

## 🎯 Objective

After completing this lesson, you will be able to:

- Understand what text editors are in Linux  
- Use Nano to create and edit files  
- Use Vim for basic file editing  
- Save and exit files safely  
- Answer exam questions on Linux editors  

---

## 🧠 What Are Text Editors?

A **text editor** allows you to create or modify plain text files.  

Common Linux editors:  
- **Nano** → Beginner-friendly, simple  
- **Vim** → Powerful, requires learning commands  

---

## 🖊 Nano Editor (Beginner-Friendly)

### Open a file in Nano
```bash
nano file.txt
````

* Opens `file.txt` for editing
* If file does not exist, it creates a new one

### Basic Nano Commands

| Command    | Action                |
| ---------- | --------------------- |
| `Ctrl + O` | Save file (write out) |
| `Ctrl + X` | Exit editor           |
| `Ctrl + K` | Cut current line      |
| `Ctrl + U` | Paste cut line        |
| `Ctrl + W` | Search text           |

---

### Example

1. Open file: `nano notes.txt`
2. Type text: `Hello Linux World!`
3. Save: `Ctrl + O` → Enter
4. Exit: `Ctrl + X`

✅ Simple, easy for beginners

---

## 🖊 Vim Editor (Advanced Beginner)

### Open a file in Vim

```bash
vim file.txt
```

### Modes in Vim

1️⃣ **Normal Mode** → For navigation and commands
2️⃣ **Insert Mode** → For typing text
3️⃣ **Command Mode** → For saving, quitting, etc. (`:` commands)

### Basic Vim Commands

| Command | Action                |
| ------- | --------------------- |
| `i`     | Switch to insert mode |
| `Esc`   | Return to normal mode |
| `:w`    | Save file             |
| `:q`    | Quit Vim              |
| `:wq`   | Save and quit         |
| `:q!`   | Quit without saving   |
| `dd`    | Delete current line   |
| `yy`    | Copy current line     |
| `p`     | Paste copied line     |

---

### Example

1. Open file: `vim notes.txt`
2. Press `i` → type: `Hello Linux!`
3. Press `Esc` → type `:wq` → Enter → Save & exit

✅ Vim is more powerful but needs practice

---

## 📝 Key Exam Notes (Remember This)

* Nano is beginner-friendly
* `Ctrl + O` → Save in Nano, `Ctrl + X` → Exit
* Vim has multiple modes: Normal, Insert, Command
* `:w` → Save, `:q` → Quit, `:wq` → Save & Quit
* Text editors are used to create scripts, configs, and notes

---

## ❌ Common Beginner Mistakes

❌ Forgetting to save before exiting
❌ Trying to type in Normal mode in Vim
❌ Closing Vim with `Ctrl + C` instead of `:q`
❌ Not using search features (`Ctrl + W` in Nano)

✅ Always check commands on screen prompts

---

## 🧪 Practice Questions (Short Answer)

1. How do you open a file in Nano?
2. Which key saves a file in Nano?
3. How do you exit Nano?
4. In Vim, which mode is used for typing text?
5. Command to save and quit in Vim?

---

## 🧠 MCQs (Exam-Friendly)

### Q1. Which editor is beginner-friendly in Linux?

A) Vim
B) Nano
C) Emacs
D) Vi

✅ **Answer:** B

---

### Q2. Key combination to save a file in Nano:

A) Ctrl + X
B) Ctrl + S
C) Ctrl + O
D) Ctrl + P

✅ **Answer:** C

---

### Q3. In Vim, which command quits without saving?

A) :w
B) :q
C) :q!
D) :wq

✅ **Answer:** C

---

### Q4. To start typing in Vim, which key is used?

A) Esc
B) i
C) :
D) x

✅ **Answer:** B

---

### Q5. Command to save and quit in Vim:

A) :w
B) :q
C) :wq
D) :x

✅ **Answer:** C

---

## 🚀 What’s Next?

In the next lesson, you will learn:

👉 **[15 – Basic Shell Scripting](15-basic-shell-scripting.md)**
(Learn to automate tasks and write simple scripts in Linux)

---

Happy Learning 🐧✍️

```
