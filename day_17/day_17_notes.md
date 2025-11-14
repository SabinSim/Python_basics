## **Day 17 – Variable Scope (Local, Global, and Nonlocal)**

**Project:** Build a “Counter Tracker” app that explores how variable scopes behave.

---

**01. Learning Goal**

By the end of this lesson, you will be able to:

- Understand how **local**, **global**, and **nonlocal** variables work  
- Recognize variable visibility inside and outside functions  
- Use the `global` and `nonlocal` keywords correctly  
- Apply the **LEGB rule** to predict variable access order  

---

**02. Problem Scenario**

You are creating a small program that counts how many times a function is called.  
While doing so, you notice that some variables disappear or don’t update as expected.  
Let’s explore **scope** — the concept that controls where variables can be accessed.

---

**03. Step 1 – Local Variables**

Variables declared **inside a function** exist only during that function’s execution.

```python
def show_number():
    x = 10   # Local variable
    print("Inside function:", x)

show_number()
# print(x)   # Error! (x is not defined outside)
```

When the function ends, the local variable is **destroyed**.

---

**04. Step 2 – Global Variables**

Variables declared **outside any function** can be used anywhere in the program.

```python
y = 20   # Global variable

def print_global():
    print("Inside function:", y)

print_global()
print("Outside function:", y)
```

Global variables persist throughout the program.

---

**05. Step 3 – Modifying Global Variables**

If you want to **change** a global variable inside a function, use the `global` keyword.

```python
count = 0

def increase():
    global count
    count += 1

increase()
increase()
print(count)   # 2
```

⚠️ Avoid overusing `global`. It can make your code **hard to debug**.

---

**06. Step 4 – Local vs Global Name Conflict**

If both a local and a global variable share the same name,
the local one takes precedence **inside the function**.

```python
x = 100

def test():
    x = 50   # Local variable (shadows the global one)
    print("Inside function:", x)

test()
print("Outside function:", x)
# Inside function: 50
# Outside function: 100
```

---

**07. Step 5 – The LEGB Rule**

When Python searches for a variable, it follows this order:

| Level            | Description                           |
| ---------------- | ------------------------------------- |
| **L (Local)**    | Inside the current function           |
| **E (Enclosed)** | Inside the outer (enclosing) function |
| **G (Global)**   | Defined outside any function          |
| **B (Built-in)** | Python’s built-in names               |

```python
x = "global"

def outer():
    x = "enclosed"
    def inner():
        x = "local"
        print(x)   # local
    inner()
    print(x)       # enclosed

outer()
print(x)           # global
```

---

**08. Step 6 – The `nonlocal` Keyword**

`nonlocal` allows modification of variables in an **enclosing (outer)** function,
but **not global** ones.

```python
def outer():
    x = "enclosed"
    def inner():
        nonlocal x
        x = "changed"
        print("inner:", x)
    inner()
    print("outer:", x)

outer()
```

---

**09. Step 7 – Practice Examples**

**Example 1: Local vs Global**

```python
a = 5

def func():
    a = 10
    print("Inside function:", a)

func()
print("Outside function:", a)
```

**Example 2: Using global**

```python
counter = 0

def add():
    global counter
    counter += 1

add()
add()
print(counter)   # 2
```

**Example 3: Using nonlocal**

```python
def outer():
    msg = "Hello"
    def inner():
        nonlocal msg
        msg = "Hi"
    inner()
    print(msg)

outer()
```

---

**10. Step 8 – Mini Project: Counter Tracker App**

Build a function that counts how many times it’s been called,
using `global` and `nonlocal` concepts.

```python
count = 0

def counter_app():
    global count
    count += 1
    print(f"Function called {count} times.")

for _ in range(3):
    counter_app()
```

**Bonus – Using nonlocal (functional version)**

```python
def make_counter():
    count = 0
    def increment():
        nonlocal count
        count += 1
        print(f"Counter: {count}")
    return increment

counter = make_counter()
counter()
counter()
counter()
```

---

**11. Reflection**

You have learned how to:

* Differentiate **local**, **global**, and **nonlocal** variables
* Predict variable behavior with the **LEGB rule**
* Safely update global and enclosed variables
* Build a **Counter Tracker App** to visualize scope in action
