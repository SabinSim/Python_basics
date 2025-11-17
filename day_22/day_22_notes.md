## **Day 22 – OOP Basics: Class & Object**

**Project:** Build a “Student Management App” using Python classes and objects.

---

**01. Learning Goal**

By the end of this lesson, you will be able to:

- Understand the **core idea of Object-Oriented Programming (OOP)**  
- Define a **class** and create **objects (instances)**  
- Use attributes and methods effectively  
- Understand how the `__init__()` constructor works  

---

**02. Problem Scenario**

Imagine you’re building a system to manage students in a school.  
Each student has a **name**, an **age**, and the ability to **introduce themselves**.  
Instead of storing data in plain variables, you’ll group related data and actions together inside a **class**.

---

**03. Step 1 – What is OOP?**

OOP (Object-Oriented Programming) is a paradigm where you model real-world entities as **objects**.  
Each object has:

- **Attributes** → data (e.g., name, age)  
- **Methods** → behaviors or actions (e.g., introduce, study)

In Korean:  
객체지향 프로그래밍(OOP)은 현실 세계의 개체를 **객체(object)** 로 모델링하는 방식으로,  
객체는 **속성(데이터)** 과 **메서드(동작)** 를 가진다.

---

**04. Step 2 – Defining a Class**

Let’s define a simple `Student` class with attributes and methods.

```python
class Student:
    def __init__(self, name, age):  # Constructor
        self.name = name            # Attribute
        self.age = age

    def introduce(self):            # Method
        print(f"My name is {self.name}, I am {self.age} years old.")
```

---

**05. Step 3 – Creating Objects**

A **class** is just a blueprint — we create **objects (instances)** from it.

```python
s1 = Student("Sabin", 30)
s2 = Student("Anna", 22)

s1.introduce()  # My name is Sabin, I am 30 years old.
s2.introduce()  # My name is Anna, I am 22 years old.
```

---

**06. Step 4 – The `__init__()` Constructor**

The `__init__()` method runs automatically whenever an object is created.
It initializes the object’s attributes.

```python
class Car:
    def __init__(self, brand, model):
        self.brand = brand
        self.model = model

car1 = Car("Tesla", "Model 3")
print(car1.brand, car1.model)  # Tesla Model 3
```

---

**07. Step 5 – Attributes & Methods**

Attributes store data; methods define actions.

```python
class Dog:
    def __init__(self, name):
        self.name = name

    def bark(self):
        print(f"{self.name} is barking! / {self.name}가 짖고 있어요!")

d = Dog("Buddy")
print(d.name)  # Buddy
d.bark()       # Buddy is barking! / Buddy가 짖고 있어요!
```

---

**08. Step 6 – Practice Examples**

**Example 1: Book Class**

```python
class Book:
    def __init__(self, title, author):
        self.title = title
        self.author = author

    def info(self):
        print(f"'{self.title}' written by {self.author}")

b = Book("Python Basics", "Sabin")
b.info()
```

Output:

```
'Python Basics' written by Sabin
```

---

**Example 2: Calculator Class**

```python
class Calculator:
    def add(self, a, b):
        return a + b

    def sub(self, a, b):
        return a - b

calc = Calculator()
print(calc.add(10, 5))  # 15
print(calc.sub(10, 5))  # 5
```

---

**09. Step 7 – Mini Project: Student Management App**

Let’s expand our `Student` class to include a grade and a study method.

```python
class Student:
    def __init__(self, name, age, grade):
        self.name = name
        self.age = age
        self.grade = grade

    def introduce(self):
        print(f"My name is {self.name}, I’m {self.age} years old and in grade {self.grade}.")

    def study(self, subject):
        print(f"{self.name} is studying {subject}!")

s = Student("Sabin", 30, "A")
s.introduce()
s.study("Python")
```

Output:

```
My name is Sabin, I’m 30 years old and in grade A.
Sabin is studying Python!
```

---

**10. Reflection**

You have learned how to:

* Define and instantiate classes
* Use attributes and methods to represent data and behavior
* Understand how the `__init__()` constructor works
* Build your first **object-oriented program**
