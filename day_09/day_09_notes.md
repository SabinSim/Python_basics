## **Day 9 – Strings**

**Project:** Build a “String Analyzer” to explore and manipulate text data

---

**01. Learning Goal**

By the end of this lesson, you will be able to:

- Create and manipulate strings in Python  
- Access and slice string elements  
- Use string methods to clean and modify text  
- Analyze and extract information from text  

---

**02. Problem Scenario**

Text data is everywhere — from names and emails to user input.  
You need to process, clean, and analyze text efficiently.  
Your goal today: learn how to slice, join, search, and modify strings.

---

**03. Step 1 – What is a String?**

A string is a sequence of characters enclosed in either single `' '` or double `" "` quotes.

```python
text1 = "Hello"
text2 = 'Python'
print(text1, text2)
```

---

**04. Step 2 – Indexing and Slicing**

Like lists, strings are **ordered sequences** and support indexing.

```python
word = "Python"

print(word[0])    # P (first character)
print(word[-1])   # n (last character)
print(word[0:4])  # Pyth (from index 0 to 3)
print(word[:2])   # Py
print(word[2:])   # thon
```

---

**05. Step 3 – String Operations**

You can combine (`+`) or repeat (`*`) strings easily.

```python
a = "Hello"
b = "World"

print(a + " " + b)   # Concatenation → Hello World
print(a * 3)         # Repetition → HelloHelloHello
```

---

**06. Step 4 – Common String Methods**

Python provides many built-in methods to process strings.

```python
s = "  python programming  "

print(s.upper())      # Convert to uppercase
print(s.lower())      # Convert to lowercase
print(s.strip())      # Remove whitespace
print(s.replace("python", "java"))  # Replace text
print(s.split())      # Split by spaces → ['python', 'programming']
```

---

**07. Step 5 – String Checks**

You can check for substrings and specific patterns.

```python
msg = "Hello Python"

print("Python" in msg)    # True
print("Java" not in msg)  # True

print(msg.startswith("Hello"))  # True
print(msg.endswith("Python"))   # True
```

---

**08. Step 6 – Using f-Strings**

The `f-string` allows easy variable insertion into text.

```python
name = "Sabin"
lang = "Python"
print(f"{name} is learning {lang}.")
```

---

**09. Step 7 – Strings and Loops**

You can loop through each character in a string.

```python
for ch in "Hello":
    print(ch)
```

---

**10. Step 8 – Practice Examples**

**Example 1: Find String Length**

```python
s = "Python"
print(len(s))   # 6
```

**Example 2: Extract Username from Email**

```python
email = "sabin@test.com"
user = email.split("@")[0]
print("Username:", user)   # sabin
```

**Example 3: Reverse a String**

```python
text = "Python"
print(text[::-1])   # nohtyP
```

---

**11. Step 9 – Mini Project: String Analyzer**

Create a simple program that takes a sentence and prints key details.

```python
sentence = input("Enter a sentence: ")

print("Length:", len(sentence))
print("Uppercase:", sentence.upper())
print("Lowercase:", sentence.lower())
print("Reversed:", sentence[::-1])
print("Words:", len(sentence.split()))
```

---

**12. Reflection**

You have learned how to:

* Access, slice, and modify strings
* Clean and transform text with string methods
* Use f-strings for formatted output
* Build a **String Analyzer** that processes user input
