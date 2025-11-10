## **Day 6 – Loops (for / range)**

**Project:** Build a “Multiplication Table Generator”

---

**01. Learning Goal**

By the end of this lesson, you will be able to:

- Understand how `for` loops work in Python  
- Use the `range()` function for numeric repetition  
- Combine loops with lists, strings, and nested loops  
- Build a program that generates a multiplication table  

---

**02. Problem Scenario**

You want to repeat actions automatically — for example,  
printing every fruit in a basket or generating a multiplication table.  
Manually typing each line is inefficient. Loops can automate this process.

---

**03. Step 1 – What is a Loop?**

A loop repeats a block of code multiple times.  
In Python, there are two main types: `for` and `while`.  
Today, we focus on `for`.

---

**04. Step 2 – Basic for Loop**

The `for` loop iterates over **iterable objects** such as lists, strings, or ranges.

```python
fruits = ["apple", "banana", "grape"]

for f in fruits:
    print(f)
```

**Output:**

```
apple
banana
grape
```

---

**05. Step 3 – Using the range() Function**

`range()` generates a sequence of numbers — commonly used for numeric loops.

```python
# range(stop)
# range(start, stop)
# range(start, stop, step)

for i in range(5):
    print(i)   # 0, 1, 2, 3, 4

for i in range(1, 6):
    print(i)   # 1, 2, 3, 4, 5

for i in range(2, 11, 2):
    print(i)   # 2, 4, 6, 8, 10
```

---

**06. Step 4 – Nested Loops**

A loop can contain another loop — this is called a **nested loop**.

```python
for i in range(2, 4):       # 2, 3
    for j in range(1, 4):   # 1, 2, 3
        print(i, "*", j, "=", i * j)
```

---

**07. Step 5 – Looping Through Strings**

Strings are also iterable, so each character can be processed individually.

```python
for ch in "Python":
    print(ch)
```

---

**08. Step 6 – Practice Examples**

**Example 1: Sum of 1 to 10**

```python
total = 0
for i in range(1, 11):
    total += i
print("Sum:", total)
```

**Example 2: Multiplication Table (2 Times)**

```python
for i in range(1, 10):
    print(f"2 x {i} = {2 * i}")
```

**Example 3: Looping Through a List**

```python
names = ["Tom", "Anna", "Sabin"]

for n in names:
    print(f"Hello, {n}!")
```

---

**09. Step 7 – Mini Project: Multiplication Table Generator**

Now create a program that prints any multiplication table the user requests.

```python
dan = int(input("Enter a number to generate its table: "))

for i in range(1, 10):
    print(f"{dan} x {i} = {dan * i}")
```

---

**10. Reflection**

You learned how to:

* Automate repetitive tasks using loops
* Iterate over lists, strings, and numeric sequences
* Use nested loops to handle structured patterns
* Build a functional **Multiplication Table Generator**

