## **Day 20 – Python Standard Library**

**Project:** Build a “Utility Toolkit” using core Python standard modules (`math`, `random`, `datetime`, `time`, `os`).

---

**01. Learning Goal**

By the end of this lesson, you will be able to:

- Use Python’s built-in **standard libraries** effectively  
- Perform mathematical operations with `math`  
- Generate random numbers with `random`  
- Work with dates and time using `datetime` and `time`  
- Manage files and folders with `os`  

---

**02. Problem Scenario**

You’re developing a small automation program and need tools for math calculations, random data generation, time management, and file handling — all without installing extra libraries.  
Luckily, Python’s **Standard Library** already provides everything you need.

---

**03. Step 1 – math module (Mathematical Operations)**

Provides mathematical functions like square roots, powers, factorials, and constants such as π.

```python
import math

print(math.sqrt(16))    # Square root
print(math.pow(2, 3))   # Power
print(math.factorial(5)) # Factorial
print(math.pi)          # Pi constant

print(math.ceil(3.2))   # Ceiling (round up)
print(math.floor(3.9))  # Floor (round down)
```

---

**04. Step 2 – random module (Random Number Generation)**

Generate random integers, choices, or samples — useful for games, simulations, and testing.

```python
import random

print(random.randint(1, 6))               # Random integer (1–6)
print(random.choice(["Apple", "Banana", "Grape"]))  # Random choice
print(random.sample(range(1, 46), 6))    # Lotto numbers
```

---

**05. Step 3 – datetime module (Date and Time Handling)**

Work with current dates, format conversions, and time calculations.

```python
from datetime import datetime, timedelta

now = datetime.now()
print("Now:", now)

d = datetime(2025, 1, 1, 9, 0)
print("Specific Date:", d)

tomorrow = now + timedelta(days=1)
print("Tomorrow:", tomorrow)

date_str = "2025-09-11 18:30"
dt = datetime.strptime(date_str, "%Y-%m-%d %H:%M")
print("Parsed:", dt)

print(dt.strftime("%Y-%m-%d %H:%M"))
print(dt.strftime("%Y년 %m월 %d일 %H시 %M분"))
```

---

**06. Step 4 – time module (Delay and Execution Control)**

Pause your program or measure execution duration.

```python
import time

print("Wait 3 seconds...")
time.sleep(3)
print("Done!")
```

---

**07. Step 5 – os module (Operating System Interaction)**

Manage files, folders, and paths.

```python
import os

print("Current Working Directory:", os.getcwd())
os.mkdir("test_folder")
os.rmdir("test_folder")
```

---

**08. Step 6 – Practice Examples**

**Example 1: Circle Area Calculator**

```python
import math

r = 5
area = math.pi * r**2
print("Circle Area:", area)
```

---

**Example 2: Lotto Number Generator**

```python
import random

lotto = random.sample(range(1, 46), 6)
print("Lotto Numbers:", lotto)
```

---

**Example 3: Today’s Date Formatter**

```python
from datetime import datetime

today = datetime.today()
print("Today:", today.strftime("%Y-%m-%d"))
```

---

**09. Step 7 – Mini Project: Utility Toolkit**

Combine all modules into one useful “Utility Toolkit”.

```python
import math, random, time, os
from datetime import datetime

print("--- Utility Toolkit ---")

# 1. Math
r = 4
print("Circle Area:", math.pi * r**2)

# 2. Random
numbers = random.sample(range(1, 46), 6)
print("Random Numbers:", numbers)

# 3. Date & Time
print("Now:", datetime.now().strftime("%Y-%m-%d %H:%M"))

# 4. Delay Example
print("Processing...")
time.sleep(2)
print("Done!")

# 5. OS
print("Current Folder:", os.getcwd())
```

Output example:

```
--- Utility Toolkit ---
Circle Area: 50.26548245743669
Random Numbers: [8, 21, 34, 45, 12, 3]
Now: 2025-10-04 16:10
Processing...
Done!
Current Folder: /Users/sabin/projects
```

---

**10. Reflection**

You have learned how to:

* Use core modules (`math`, `random`, `datetime`, `time`, `os`)
* Format and calculate with dates
* Generate random sequences and delays
* Interact with your file system safely
* Build a complete **Utility Toolkit** using only built-in Python features
