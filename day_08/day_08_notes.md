## **Day 8 – Lists**

**Project:** Build a “Simple Data Manager” using Lists
 
---

**01. Learning Goal**

By the end of this lesson, you will be able to:

- Create and modify Python lists  
- Use indexing and slicing  
- Apply common list methods (`append`, `insert`, `sort`, etc.)  
- Work with nested lists  
- Build a small program that manages and analyzes list data  

---

**02. Problem Scenario**

You often need to store multiple pieces of data — like names, scores, or items.  
Instead of creating multiple variables, lists let you organize all values in one place.  
Your goal: use lists to store, update, and process data efficiently.

---

**03. Step 1 – What is a List?**

A list stores multiple values in order, enclosed by square brackets `[ ]`.

```python
fruits = ["apple", "banana", "grape"]
numbers = [10, 20, 30, 40]
mixed = [1, "Hello", True, 3.14]
```

**Key Features:**

* Ordered (index starts at 0)
* Mutable (you can change values after creation)

---

**04. Step 2 – Indexing and Slicing**

Access elements by index or select sublists using slicing.

```python
fruits = ["apple", "banana", "grape", "strawberry"]

print(fruits[0])    # apple
print(fruits[2])    # grape
print(fruits[-1])   # strawberry

print(fruits[1:3])  # ['banana', 'grape']
print(fruits[:2])   # ['apple', 'banana']
print(fruits[2:])   # ['grape', 'strawberry']
```

---

**05. Step 3 – Modifying Lists**

Lists can be updated directly by index.

```python
fruits = ["apple", "banana", "grape"]

fruits[1] = "mango"
print(fruits)  # ['apple', 'mango', 'grape']
```

---

**06. Step 4 – Common List Methods**

```python
numbers = [3, 1, 4]

numbers.append(5)        # Add to end
numbers.insert(1, 100)   # Insert at index 1
numbers.remove(1)        # Remove by value
numbers.pop()            # Remove last element

print(numbers.index(100))   # Find index of a value
print(numbers.count(4))     # Count occurrences

numbers.sort()           # Sort ascending
numbers.reverse()        # Reverse order

print(numbers)
```

---

**07. Step 5 – Lists and Loops**

You can iterate through a list directly or with index tracking.

```python
fruits = ["apple", "banana", "grape"]

for f in fruits:
    print(f)

for i, f in enumerate(fruits):
    print(i, f)
```

---

**08. Step 6 – Nested Lists**

Lists can contain other lists — useful for representing tables or grids.

```python
matrix = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

print(matrix[0][1])  # 2
print(matrix[2][2])  # 9
```

---

**09. Step 7 – Practice Examples**

**Example 1: Replace an Item**

```python
fruits = ["apple", "banana", "grape"]
fruits[1] = "strawberry"
print(fruits)
```

**Example 2: Calculate Total**

```python
numbers = [10, 20, 30, 40]
total = 0
for n in numbers:
    total += n
print("Total:", total)
```

**Example 3: Find Max and Min**

```python
numbers = [3, 7, 2, 9, 5]
print("Max:", max(numbers))
print("Min:", min(numbers))
```

---

**10. Step 8 – Mini Project: Simple Data Manager**

Create a small program to store and analyze a list of numbers.

```python
scores = [88, 92, 79, 93, 85]

print("All scores:", scores)
print("Average:", sum(scores) / len(scores))
print("Highest:", max(scores))
print("Lowest:", min(scores))
```

---

**11. Reflection**

You have learned how to:

* Store, access, and modify list elements
* Use loops and methods to process list data
* Create and work with nested lists
* Build a **Simple Data Manager** to analyze values
