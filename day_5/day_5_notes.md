## **Day 5 – Conditional Statements (if / elif / else)**

**Project:** Create a “Smart Login & Grade Evaluator”

---

**01. Learning Goal**

By the end of this lesson, you will be able to:

- Understand and use Python conditional statements  
- Combine comparison and logical operators in conditions  
- Build nested conditions for complex logic  
- Create a mini project that checks grades and simulates login  

---

**02. Problem Scenario**

You are designing a **Smart Evaluator App** that decides different outcomes:  
whether someone is an adult, what their grade is, and whether login credentials are correct.

---

**03. Step 1 – Basic if Statement**

A condition executes only when it is **True**.

```python
age = 20

if age >= 18:
    print("You are an adult.")
```

⚠️ **Indentation matters!**
Python relies on consistent indentation (recommended: 4 spaces).

---

**04. Step 2 – if ~ else**

If the condition is true → run the `if` block.
If false → run the `else` block.

```python
age = 15

if age >= 18:
    print("Adult")
else:
    print("Minor")
```

---

**05. Step 3 – if ~ elif ~ else**

Used for checking multiple conditions in sequence.
Python executes the **first True condition only**.

```python
score = 85

if score >= 90:
    print("Grade A")
elif score >= 80:
    print("Grade B")
elif score >= 70:
    print("Grade C")
else:
    print("Grade F")
```

---

**06. Step 4 – Nested if (Conditions within Conditions)**

You can place one `if` statement inside another for more complex logic.

```python
age = 20
is_student = True

if age >= 18:
    if is_student:
        print("Adult student.")
    else:
        print("Adult but not a student.")
```

---

**07. Step 5 – Logical Operators in Conditions**

You can combine multiple conditions using `and`, `or`, `not`.

```python
temp = 25

if temp > 20 and temp < 30:
    print("The weather is warm.")
```

---

**08. Step 6 – Practice Examples**

**Example 1: Even or Odd**

```python
num = int(input("Enter a number: "))

if num % 2 == 0:
    print("Even number.")
else:
    print("Odd number.")
```

**Example 2: Age Group Classifier**

```python
age = int(input("Enter your age: "))

if age < 13:
    print("Child")
elif age < 20:
    print("Teenager")
else:
    print("Adult")
```

**Example 3: Login Simulation**

```python
user_id = input("Enter ID: ")
password = input("Enter password: ")

if user_id == "admin" and password == "1234":
    print("Login successful!")
else:
    print("Login failed!")
```

---

**09. Step 7 – Mini Project: Smart Login & Grade Evaluator**

Combine multiple conditions into one program that evaluates both login and performance.

```python
user_id = input("Enter ID: ")
password = input("Enter password: ")

if user_id == "admin" and password == "1234":
    print("✅ Login successful!")
    score = int(input("Enter your score: "))

    if score >= 90:
        print("Excellent performance! Grade A")
    elif score >= 75:
        print("Good job! Grade B")
    elif score >= 60:
        print("You passed. Grade C")
    else:
        print("Failed. Try again next time.")
else:
    print("❌ Invalid credentials. Access denied.")
```

---

**10. Reflection**

You have learned how to:

* Use conditional statements to control program flow
* Combine logical and comparison operators
* Apply nested conditions for complex decisions
* Build a working **Smart Evaluator** program

