## **Day 4 – Input & Output**

**Project:** Create an “Interactive Greeting App”

---

**01. Learning Goal**

By the end of this lesson, you will be able to:

- Display information using `print()`  
- Receive user input using `input()`  
- Format messages neatly with f-strings  
- Build an interactive console program  

---

**02. Problem Scenario**

You are creating a small interactive app that asks for the user’s name and age,  
then prints a personalized greeting with properly formatted text and numbers.

---

**03. Step 1 – Output with `print()`**

The `print()` function displays text or variable values on screen.  
You can separate multiple values with commas — Python will add spaces automatically.

```python
print("Hello!")
print("Age:", 25, "years old")
# Output: Age: 25 years old
```

---

**04. Step 2 – Input with `input()`**

The `input()` function reads **user input as a string (`str`)**.
Use a prompt message to ask the user for data.

```python
name = input("Enter your name: ")
print("Hello,", name)
```

**Note:** Input values are always strings, so convert them with `int()` if you need numbers.

```python
age = int(input("Enter your age: "))
print("Next year, you’ll be", age + 1)
```

---

**05. Step 3 – Using f-strings (Formatted Strings)**

An f-string allows you to insert variables directly into strings.
Just prefix the string with `f` and use `{}` to include variables.

```python
name = "Sabin"
age = 25
print(f"My name is {name}, and I am {age} years old.")
```

You can also format numbers easily:

```python
pi = 3.141592
print(f"Pi is approximately {pi:.2f}")   # 3.14
```

---

**06. Step 4 – Multi-line Output**

To print multiple lines at once, use triple quotes (`""" """` or `''' '''`).

```python
msg = """Starting Python study!
Today we learn about input and output.
"""
print(msg)
```

---

**07. Step 5 – Practice Examples**

**Example 1: Input + Output**

```python
food = input("What’s your favorite food? ")
print("Your favorite food is", food, "!")
```

**Example 2: f-string Practice**

```python
name = input("Enter your name: ")
age = int(input("Enter your age: "))
print(f"{name}, you are {age} years old. Next year, you'll be {age + 1}!")
```

**Example 3: Floating-point Output**

```python
num = 3.14159
print(f"One decimal place: {num:.1f}")
print(f"Three decimal places: {num:.3f}")
```

---

**08. Step 6 – Mini Project: Interactive Greeting App**

Now combine everything to create your own **interactive greeting program**.

```python
name = input("What is your name? ")
age = int(input("How old are you? "))
print(f"Nice to meet you, {name}!")
print(f"Next year, you’ll be {age + 1} years old.")
```

---

**09. Reflection**

You have learned how to:

* Display messages using `print()`
* Accept user input with `input()`
* Format text using f-strings
* Build an **interactive console application**

This knowledge is the foundation for building real-world applications that interact dynamically with users.
