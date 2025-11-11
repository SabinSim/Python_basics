## **Day 11 – Tuples & Sets**

**Project:** Build a “Unique Data Manager” using Tuples and Sets

---

**01. Learning Goal**

By the end of this lesson, you will be able to:

- Understand the difference between **lists**, **tuples**, and **sets**  
- Use tuples for immutable, ordered data  
- Use sets for unique, unordered collections  
- Apply set operations like union, intersection, and difference  

---

**02. Problem Scenario**

You often need to store data that shouldn’t change (e.g., constants)  
or remove duplicates from a dataset.  
Your goal today: learn how **tuples** and **sets** help manage such cases efficiently.

---

**03. Step 1 – What is a Tuple?**

A **tuple** stores multiple values in order but cannot be modified.

```python
fruits = ("apple", "banana", "grape")
print(fruits[0])   # apple
print(fruits[-1])  # grape
```

**Key Traits:**

* Ordered
* Immutable (cannot be changed)
* Uses parentheses `( )`

---

**04. Step 2 – Tuple vs List**

```python
list1 = [1, 2, 3]      # List: mutable
tuple1 = (1, 2, 3)     # Tuple: immutable

list1[0] = 100     # ✅ Allowed
# tuple1[0] = 100  # ❌ Error (cannot modify)
```

---

**05. Step 3 – Practical Use: Return Multiple Values**

Tuples are often used for returning multiple results from a function.

```python
def calc(a, b):
    return a + b, a - b

result = calc(5, 2)
print(result)   # (7, 3)
```

---

**06. Step 4 – What is a Set?**

A **set** stores **unique** values with **no specific order**.

```python
nums = {1, 2, 3, 3, 4}
print(nums)   # {1, 2, 3, 4} (duplicates removed)
```

**Key Traits:**

* Unordered
* No duplicates
* Uses curly braces `{ }`

---

**07. Step 5 – Set Operations**

Sets are great for mathematical operations.

```python
a = {1, 2, 3}
b = {3, 4, 5}

print(a | b)   # Union → {1, 2, 3, 4, 5}
print(a & b)   # Intersection → {3}
print(a - b)   # Difference → {1, 2}
print(a ^ b)   # Symmetric Difference → {1, 2, 4, 5}
```

---

**08. Step 6 – Set Methods**

```python
s = {1, 2, 3}

s.add(4)         # Add element
s.remove(2)      # Remove element
s.discard(5)     # Remove without error if not found
print(s)

s.clear()        # Remove all
print(s)         # set()
```

---

**09. Step 7 – Type Conversion (Casting)**

Convert between lists, sets, and tuples easily.

```python
text = "banana"
print(set(text))     # {'b', 'a', 'n'} (duplicates removed)

numbers = [1, 2, 2, 3, 4]
unique = set(numbers)
print(list(unique))  # [1, 2, 3, 4]
```

---

**10. Step 8 – Practice Examples**

**Example 1: Tuple Iteration**

```python
colors = ("red", "green", "blue")
for c in colors:
    print(c)
```

**Example 2: Set Addition**

```python
my_set = {1, 2, 3}
my_set.add(2)
my_set.add(4)
print(my_set)   # {1, 2, 3, 4}
```

**Example 3: Remove Duplicates**

```python
nums = [1, 2, 2, 3, 3, 3, 4]
unique_nums = list(set(nums))
print(unique_nums)   # [1, 2, 3, 4]
```

---

**11. Step 9 – Mini Project: Unique Data Manager**

Create a program that takes user input and removes duplicates automatically.

```python
data = input("Enter items separated by spaces: ").split()
unique_data = set(data)

print("Original:", data)
print("Unique:", list(unique_data))
```

---

**12. Reflection**

You have learned how to:

* Store ordered, unchangeable data with **tuples**
* Handle unique, unordered data with **sets**
* Perform set operations (union, intersection, etc.)
* Build a **Unique Data Manager** to clean duplicated input
