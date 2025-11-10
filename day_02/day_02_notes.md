## **Day 2 – Variables and Data Types**

**Project:** Build a “User Info Display App”

---

**01. Learning Goal**

By the end of this lesson, you will be able to:

- Understand what variables are and how to use them  
- Work with Python’s basic data types (`int`, `float`, `str`, `bool`)  
- Convert between data types using casting  
- Build a simple Python app that prints user information  

---

**02. Problem Scenario**

You are creating a small program that stores user details such as name, age, and height.  
Your goal is to correctly assign values to variables, identify their data types, and display them on screen.

---

**03. Step 1 – What Is a Variable?**

A **variable** is like a label used to store data.  
Use the `=` operator to assign values.

```python
x = 10          # Integer (int)
y = 3.14        # Float
name = "Sabin"  # String (str)
is_ok = True    # Boolean (bool)
```

---

**04. Step 2 – Primitive Data Types**

**Integers (`int`)**
Example: `age = 25` → `print(age, type(age))` will show `25 <class 'int'>`.

**Floats (`float`)**
Example: `pi = 3.14159` → `print(pi, type(pi))` outputs `3.14159 <class 'float'>`.

**Strings (`str`)**
Example: `greeting = "Hello"` → `print(greeting, type(greeting))` gives `Hello <class 'str'>`.

**Booleans (`bool`)**
Example: `is_student = True` → `print(is_student, type(is_student))` outputs `True <class 'bool'>`.

---

**05. Step 3 – Variable Naming Rules**

Follow these rules:

* ✅ Use letters, numbers, and underscores (`_`)
* ❌ Do not start with a number
* ✅ Case-sensitive (`Name` ≠ `name`)
* ✅ Use meaningful names

Example of good vs bad naming:

```python
a = 10               # ❌ Not descriptive
student_age = 20     # ✅ Clear and meaningful
```

---

**06. Step 4 – Type Casting (Data Conversion)**

Convert between types using built-in functions.

```python
x = 10
print(float(x))  # int → float: 10.0

y = 3.99
print(int(y))    # float → int: 3

num_str = "100"
print(int(num_str) + 1)  # str → int: 101

age = 25
print("Age: " + str(age))  # int → str: Age: 25
```

---

**07. Step 5 – Mini Project: User Info Display App**

Combine everything to display user info in one script.

```python
name = "Sabin"
age = 30
height = 175.5
is_student = False

print("Name:", name)
print("Age:", age)
print("Height:", height)
print("Is student?", is_student)
```

---

**08. Practice Task**

1. Ask the user for their name and age using `input()`.
2. Convert the age to an integer and calculate next year’s age.
3. Display the result using an f-string.

```python
name = input("Enter your name: ")
age = int(input("Enter your age: "))
print(f"Hi {name}! You'll be {age + 1} next year.")
```

---

**09. Reflection**

You have learned to:

* Use variables to store values
* Work with `int`, `float`, `str`, and `bool` types
* Convert between types using casting
* Build a simple **User Info App** that prints formatted output
