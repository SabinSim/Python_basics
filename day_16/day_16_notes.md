## **Day 16 – Advanced Functions**

**Project:** Build a “Flexible Calculator & Info App” using default parameters, *args, and **kwargs.

---

**01. Learning Goal**

By the end of this lesson, you will be able to:

- Use **default parameters** to set optional arguments  
- Use **\*args** to accept multiple inputs  
- Use **\*\*kwargs** to handle keyword-based arguments  
- Combine all types of parameters in one function  

---

**02. Problem Scenario**

Imagine you’re developing a **utility app** that calculates values and manages user info.  
Some functions may take one, two, or even many arguments — you don’t know in advance.  
You’ll learn to make your functions **flexible** and **dynamic**.

---

**03. Step 1 – Default Parameters**

You can assign default values to parameters.  
If no argument is provided, the function uses the default.

```python
def greet(name="Guest"):
    print(f"Hello, {name}!")

greet()          # Hello, Guest!
greet("Sabin")   # Hello, Sabin!
```

---

**04. Step 2 – Variable-Length Arguments (*args)**

If you add `*` before a parameter, Python collects all extra positional arguments into a **tuple**.

```python
def add_all(*numbers):
    total = 0
    for n in numbers:
        total += n
    return total

print(add_all(1, 2, 3))        # 6
print(add_all(10, 20, 30, 40)) # 100
```

**Why use it?**
It allows you to pass **any number of arguments** to a single function.

---

**05. Step 3 – Keyword Variable Arguments (**kwargs)**

If you use `**`, Python collects all **keyword arguments** (key=value pairs) into a **dictionary**.

```python
def print_info(**kwargs):
    for key, value in kwargs.items():
        print(f"{key}: {value}")

print_info(name="Sabin", age=30, hobby="Coding")
# name: Sabin
# age: 30
# hobby: Coding
```

**Use case:** great for **user profiles**, **settings**, or **API parameters**.

---

**06. Step 4 – Mixing Parameters**

You can use all types of parameters together in one function.
Order matters → `regular` → `*args` → `**kwargs`

```python
def show_info(title, *args, **kwargs):
    print("Title:", title)
    print("Args:", args)
    print("Kwargs:", kwargs)

show_info("Student Info", "Tom", "Anna", grade="A", age=20)
# Title: Student Info
# Args: ('Tom', 'Anna')
# Kwargs: {'grade': 'A', 'age': 20}
```

---

**07. Step 5 – Practice Examples**

**Example 1: Default Parameter**

```python
def power(base, exp=2):
    return base ** exp

print(power(3))    # 9 (square)
print(power(3, 3)) # 27 (cube)
```

**Example 2: Using *args**

```python
def multiply_all(*nums):
    result = 1
    for n in nums:
        result *= n
    return result

print(multiply_all(2, 3, 4))  # 24
```

**Example 3: Using **kwargs**

```python
def introduce(**person):
    print(f"{person['name']} is {person['age']} years old.")

introduce(name="Sabin", age=30)
```

---

**08. Step 6 – Mini Project: Flexible Calculator & Info App**

Combine everything into one smart utility app.

```python
def calculate(op="add", *nums):
    if not nums:
        return "No numbers provided!"

    if op == "add":
        return sum(nums)
    elif op == "mul":
        result = 1
        for n in nums:
            result *= n
        return result
    else:
        return "Unknown operation!"

def profile(**info):
    print("=== User Profile ===")
    for k, v in info.items():
        print(f"{k.capitalize()}: {v}")

# Run examples
print("Sum:", calculate("add", 2, 4, 6, 8))
print("Product:", calculate("mul", 2, 4, 6, 8))

profile(name="Sabin", age=30, country="Switzerland", hobby="Coding")
```

---

**09. Reflection**

You have learned how to:

* Use **default parameters** to simplify function calls
* Use ***args** and ****kwargs** for flexible argument handling
* Combine them to create more powerful, reusable functions
* Build a **Flexible Calculator & Info App** that adapts to user input
