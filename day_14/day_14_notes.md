## **Day 14 – Exception Handling (try / except)**

**Project:** Build a “Safe Calculator” that handles user input errors gracefully.

---

**01. Learning Goal**

By the end of this lesson, you will be able to:

- Understand what exceptions (errors) are in Python  
- Handle errors using `try` and `except` blocks  
- Use `else` and `finally` for structured control flow  
- Prevent your program from crashing unexpectedly  

---

**02. Problem Scenario**

When users input wrong data or when files are missing, your program crashes.  
Your goal today is to **handle exceptions** safely and ensure the app continues running smoothly.

---

**03. Step 1 – What is an Exception?**

An **exception** occurs when something goes wrong during execution.  
If not handled, it will stop the program.

```python
print(10 / 0)   # ZeroDivisionError
numbers = [1, 2, 3]
print(numbers[5])   # IndexError
```

**Examples of common errors:**

* Division by zero
* Accessing an invalid index
* File not found

---

**04. Step 2 – Basic try / except Structure**

```python
try:
    # Code that may cause an error
except:
    # Code to run if an error occurs
```

**Example:**

```python
try:
    x = int(input("Enter a number: "))
    print("You entered:", x)
except:
    print("That's not a valid number!")
```

---

**05. Step 3 – Handling Specific Exceptions**

You can handle different types of errors separately.

```python
try:
    num = int("abc")   # Raises ValueError
except ValueError:
    print("Cannot convert to integer.")
```

---

**06. Step 4 – Multiple Exception Types**

```python
try:
    a = [1, 2, 3]
    print(a[5])         # IndexError
    print(10 / 0)       # ZeroDivisionError
except IndexError:
    print("List index out of range!")
except ZeroDivisionError:
    print("Cannot divide by zero.")
```

---

**07. Step 5 – Using else and finally**

* `else`: Runs only if **no exception** occurs.
* `finally`: Always runs, even if an exception occurs.

```python
try:
    n = int(input("Enter a number: "))
except ValueError:
    print("Invalid input.")
else:
    print("Valid number:", n)
finally:
    print("Program finished.")
```

---

**08. Step 6 – Using the Exception Object**

You can capture the error message for debugging.

```python
try:
    x = 10 / 0
except Exception as e:
    print("Error occurred:", e)
```

---

**09. Step 7 – Practice Examples**

**Example 1: Prevent Division by Zero**

```python
try:
    a = int(input("Enter numerator: "))
    b = int(input("Enter denominator: "))
    print(a / b)
except ZeroDivisionError:
    print("Cannot divide by zero.")
```

**Example 2: File Handling**

```python
try:
    with open("not_exist.txt", "r", encoding="utf-8") as f:
        data = f.read()
except FileNotFoundError:
    print("File not found!")
```

---

**10. Step 8 – Mini Project: Safe Calculator**

Create a calculator that safely handles user errors (e.g., wrong input or zero division).

```python
while True:
    try:
        a = float(input("Enter first number: "))
        b = float(input("Enter second number: "))
        op = input("Enter operator (+, -, *, /): ")

        if op == "+":
            print("Result:", a + b)
        elif op == "-":
            print("Result:", a - b)
        elif op == "*":
            print("Result:", a * b)
        elif op == "/":
            print("Result:", a / b)
        else:
            print("Unknown operator!")

    except ValueError:
        print("Please enter a valid number.")
    except ZeroDivisionError:
        print("You can’t divide by zero.")
    except Exception as e:
        print("Unexpected error:", e)

    again = input("Try again? (y/n): ")
    if again.lower() != "y":
        print("Goodbye!")
        break
```

---

**11. Reflection**

You have learned how to:

* Prevent crashes with `try / except` blocks
* Handle multiple error types safely
* Use `else`, `finally`, and `Exception as e`
* Build a **Safe Calculator** that gracefully manages errors
