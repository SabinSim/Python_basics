## **Day 18 – Lambda Functions (Anonymous Functions)**

**Project:** Build a “Quick Data Transformer” using lambda, map, filter, and reduce.

---

**01. Learning Goal**

By the end of this lesson, you will be able to:

- Understand what **lambda functions** are and when to use them  
- Replace small `def` functions with concise `lambda` expressions  
- Use lambda with **map()**, **filter()**, and **reduce()**  
- Apply lambda for sorting and conditional expressions  

---

**02. Problem Scenario**

Imagine you’re working on a data processing app that needs to perform quick operations  
— squaring numbers, filtering values, or sorting strings — all in one line.  
Instead of defining a new function each time, you can use **lambda functions** to simplify your code.

---

**03. Step 1 – What is a Lambda Function?**

A lambda function is a **small anonymous function** written in one line.

Syntax:  
`lambda arguments: expression`

```python
add = lambda x, y: x + y
print(add(3, 5))   # 8
```

Use lambda when you need a **simple function for short-term use**.

---

**04. Step 2 – Regular vs Lambda Function**

```python
# Regular function
def square(x):
    return x * x

# Lambda function
square2 = lambda x: x * x

print(square(4))   # 16
print(square2(4))  # 16
```

Both work the same — but lambda makes your code shorter and cleaner.

---

**05. Step 3 – Common Uses of Lambda Functions**

### 1️⃣ Sorting with `key`

```python
nums = [3, 1, 5, 2, 4]
nums.sort(key=lambda x: -x)
print(nums)   # [5, 4, 3, 2, 1]
```

---

### 2️⃣ Using `map()` – Apply a Function to All Elements

```python
numbers = [1, 2, 3, 4]
squares = list(map(lambda x: x**2, numbers))
print(squares)   # [1, 4, 9, 16]
```

---

### 3️⃣ Using `filter()` – Keep Only Matching Items

```python
numbers = [10, 15, 20, 25]
even = list(filter(lambda x: x % 2 == 0, numbers))
print(even)   # [10, 20]
```

---

### 4️⃣ Using `reduce()` – Combine All Elements

```python
from functools import reduce

numbers = [1, 2, 3, 4]
product = reduce(lambda x, y: x * y, numbers)
print(product)   # 24
```

---

**06. Step 4 – Lambda with Conditions**

You can use **conditional expressions** directly inside lambda.

```python
max_num = lambda a, b: a if a > b else b
print(max_num(10, 20))   # 20
```

---

**07. Step 5 – Practice Examples**

**Example 1: Sort Words by Length**

```python
words = ["apple", "banana", "kiwi"]
words.sort(key=lambda w: len(w))
print(words)   # ['kiwi', 'apple', 'banana']
```

---

**Example 2: Filter Odd Numbers**

```python
nums = [1, 2, 3, 4, 5]
odds = list(filter(lambda n: n % 2 == 1, nums))
print(odds)   # [1, 3, 5]
```

---

**Example 3: Convert Celsius to Fahrenheit**

```python
temps_c = [0, 10, 20, 30]
temps_f = list(map(lambda c: (c * 9/5) + 32, temps_c))
print(temps_f)   # [32.0, 50.0, 68.0, 86.0]
```

---

**08. Step 6 – Mini Project: Quick Data Transformer**

Let’s combine what you’ve learned into a simple data processing tool.

```python
from functools import reduce

numbers = [2, 4, 6, 8, 10]

# Square numbers
squares = list(map(lambda x: x**2, numbers))

# Filter values greater than 20
filtered = list(filter(lambda x: x > 20, squares))

# Sum them all
total = reduce(lambda x, y: x + y, filtered)

print("Original:", numbers)
print("Squares:", squares)
print("Filtered (>20):", filtered)
print("Total:", total)
```

---

**09. Reflection**

You have learned how to:

* Write **lambda functions** as one-line anonymous functions
* Combine lambda with **map**, **filter**, and **reduce**
* Use lambda for sorting, filtering, and transforming data
* Build a **Quick Data Transformer** that processes lists efficiently
