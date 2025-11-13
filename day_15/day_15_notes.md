## **Day 15 – Functions (def, return, parameters)**

**Project:** Build a “Simple Calculator” using user-defined functions

---

**01. Learning Goal**

By the end of this lesson, you will be able to:

- Define and call your own functions using `def`  
- Pass values into functions using parameters  
- Return results using `return`  
- Understand default parameters and multiple return values  

---

**02. Problem Scenario**

You often repeat the same code for arithmetic operations.  
Your goal is to **modularize your code** by creating reusable functions to handle these tasks.

---

**03. Step 1 – What is a Function?**

A **function** is a reusable block of code that performs a specific task.  
You must **define** it first, then **call** it.

```python
def say_hello():
    print("Hello!")

say_hello()   # Function call
```

---

**04. Step 2 – Using Parameters**

Functions can receive data through **parameters**.

```python
def greet(name):
    print(f"Nice to meet you, {name}!")

greet("Sabin")   # Nice to meet you, Sabin!
```

---

**05. Step 3 – Returning Values**

Functions can **return** results using `return`.

```python
def add(a, b):
    return a + b

result = add(3, 5)
print(result)   # 8
```

---

**06. Step 4 – Returning Multiple Values**

Python functions can return more than one value at once (as a tuple).

```python
def calc(a, b):
    return a + b, a - b, a * b

s, d, m = calc(10, 5)
print(s, d, m)   # 15 5 50
```

---

**07. Step 5 – Default Parameters**

A parameter can have a default value, used when no argument is provided.

```python
def greet(name="Guest"):
    print(f"Hello, {name}")

greet()          # Hello, Guest
greet("Sabin")   # Hello, Sabin
```

---

**08. Step 6 – Functions with Loops**

You can combine loops with functions for repetitive calculations.

```python
def square(n):
    return n * n

for i in range(1, 6):
    print(square(i))
```

---

**09. Step 7 – Practice Examples**

**Example 1: Basic Calculator Functions**

```python
def add(a, b):
    return a + b

def sub(a, b):
    return a - b

print("Add:", add(10, 5))
print("Subtract:", sub(10, 5))
```

**Example 2: String Function**

```python
def shout(text):
    return text.upper() + "!!!"

print(shout("python"))   # PYTHON!!!
```

---

**10. Step 8 – Mini Project: Simple Calculator**

Build a mini calculator that performs multiple operations using functions.

```python
def add(a, b): return a + b
def sub(a, b): return a - b
def mul(a, b): return a * b
def div(a, b): return a / b if b != 0 else "Error: Division by zero"

a = float(input("Enter first number: "))
b = float(input("Enter second number: "))

print("Add:", add(a, b))
print("Subtract:", sub(a, b))
print("Multiply:", mul(a, b))
print("Divide:", div(a, b))
```

---

**11. Reflection**

You have learned how to:

* Define and call custom functions
* Use parameters and return statements
* Handle multiple results and default values
* Build a **Simple Calculator** using clean, modular code
