## **Day 3 – Operators**

**Project:** Build a “Smart Grade Calculator”

---

**01. Learning Goal**

By the end of this lesson, you will be able to:

- Use Python’s arithmetic, comparison, and logical operators  
- Understand operator precedence  
- Combine operators to create expressions  
- Build a small project that evaluates pass/fail and excellence  

---

**02. Problem Scenario**

You are designing a simple **“Smart Grade Calculator”**.  
The program will calculate total points, compare grades, and determine if a student passes or is excellent using logical operators.

---

**03. Step 1 – Arithmetic Operators**

Used for basic mathematical operations.  

|Operator|Meaning|Example|Result|
|---|---|---|---|
|`+`|Addition|`5 + 2`|7|
|`-`|Subtraction|`5 - 2`|3|
|`*`|Multiplication|`5 * 2`|10|
|`/`|Division (float)|`5 / 2`|2.5|
|`//`|Floor Division|`5 // 2`|2|
|`%`|Modulus (Remainder)|`5 % 2`|1|
|`**`|Exponentiation|`2 ** 3`|8|

Example:

```python
a = 7
b = 3
print(a + b)   # 10
print(a / b)   # 2.333...
print(a // b)  # 2
print(a % b)   # 1
print(a ** b)  # 343
```

---

**04. Step 2 – Comparison Operators**

Used to compare values. The result is always `True` or `False`.

| Operator | Meaning          | Example  | Result |
| -------- | ---------------- | -------- | ------ |
| `==`     | Equal to         | `5 == 5` | True   |
| `!=`     | Not equal to     | `5 != 3` | True   |
| `>`      | Greater than     | `5 > 3`  | True   |
| `<`      | Less than        | `5 < 3`  | False  |
| `>=`     | Greater or equal | `5 >= 5` | True   |
| `<=`     | Less or equal    | `3 <= 5` | True   |

Example:

```python
x = 10
y = 20
print(x == y)  # False
print(x != y)  # True
print(x < y)   # True
```

---

**05. Step 3 – Logical Operators**

Used to combine multiple conditions.

| Operator | Meaning            | Example          | Result |
| -------- | ------------------ | ---------------- | ------ |
| `and`    | Both must be True  | `True and False` | False  |
| `or`     | Either can be True | `True or False`  | True   |
| `not`    | Negation           | `not True`       | False  |

Example:

```python
age = 25
is_student = False

print(age > 18 and is_student)  # False (one is False)
print(age > 18 or is_student)   # True (one is True)
print(not is_student)           # True (negation)
```

---

**06. Step 4 – Operator Precedence**

Operations are executed in the following order:
**Multiplication / Division → Addition / Subtraction**
Use parentheses `( )` to control order.

```python
print(2 + 3 * 4)      # 14 (multiplication first)
print((2 + 3) * 4)    # 20 (parentheses first)
```

---

**07. Step 5 – Practice Examples**

**Example 1: Arithmetic Practice**

```python
x = 15
y = 4
print("Quotient:", x // y)
print("Remainder:", x % y)
print("Power:", x ** y)
```

**Example 2: Comparison Practice**

```python
temperature = 30
print("Is it hot?", temperature > 25)
print("Is it cold?", temperature < 10)
```

**Example 3: Logical Practice**

```python
score = 85
is_pass = score >= 60
is_excellent = score >= 90

print("Passed?", is_pass)
print("Excellent?", is_excellent)
print("Pass & Excellent?", is_pass and is_excellent)
```

---

**08. Step 6 – Mini Project: Smart Grade Calculator**

Build a program that evaluates a student’s performance.

```python
name = "Sabin"
score = 88

print(f"Student: {name}")
print("Passed?", score >= 60)
print("Excellent?", score >= 90)
print("Pass but not Excellent?", score >= 60 and score < 90)
```

---

**09. Reflection**

You have learned how to:

* Perform mathematical operations
* Compare and combine logical conditions
* Understand operator precedence
* Build a simple **Smart Grade Calculator**

This knowledge is essential for decision-making logic you’ll use in conditionals, loops, and full applications later.
