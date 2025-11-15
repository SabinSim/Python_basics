## **Day 19 – Modules & Packages (import, from, __main__)**

**Project:** Build a modular “Math & Greeting Toolkit” that imports and reuses your own functions.

---

**01. Learning Goal**

By the end of this lesson, you will be able to:

- Understand what **modules** and **packages** are  
- Import both built-in and custom Python modules  
- Use **from-import**, **aliasing**, and **__main__** effectively  
- Organize your code for **reusability and clarity**

---

**02. Problem Scenario**

As your projects grow, you’ll want to organize your code into smaller, reusable files.  
Instead of putting everything into one Python file, you’ll learn to use **modules** and **packages** to make your project scalable and clean.

---

**03. Step 1 – What is a Module?**

A **module** is simply a Python file (`.py`) that contains functions, classes, or variables.  
You can import it into another file to reuse its code.

Example: using Python’s built-in `math` module

```python
import math

print(math.sqrt(16))   # 4.0
print(math.pi)         # 3.141592...
```

---

**04. Step 2 – Different Ways to Import**

You can import modules in multiple ways depending on your use case.

```python
# Import the entire module
import math
print(math.sqrt(25))

# Import specific functions
from math import sqrt, pi
print(sqrt(25), pi)

# Use an alias for convenience
import math as m
print(m.sqrt(36))
```

---

**05. Step 3 – Creating Your Own Module**

You can create your own Python file and reuse it as a module.

**calc.py**

```python
def add(a, b):
    return a + b

def sub(a, b):
    return a - b
```

**main.py**

```python
import calc

print(calc.add(3, 5))   # 8
print(calc.sub(10, 7))  # 3
```

When you import `calc`, Python automatically runs that file once and gives access to its functions.

---

**06. Step 4 – What is a Package?**

A **package** is a folder that contains multiple modules.
It must include an `__init__.py` file to be recognized as a package.

```
my_package/
    __init__.py
    math_ops.py
    string_ops.py
```

```python
from my_package import math_ops
print(math_ops.add(2, 3))
```

Packages make it easy to group related modules together for large-scale projects.

---

**07. Step 5 – The `__name__` and `__main__` Check**

Every Python file can act as either:

1. **A script** (run directly)
2. **A module** (imported into another file)

You can distinguish them using `if __name__ == "__main__":`

```python
# test.py
def hello():
    print("Hello!")

if __name__ == "__main__":
    hello()
```

When executed directly:

```bash
$ python test.py
Hello!
```

When imported:

```python
import test
# Does not print automatically
```

This allows you to include test code or demos that run **only when executed directly**.

---

**08. Step 6 – Installing External Libraries**

You can install third-party libraries using **pip**.

```bash
pip install requests
```

Then, use it in your project:

```python
import requests

res = requests.get("https://api.github.com")
print(res.status_code)
```

---

**09. Step 7 – Practice Examples**

**Example 1: Standard Module**

```python
import random

print(random.randint(1, 6))   # Roll a dice
```

---

**Example 2: Custom Module**

**greet.py**

```python
def say_hello(name):
    return f"Hello, {name}!"
```

**main.py**

```python
import greet
print(greet.say_hello("Sabin"))
```

---

**10. Step 8 – Mini Project: Math & Greeting Toolkit**

Let’s build a simple package that combines math and greeting modules.

**project structure**

```
toolkit/
    __init__.py
    math_tools.py
    greet_tools.py
main.py
```

**math_tools.py**

```python
def add(a, b):
    return a + b

def multiply(a, b):
    return a * b
```

**greet_tools.py**

```python
def greet(name):
    return f"Welcome, {name}!"
```

**main.py**

```python
from toolkit import math_tools, greet_tools

print(math_tools.add(10, 5))
print(greet_tools.greet("Sabin"))
```

Output:

```
15
Welcome, Sabin!
```

---

**11. Reflection**

You have learned how to:

* Import built-in and custom **modules**
* Organize multiple files into **packages**
* Use `__main__` to separate test code from imports
* Build your own **Math & Greeting Toolkit** for reusable code
