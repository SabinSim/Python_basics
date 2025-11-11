## **Day 12 – File Input & Output (File I/O)**

**Project:** Build a “Simple Notepad App” that writes and reads text files.

---

**01. Learning Goal**

By the end of this lesson, you will be able to:

- Open, read, and write files in Python  
- Understand file modes (`r`, `w`, `a`)  
- Use `with` statements for safe file handling  
- Build a simple note-taking program  

---

**02. Problem Scenario**

You need to save and read data from files — such as notes, logs, or user data.  
Your goal today: learn how to handle files safely and efficiently in Python.

---

**03. Step 1 – Opening Files**

```python
f = open("test.txt", "w")   # Open file for writing
f.write("Hello File!")      # Write content
f.close()                   # Close file
```

`open("filename", "mode")`

* `"w"` : Write (overwrites existing content)
* `"a"` : Append (adds new content at the end)
* `"r"` : Read

---

**04. Step 2 – Writing to Files**

```python
f = open("example.txt", "w", encoding="utf-8")
f.write("First line\n")
f.write("Second line\n")
f.close()
```

`encoding="utf-8"` prevents text corruption when working with non-English characters.

---

**05. Step 3 – Reading Files**

**Read the entire file:**

```python
f = open("example.txt", "r", encoding="utf-8")
data = f.read()
print(data)
f.close()
```

**Read line by line:**

```python
f = open("example.txt", "r", encoding="utf-8")
line1 = f.readline()
line2 = f.readline()
print(line1, line2)
f.close()
```

**Read all lines as a list:**

```python
f = open("example.txt", "r", encoding="utf-8")
lines = f.readlines()
for line in lines:
    print(line.strip())   # Remove newline
f.close()
```

---

**06. Step 4 – Using `with` (Recommended Way)**

`with` automatically closes the file, even if an error occurs.

```python
with open("example.txt", "r", encoding="utf-8") as f:
    for line in f:
        print(line.strip())
```

---

**07. Step 5 – Writing a List to a File**

```python
fruits = ["apple", "banana", "grape"]

with open("fruits.txt", "w", encoding="utf-8") as f:
    for fruit in fruits:
        f.write(fruit + "\n")
```

---

**08. Step 6 – Reading and Processing File Data**

```python
with open("fruits.txt", "r", encoding="utf-8") as f:
    fruits = f.readlines()

fruits = [f.strip() for f in fruits]  # Remove line breaks
print(fruits)   # ['apple', 'banana', 'grape']
```

---

**09. Step 7 – Practice Examples**

**Example 1: Write Notes**

```python
note = input("Enter your note: ")

with open("note.txt", "a", encoding="utf-8") as f:
    f.write(note + "\n")
```

**Example 2: Read Notes**

```python
with open("note.txt", "r", encoding="utf-8") as f:
    print(f.read())
```

---

**10. Step 8 – Mini Project: Simple Notepad App**

Create a text-based notepad that saves and reads user notes.

```python
while True:
    choice = input("1: Write note, 2: Read notes, 0: Exit → ")

    if choice == "1":
        note = input("Enter your note: ")
        with open("notes.txt", "a", encoding="utf-8") as f:
            f.write(note + "\n")
        print("Note saved!\n")

    elif choice == "2":
        with open("notes.txt", "r", encoding="utf-8") as f:
            print("\nYour Notes:")
            print(f.read())

    elif choice == "0":
        print("Exiting Notepad. Goodbye!")
        break
```

---

**11. Reflection**

You have learned how to:

* Open, read, and write files
* Use `with` statements to handle files safely
* Store and retrieve lists of data
* Build a **Simple Notepad App** to practice file I/O
