# 15 – Basic Shell Scripting

---

## 🔙 Navigation
⬅️ **Previous:** [14 – Editors: Nano & Vim](14-editors-nano-vim.md)  
➡️ **Next:** [16 – Environment Variables](16-environment-variables.md)

---

## 🎯 Objective

After completing this lesson, you will be able to:

- Understand what a shell script is  
- Create and run simple shell scripts  
- Use variables and basic commands in scripts  
- Understand `if-else` and loops (simple examples)  
- Answer exam questions on basic shell scripting  

---

## 🧠 What Is a Shell Script?

A **shell script** is a file containing a series of commands that the shell executes sequentially.

- Usually saved with `.sh` extension  
- Automates tasks in Linux  
- Makes repetitive tasks easier  

---

## 🏗 Creating Your First Script

### 1️⃣ Create a file
```bash
nano hello.sh
````

### 2️⃣ Add the shebang (interpreter)

```bash
#!/bin/bash
```

### 3️⃣ Add a simple command

```bash
#!/bin/bash
echo "Hello Linux World!"
```

### 4️⃣ Save and exit (`Ctrl + O`, `Ctrl + X` in Nano)

### 5️⃣ Make the script executable

```bash
chmod +x hello.sh
```

### 6️⃣ Run the script

```bash
./hello.sh
```

✅ Output: `Hello Linux World!`

---

## 📝 Using Variables

```bash
#!/bin/bash
name="Rocky"
echo "Hello $name!"
```

* `$name` → accesses the variable
* Variables **do not have spaces** around `=`

---

## 🔄 Basic Conditional (`if-else`)

```bash
#!/bin/bash
number=10

if [ $number -gt 5 ]; then
    echo "Number is greater than 5"
else
    echo "Number is 5 or less"
fi
```

* `[ $number -gt 5 ]` → test condition
* `-gt` → greater than
* `-lt` → less than
* `-eq` → equal

---

## 🔁 Simple Loop

### `for` loop

```bash
#!/bin/bash
for i in 1 2 3
do
    echo "Number $i"
done
```

### `while` loop

```bash
#!/bin/bash
count=1
while [ $count -le 3 ]
do
    echo "Count $count"
    count=$((count + 1))
done
```

---

## 📝 Key Exam Notes (Remember This)

* Shebang: `#!/bin/bash` → tells shell which interpreter to use
* Make script executable: `chmod +x script.sh`
* Run script: `./script.sh`
* Variables: `$variable_name`
* Conditional: `if [ condition ]; then ... fi`
* Loops: `for` and `while`

---

## ❌ Common Beginner Mistakes

❌ Forgetting `#!/bin/bash`
❌ Not making the script executable
❌ Using spaces incorrectly in variable assignment
❌ Forgetting `fi` to close `if` statement
❌ Using `=` in `[ ]` instead of `-eq` for numbers

✅ Always test scripts with `echo` statements first

---

## 🧪 Practice Questions (Short Answer)

1. What is a shell script?
2. How do you make a script executable?
3. What does `#!/bin/bash` do?
4. How do you access a variable in a script?
5. Write a simple `for` loop to print numbers 1 to 3

---

## 🧠 MCQs (Exam-Friendly)

### Q1. What is the purpose of `chmod +x script.sh`?

A) Delete the script
B) Make the script executable
C) Run the script
D) Edit the script

✅ **Answer:** B

---

### Q2. How do you run a shell script in current directory?

A) bash script.sh
B) ./script.sh
C) /script.sh
D) Both A and B

✅ **Answer:** D

---

### Q3. What is the shebang line in a shell script?

A) #!/bin/bash
B) #!/usr/bin/python
C) echo "Hello"
D) ./script.sh

✅ **Answer:** A

---

### Q4. Which is correct variable assignment in Bash?

A) name = "Rocky"
B) name=Rocky
C) name= "Rocky"
D) name =Rocky

✅ **Answer:** B

---

### Q5. What does `-gt` mean in `[ $number -gt 5 ]`?

A) Greater than
B) Less than
C) Equal
D) Not equal

✅ **Answer:** A

---

## 🚀 What’s Next?

In the next lesson, you will learn:

👉 **[16 – Environment Variables](16-environment-variables.md)**
(Understanding PATH, HOME, USER, and temporary variables)

---

Happy Learning 🐧💻

```
