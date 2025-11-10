## **Day 10 – Dictionaries**

**Project:** Build a “Student Information System” using Dictionaries

---

**01. Learning Goal**

By the end of this lesson, you will be able to:

- Create and manipulate dictionaries (`dict`)  
- Access, update, and delete key-value pairs  
- Use dictionary methods like `.keys()`, `.values()`, and `.items()`  
- Build nested dictionaries for structured data  

---

**02. Problem Scenario**

You’re building a simple student record manager.  
Each student has attributes like name, age, and major.  
Dictionaries allow you to store and retrieve this information efficiently using key-value pairs.

---

**03. Step 1 – What is a Dictionary?**

A dictionary stores data as **key-value pairs**, enclosed in `{}`.

```python
student = {
    "name": "Sabin",
    "age": 30,
    "major": "Computer Science"
}
```

**Key Features:**

* Keys must be **immutable** (strings, numbers, or tuples).
* Values can be of **any data type**.

---

**04. Step 2 – Accessing Values**

Use keys or `.get()` to retrieve values safely.

```python
print(student["name"])   # Sabin
print(student["age"])    # 30

# Using get() (avoids KeyError)
print(student.get("major"))       # Computer Science
print(student.get("grade"))       # None
print(student.get("grade", "N/A"))  # Default value if key not found
```

---

**05. Step 3 – Updating and Adding Data**

You can modify existing keys or add new ones dynamically.

```python
student["age"] = 31       # Modify value
student["grade"] = "A"    # Add new key
print(student)
```

---

**06. Step 4 – Removing Data**

Use `del` or `.pop()` to delete data.

```python
del student["major"]      # Remove a specific key
print(student)

grade = student.pop("grade", "N/A")   # Remove and return the value
print("Removed:", grade)
```

---

**07. Step 5 – Dictionary Methods**

```python
person = {"name": "Anna", "age": 22}

print(person.keys())     # dict_keys(['name', 'age'])
print(person.values())   # dict_values(['Anna', 22])
print(person.items())    # dict_items([('name', 'Anna'), ('age', 22)])

# Loop through keys and values
for k, v in person.items():
    print(k, ":", v)
```

---

**08. Step 6 – Nested Dictionaries**

Dictionaries can contain other dictionaries — useful for structured data.

```python
students = {
    "s1": {"name": "Tom", "age": 20},
    "s2": {"name": "Anna", "age": 22}
}

print(students["s1"]["name"])   # Tom
```

---

**09. Step 7 – Practice Examples**

**Example 1: Print Student Information**

```python
student = {"name": "Sabin", "age": 30, "major": "CS"}

for k, v in student.items():
    print(f"{k}: {v}")
```

**Example 2: Manage Scores**

```python
scores = {"Korean": 90, "English": 85, "Math": 80}

print("Total:", sum(scores.values()))
print("Average:", sum(scores.values()) / len(scores))
```

---

**10. Step 8 – Mini Project: Student Information System**

Create a dictionary-based system that manages and displays student data.

```python
students = {
    "101": {"name": "Tom", "age": 20, "grade": "A"},
    "102": {"name": "Anna", "age": 22, "grade": "B"},
    "103": {"name": "Sabin", "age": 30, "grade": "A+"}
}

for sid, info in students.items():
    print(f"ID: {sid}")
    for k, v in info.items():
        print(f"  {k}: {v}")
    print()
```

---

**11. Reflection**

You have learned how to:

* Store data efficiently with **key-value pairs**
* Use dictionary methods to manage and inspect data
* Work with **nested dictionaries** for complex records
* Build a **Student Information System**
