---
title: Python Course – Full Notes
tags:
  - python
  - foundation
  - learning
  - coding
created: 2026-04-27
updated: 2026-04-27
---

---

# 🐍 Python Course – Full Notes Template

> [!info] About This Note
> This is a comprehensive template for organizing Python course notes. 
> Sections are structured based on standard course syllabi and fundamental concepts. .

---

# 0. Introduction  

> [!summary] What is Python?
> Python is a high-level, readable, multi-purpose programming language that is excellent for beginners and professionals alike.

**Why Python?**
- High readability and clean syntax.
- Massive ecosystem of libraries.
- Versatile: Web Development, Data Science, AI, and Automation.

---

# 1. Setup & Installation  

## Setup 
- Install [Python](https://www.python.org/downloads/)
- Install [VSCode](https://code.visualstudio.com/) or PyCharm
- Install Python extensions for your IDE
- Run your first `Hello World` program

> [!tip] Verification
> Always check your installed version using the terminal:
> ```bash
> python --version
> ```

---

# 2. Basic Data Structures

> [!note] Foundation Note
> Everything in Python is an object. Below are the core data types. 

## 2.1 Variables & Basic Types
```python
device_name = "Laptop"    # str
device_price = 1200.50    # float
quantity = 5              # int
is_available = True       # bool
```

---

## 2.2 Strings

```python
text = "Python Programming"
```

---

### 2.2.1 What is a String?
A **string** is a sequence of characters inside quotes:

```python
name = "Dany"
message = 'Hello World'
text = "Python Programming"
```

---

### 2.2.2 Accessing Characters (Indexing)
```python
text = "Python Programming"
print(text[0])     # P
print(text[-1])    # g
```

---

### 2.2.3 Slicing Strings
```python
text = "Python Programming"
print(text[0:6])   # Python
print(text[7:])    # Programming
print(text[:6])    # Python
```

---

### 2.2.4 Changing Case
```python
text = "Python Programming"

print(text.upper())        # PYTHON PROGRAMMING
print(text.lower())        # python programming
print(text.title())        # Python Programming
print(text.capitalize())   # Python programming
```

---

### 2.2.5 Removing Spaces
```python
text = "  Python  "

print(text.strip())    # Python
print(text.lstrip())   # Python  
print(text.rstrip())   #   Python
```

---

### 2.2.6 Searching Inside String
```python
text = "Python Programming"

print(text.startswith("Python"))  # True
print(text.endswith("ing"))       # True
print(text.find("Program"))       # 7
print(text.count("m"))            # 2
```

---

### 2.2.7 Replacing Text
```python
text = "Python Programming"

print(text.replace("Python", "Java"))   # Java Programming
```

---

### 2.2.8 Splitting & Joining
```python
text = "Python Programming"

print(text.split())   # ['Python', 'Programming']

words = ["Python", "is", "fun"]
print(" ".join(words))   # Python is fun
```

---

### 2.2.9 String Formatting
```python
device_name = "Laptop"
device_price = 1200

print(f"The {device_name} costs ${device_price}")  
# The Laptop costs $1200
```

---

### 2.2.10 String Length
```python
text = "Python Programming"

print(len(text))   # 18
```
---
## 2.3 Numbers & Math
```python
print(10 + 5)   # Addition: 15
print(10 / 3)   # True Division: 3.333...
print(10 // 3)  # Floor Division: 3
print(10 ** 2)  # Exponentiation: 100
```

## 2.4 Lists (Ordered, Mutable)
```python
devices = ["Laptop", "Phone", "Tablet"]
devices.append("Monitor")   # Adds to the end
devices.insert(1, "Mouse")  # Inserts at index 1
```

## 2.5 Dictionaries (Key-Value pairs)
```python
device = {"name": "Laptop", "price": 1200}
print(device["name"])      # Access value
device["brand"] = "Apple"  # Add new key-value
```

## 2.6 Sets (Unordered, Unique elements)
```python
ids = {101, 102, 103, 101}
print(ids)  # Output: {101, 102, 103}
```

## 2.7 Tuples (Ordered, Immutable)
```python
coordinates = (45.0, 90.0)
# coordinates[0] = 50.0  # -> This will raise an error
```

---

# 3. Comparison & Logical Operators  
```python
# Comparison
print(5 > 3)      # True
print(10 == 10)   # True
print(4 != 2)     # True

# Logical
print(True and False) # False
print(True or False)  # True
print(not True)       # False
```

---

# 4. Control Flow & Loops  

## 4.1 If / Elif / Else  
```python
battery = 15

if battery > 50:
    print("Battery Good")
elif battery > 20:
    print("Battery OK")
else:
    print("Low Battery!")
```

## 4.2 For Loop  
```python
# Iterating over a list
for item in devices:
    print(item)

# Using range
for i in range(5):  # 0 to 4
    print(i)
```

## 4.3 While Loop  
```python
count = 0
while count < 3:
    print(f"Count is {count}")
    count += 1
```

---

# 5. Methods & Functions  

## 5.1 Basic Function
```python
def greet(name="Guest"):
    return f"Hello, {name}!"

print(greet("Alice"))
```

## 5.2 args & kwargs (Variable Arguments)
```python
def add_all(*args):
    return sum(args)
```

## 5.3 Lambda Functions (Anonymous)
```python
square = lambda x: x ** 2
print(square(5))  # 25
```

---

# 6. Object-Oriented Programming (OOP)

## 6.1 Classes & Objects
```python
class Device:
    # Constructor
    def __init__(self, name, price):
        self.name = name
        self.price = price

    # Method
    def get_info(self):
        return f"{self.name} costs ${self.price}"

laptop = Device("MacBook", 1500)
print(laptop.get_info())
```

## 6.2 Inheritance
```python
class Phone(Device):
    def __init__(self, name, price, os):
        super().__init__(name, price)
        self.os = os
```

---

# 7. Modules & Packages  
```python
# Built-in modules
import math
from datetime import datetime

print(math.sqrt(16))  # 4
print(datetime.now())
```

> [!tip] Best Practice  
> Keep your custom modules in the same directory and import them using `import my_module`.

---

# 8. Error Handling
```python
try:
    x = int("abc")
except ValueError as e:
    print(f"Error caught: {e}")
else:
    print("Runs if no exception occurs")
finally:
    print("Always runs (e.g., closing a file)")
```

---

# 9. Decorators  
> [!info] Concept  
> Decorators modify the behavior of a function without changing its source code.

```python
def logger(func):
    def wrapper(*args, **kwargs):
        print(f"Executing {func.__name__}...")
        return func(*args, **kwargs)
    return wrapper

@logger
def say_hi():
    print("Hi!")

say_hi()
```

---

# 10. Generators  
```python
def count_up_to(max_val):
    count = 1
    while count <= max_val:
        yield count
        count += 1

counter = count_up_to(5)
print(next(counter))  # 1
```

---

# 11. Advanced Built-in Modules  
- itertools  
- functools  
- collections  
- pathlib  

---

# 🌐 12. Web Scraping  
> [!warning] Note  
> Always check a website's robots.txt before scraping.

```python
import requests
from bs4 import BeautifulSoup

response = requests.get("https://example.com")
soup = BeautifulSoup(response.text, "html.parser")
print(soup.title.text)
```

---

# 13. Image Processing  
```python
# Requires: pip install Pillow
from PIL import Image

img = Image.open("sample.jpg")
img_resized = img.resize((300, 300))
img_resized.save("sample_small.jpg")
```

---

# 14. File & Data Handling  

## 14.1 Reading/Writing Text
```python
with open("data.txt", "w") as file:
    file.write("Hello World!")
```

## 14.2 JSON Handling
```python
import json

data = {"name": "Alice", "age": 30}

# Write to JSON
with open("data.json", "w") as f:
    json.dump(data, f)
```

---

# 🌍 15. Web Development Frameworks  
- [[FastAPI]]  
- [[Flask]]  
- [[Django]]  

---

# 🧠 16. Advanced Data Structures & Algorithms  
- Stack  
- Queue  
- Linked List  
- Tree  
- Graph  
