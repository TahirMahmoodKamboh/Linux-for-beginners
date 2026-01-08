# 21 – Mini Project 02 – Basic Shell Scripting & Environment Variables

---

## 🔙 Navigation
⬅️ **Previous:** [21 – Mini Project 01](21-Mini-Project-01.md)  
➡️ **Next:** [23 – Mini Project 01](23-Mini-Project-03.md)

---

## 🎯 Objective

This project will help you practice **basic shell scripting and environment variables**.  
By the end of this project, you will be able to:

- Create and run simple shell scripts  
- Use variables, arguments, and environment variables  
- Make scripts executable  
- Understand how scripts interact with the Linux environment  

---

## 📂 Project Setup

1. Open your terminal  
2. Create a new project directory:
```bash
mkdir ~/mini-project-02
cd ~/mini-project-02
````

---

## 🛠 Tasks

### Task 1 – Create a Hello User Script

1. Create a file `greet.sh`:

```bash
nano greet.sh
```

2. Add the following content:

```bash
#!/bin/bash
# This script greets the current user
echo "Hello, $USER! Welcome to Linux."
```

3. Save and exit (`Ctrl + O`, `Enter`, `Ctrl + X`)

4. Make it executable:

```bash
chmod +x greet.sh
```

5. Run the script:

```bash
./greet.sh
```

✅ Expected Output:

```
Hello, <your_username>! Welcome to Linux.
```

---

### Task 2 – Use Environment Variables

1. Create a file `show_path.sh`:

```bash
nano show_path.sh
```

2. Add the following content:

```bash
#!/bin/bash
# Display important environment variables
echo "Your PATH: $PATH"
echo "Your HOME directory: $HOME"
echo "Current working directory: $PWD"
```

3. Save and exit, then make it executable:

```bash
chmod +x show_path.sh
```

4. Run the script:

```bash
./show_path.sh
```

✅ Expected Output:

```
Your PATH: /usr/local/bin:/usr/bin:/bin:...
Your HOME directory: /home/<your_username>
Current working directory: /home/<your_username>/mini-project-02
```

---

### Task 3 – Script with Arguments

1. Create a file `greet_person.sh`:

```bash
nano greet_person.sh
```

2. Add the following content:

```bash
#!/bin/bash
# Greet a person passed as an argument
if [ $# -eq 0 ]; then
  echo "Usage: ./greet_person.sh <name>"
else
  echo "Hello, $1! Nice to meet you."
fi
```

3. Save, exit, and make it executable:

```bash
chmod +x greet_person.sh
```

4. Run the script with an argument:

```bash
./greet_person.sh Rocky
```

✅ Expected Output:

```
Hello, Rocky! Nice to meet you.
```

5. Run without arguments to see the usage message:

```bash
./greet_person.sh
```

✅ Expected Output:

```
Usage: ./greet_person.sh <name>
```

---

### Task 4 – Explore Environment Commands

1. View all environment variables:

```bash
printenv
```

2. Check a specific variable:

```bash
printenv PATH
echo $HOME
```

3. Add a temporary environment variable:

```bash
export MYVAR="LinuxProject"
echo $MYVAR
```

4. Remove the variable:

```bash
unset MYVAR
```

✅ Expected Outcome:

* Able to view, create, and delete environment variables in a session

---

## ✅ Expected Outcomes

By the end of this project, you should be able to:

* Create simple Bash scripts
* Use variables and environment variables
* Accept command-line arguments in scripts
* Make scripts executable and run them
* Explore basic shell commands (`echo`, `printenv`, `export`, `unset`)

---

## 📝 Notes / Tips

* The first line `#!/bin/bash` is called the **shebang**, it tells Linux to use the Bash shell
* `$USER`, `$HOME`, `$PWD` are environment variables
* `$1` is the **first argument** passed to the script
* Use `chmod +x filename` to make scripts executable
* Test scripts carefully before adding more functionality

---

## 🎯 Learning Outcomes

By completing this project, you will:

* Gain confidence writing and running scripts
* Understand how to use environment variables in Linux
* Learn how to pass arguments to scripts
* Be prepared to write more complex scripts in future projects
