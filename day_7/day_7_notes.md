## **Day 7 – While Loop + Mini Projects**

**Project:** Build an Interactive Number Game & Calculator

---

**01. Learning Goal**

By the end of this lesson, you will be able to:

- Use `while` loops to repeat tasks based on conditions  
- Understand infinite loops, `break`, and `continue`  
- Compare `for` and `while` loops  
- Build interactive console programs (number guessing, calculator, etc.)  

---

**02. Problem Scenario**

You want your program to keep running **until a condition changes** — for example,  
asking users for passwords, summing numbers, or repeating actions until the correct answer is given.  
The `while` loop helps make your program more dynamic and interactive.

---

**03. Step 1 – Basic While Loop Structure**

A `while` loop runs **as long as its condition is `True`**.  
When the condition becomes `False`, the loop ends.

```python
count = 1

while count <= 5:
    print("Hello", count)
    count += 1
```

**Output:**

```
Hello 1
Hello 2
Hello 3
Hello 4
Hello 5
```

---

**04. Step 2 – Infinite Loop & break**

A loop with `while True` runs forever unless stopped with `break`.

```python
while True:
    cmd = input("Type 'q' to quit: ")
    if cmd == "q":
        print("Program terminated!")
        break
```

---

**05. Step 3 – continue Statement**

`continue` skips the rest of the loop and goes back to the next iteration.

```python
num = 0

while num < 10:
    num += 1
    if num % 2 == 0:
        continue
    print(num)  # Prints only odd numbers
```

---

**06. Step 4 – for vs while**

* **for loop:** When you know *how many times* to repeat.
* **while loop:** When repetition depends on *a condition*.

| Loop Type | When to Use                 | Example                  |
| --------- | --------------------------- | ------------------------ |
| `for`     | Fixed number of repetitions | Iterating through a list |
| `while`   | Conditional repetition      | Waiting for user input   |

---

**07. Step 5 – Practice Examples**

**Example 1: Print Numbers from 1 to 10**

```python
n = 1
while n <= 10:
    print(n)
    n += 1
```

**Example 2: Password Checker**

```python
password = "1234"

while True:
    guess = input("Enter password: ")
    if guess == password:
        print("Login successful!")
        break
    else:
        print("Incorrect password. Try again.")
```

---

**08. Step 6 – Mini Projects**

**(1) Multiplication Table (구구단 출력기)**

```python
dan = int(input("Enter a number: "))
i = 1

while i <= 9:
    print(f"{dan} x {i} = {dan * i}")
    i += 1
```

---

**(2) Sum Calculator**

Keep accepting numbers until the user enters `0`,
then print the total sum.

```python
total = 0

while True:
    num = int(input("Enter a number (0 to stop): "))
    if num == 0:
        break
    total += num

print("Total Sum:", total)
```

---

**(3) Number Guessing Game**

```python
import random

secret = random.randint(1, 20)
tries = 0

while True:
    guess = int(input("Guess the number (1–20): "))
    tries += 1
    if guess == secret:
        print(f"Correct! You guessed it in {tries} tries.")
        break
    elif guess < secret:
        print("Try a higher number.")
    else:
        print("Try a lower number.")
```

---

**09. Reflection**

You have learned how to:

* Use `while` loops for dynamic repetition
* Break out of infinite loops with `break`
* Skip specific iterations with `continue`
* Build **interactive projects** such as a password system, calculator, and guessing game
