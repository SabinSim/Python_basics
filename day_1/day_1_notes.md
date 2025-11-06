Markdown

# 🐍 Day 1 – Python Setup & Basic Functions (`print`, `type`)

## Project: Build Your First “Python Greeting App”

### 01. Learning Goal

By the end of this lesson, you will be able to:

* **Set up** a Python environment on your computer (VS Code integration).
* Use `print()` to display messages dynamically.
* Use `type()` to check data types.
* Write a simple, functioning Python script.

---

### 02. Problem Scenario

You’ve just installed Python and VS Code, and you need to verify that everything works. Your mission: Create a small **“Greeting App”** that prints a personalized message using your name and age, and displays their data types.

### 03. Step 1 – Set Up Your Environment

1.  Install **Python 3.10** or newer → [python.org/downloads](https://www.python.org/downloads/)
2.  Install **VS Code** (your development environment).
3.  Check your Python installation via the terminal:

```bash
python --version   # Check Python version
python             # Enter Python shell
exit()             # Exit the shell
If you see something like Python 3.11.x, you’re ready.
```
04. Step 2 – Display Output with `print()`
`print()` outputs text or variable values to the screen.

```Python

# Simple message
print("Hello, Python!")

# Print multiple values
print("My age is", 35)

# Print using f-string (highly recommended for modern Python)
name = "Sabin"
print(f"My name is {name}")
```
Why it matters: print() is your main debugging tool—it shows what your code is doing in real-time.

05. Step 3 – Inspect Data Types with type()
`type()` returns the data type of any variable—essential for understanding what your code is handling.

```Python

a = 10
print(type(a))   # <class 'int'>

b = 3.14
print(type(b))   # <class 'float'>

c = "Hello"
print(type(c))   # <class 'str'>

d = True
print(type(d))   # <class 'bool'>
```
Insight: Knowing your data types prevents logical errors and helps ensure correct operation during complex tasks.

06. Step 4 – Mini Project: “Python Greeting App”
Combine what you learned to build a small, meaningful script.

```Python

name = "Sabin"
age = 30

print(f"My name is {name}, and I am {age} years old.")
print("Name Type:", type(name))
print("Age Type:", type(age))
```
Expected Output:
```Python
My name is Sabin, and I am 30 years old.
Name Type: <class 'str'>
Age Type: <class 'int'>
```
07. Practice Tasks
Modify the code to ask for user input using `input()` (e.g., name and age).

Add a new variable `is_student` = True and print its type.

Experiment with changing `age` to a float `(30.5)` and check the new type.

08. Reflection
You successfully: Installed and verified Python, used `print()` to output text and variables, checked data types using `type()`, and built a working Greeting App.

🔍 This foundational knowledge will be reused in almost every Python project you create—whether for data analysis, web apps, or automation.
