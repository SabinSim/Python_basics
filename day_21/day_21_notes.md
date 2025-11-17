## **Day 21 – External Libraries (pip, requests)**

**Project:** Build a “Simple API Client” that fetches and sends data using the `requests` library.

---

**01. Learning Goal**

By the end of this lesson, you will be able to:

- Install external libraries using **pip**  
- Understand how to use the `requests` module  
- Send **GET** and **POST** HTTP requests  
- Handle API responses and errors gracefully  

---

**02. Problem Scenario**

Python’s built-in modules are powerful, but sometimes you need more advanced tools — for example, when connecting to web APIs.  
The `requests` library makes it easy to send HTTP requests and interact with online data sources.

---

**03. Step 1 – pip: Python Package Installer**

`pip` is Python’s package management tool for installing and managing third-party libraries.

```bash
# Install a package
pip install requests

# Install a specific version
pip install requests==2.31.0

# Upgrade a package
pip install --upgrade requests

# List installed packages
pip list
```

After installation, you can import and use the library in your project.

---

**04. Step 2 – The requests Module**

The `requests` module allows you to easily send **HTTP requests** such as `GET`, `POST`, `PUT`, and `DELETE`.

---

**05. Step 3 – GET Request (Fetching Data)**

Use `GET` to retrieve information from an API.

```python
import requests

res = requests.get("https://jsonplaceholder.typicode.com/todos/1")

print("Status Code:", res.status_code)
print("Text:", res.text)

data = res.json()
print("JSON:", data)
print("Title:", data["title"])
```

---

**06. Step 4 – POST Request (Sending Data)**

Use `POST` to send new data to a server.

```python
import requests

payload = {"title": "Buy milk", "completed": False}
res = requests.post("https://jsonplaceholder.typicode.com/todos", json=payload)

print("Status Code:", res.status_code)
print("Response JSON:", res.json())
```

---

**07. Step 5 – Error Handling**

Always handle exceptions when working with external APIs to prevent crashes.

```python
import requests

try:
    res = requests.get("https://jsonplaceholder.typicode.com/todos/1", timeout=5)
    res.raise_for_status()  # Raises an error if response status is 4xx or 5xx
    print(res.json())
except requests.exceptions.RequestException as e:
    print("Error occurred:", e)
```

---

**08. Step 6 – Practice Examples**

**Example 1: GitHub API – Get User Info**

```python
import requests

url = "https://api.github.com/users/octocat"
res = requests.get(url)
data = res.json()

print("Name:", data["name"])
print("Public Repos:", data["public_repos"])
```

---

**Example 2: Weather API – Get Weather Data**

To use most APIs, you’ll need an API key.
Here’s how you could use the OpenWeatherMap API:

```python
import requests

city = "London"
api_key = "YOUR_API_KEY"
url = f"http://api.openweathermap.org/data/2.5/weather?q={city}&appid={api_key}"

res = requests.get(url)
print(res.json())
```

---

**09. Step 7 – Mini Project: Simple API Client**

Let’s build a small app that fetches user data and posts new content.

```python
import requests

def get_user(user_id):
    res = requests.get(f"https://jsonplaceholder.typicode.com/users/{user_id}")
    if res.status_code == 200:
        return res.json()
    return None

def create_post(title, body, user_id):
    payload = {"title": title, "body": body, "userId": user_id}
    res = requests.post("https://jsonplaceholder.typicode.com/posts", json=payload)
    return res.json()

user = get_user(1)
print("User:", user["name"])

post = create_post("My first API post", "Learning requests in Python!", user["id"])
print("New Post Created:", post)
```

Output example:

```
User: Leanne Graham
New Post Created: {'title': 'My first API post', 'body': 'Learning requests in Python!', 'userId': 1, 'id': 101}
```

---

**10. Reflection**

You have learned how to:

* Use **pip** to install third-party Python packages
* Send and handle **GET** and **POST** HTTP requests using `requests`
* Work with **JSON** API responses
* Handle exceptions safely during API communication
* Build a **Simple API Client** that interacts with real-world APIs
