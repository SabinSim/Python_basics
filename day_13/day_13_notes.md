## **Day 13 – JSON (JavaScript Object Notation)**

**Project:** Build a “User Profile Data Manager” using JSON files

---

**01. Learning Goal**

By the end of this lesson, you will be able to:

- Understand what JSON is and why it’s used  
- Convert between JSON and Python objects  
- Read from and write to JSON files  
- Manage structured data (like user profiles) with ease  

---

**02. Problem Scenario**

You’re building an application that stores and retrieves user information (name, age, skills).  
You want this data to be **readable, lightweight, and compatible** with APIs — this is where **JSON** comes in.

---

**03. Step 1 – What is JSON?**

JSON (JavaScript Object Notation) is a text-based data format used for data exchange.  
It looks similar to Python dictionaries.

```json
{
  "name": "Sabin",
  "age": 30,
  "skills": ["Python", "Flask", "React"]
}
```

**Why it matters:**
JSON is the standard format for communication between servers, databases, and APIs.

---

**04. Step 2 – Working with JSON in Python**

Python provides a built-in module `json` to handle JSON easily.

```python
import json
```

---

**05. Step 3 – Converting Between JSON and Python Objects**

**JSON → Python**

```python
import json

data = '{"name": "Sabin", "age": 30}'   # JSON string
py_obj = json.loads(data)                # Convert to dict
print(py_obj)                            # {'name': 'Sabin', 'age': 30}
print(py_obj["name"])                    # Sabin
```

**Python → JSON**

```python
person = {"name": "Sabin", "age": 30}
json_str = json.dumps(person, ensure_ascii=False)
print(json_str)   # {"name": "Sabin", "age": 30}
```

---

**06. Step 4 – Reading and Writing JSON Files**

**Write to file:**

```python
person = {"name": "Sabin", "age": 30, "skills": ["Python", "Flask"]}

with open("person.json", "w", encoding="utf-8") as f:
    json.dump(person, f, ensure_ascii=False, indent=2)
```

* `indent=2`: pretty formatting with indentation
* `ensure_ascii=False`: keeps non-English characters readable

**Read from file:**

```python
with open("person.json", "r", encoding="utf-8") as f:
    data = json.load(f)

print(data)           # {'name': 'Sabin', 'age': 30, 'skills': ['Python', 'Flask']}
print(data["skills"]) # ['Python', 'Flask']
```

---

**07. Step 5 – JSON with Lists**

You can store multiple objects inside a list.

```python
people = [
    {"name": "Tom", "age": 20},
    {"name": "Anna", "age": 22}
]

with open("people.json", "w", encoding="utf-8") as f:
    json.dump(people, f, ensure_ascii=False, indent=2)

with open("people.json", "r", encoding="utf-8") as f:
    loaded = json.load(f)

print(loaded[0]["name"])  # Tom
```

---

**08. Step 6 – Practice Examples**

**Example 1: Convert Dictionary → JSON String**

```python
book = {"title": "Python Basics", "price": 25000}
json_str = json.dumps(book, ensure_ascii=False)
print(json_str)
```

**Example 2: Convert JSON String → Dictionary**

```python
json_data = '{"title": "AI Guide", "author": "Sabin"}'
book = json.loads(json_data)
print(book["author"])
```

---

**09. Step 7 – Mini Project: User Profile Data Manager**

Create a small program to save and load user profile information using JSON.

```python
import json

profile = {
    "name": "Sabin",
    "age": 30,
    "skills": ["Python", "Flask", "React"]
}

# Save profile
with open("profile.json", "w", encoding="utf-8") as f:
    json.dump(profile, f, ensure_ascii=False, indent=2)

# Load profile
with open("profile.json", "r", encoding="utf-8") as f:
    loaded = json.load(f)

print("Loaded Profile:")
for key, value in loaded.items():
    print(f"{key}: {value}")
```

---

**10. Reflection**

You have learned how to:

* Use the `json` module for serialization and deserialization
* Convert between Python dictionaries and JSON strings
* Read and write structured data files
* Build a **User Profile Manager** that stores and loads JSON data
