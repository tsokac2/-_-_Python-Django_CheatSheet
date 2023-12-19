<h1 align="center">Common Python Interview Questions</h1>

## Basic Python Knowledge

### Differences between Python 2 and Python 3:
Python 2 reached its end of life, and Python 3 is the current version with improved syntax and features. Some differences include print statements, Unicode support, and integer division.


### Generators in Python:
Generators are functions that ``yield`` a sequence of values, allowing iteration. They differ from lists as they generate values on-the-fly, saving memory. 

``yield`` is used to produce values during iteration.

## API Concepts:

### API Importance:
APIs (Application Programming Interfaces) enable communication between different software components. They define how software components should interact.

### REST vs. SOAP APIs:
REST (Representational State Transfer) is lightweight and uses standard HTTP methods, while SOAP (Simple Object Access Protocol) is a protocol with XML-based messaging. 

REST is preferred for its simplicity.

### OAuth:
- OAuth is an authentication protocol that allows secure authorization to access resources. 
- It's widely used in API integrations for user authentication without sharing credentials.

## Python for API Integration

### Making HTTP Requests:
Python provides libraries like ``requests`` for making HTTP requests. 
For instance, ``requests.get('https://api.example.com/data')``.

### requests Library:
The ``requests`` library simplifies HTTP requests. Methods like ``get``, ``post``, and ``json()`` facilitate data retrieval and processing.

``json Module``:
The json module in Python handles JSON encoding and decoding. ``json.loads()`` is used to parse JSON data.

## Error Handling:

### Handling Exceptions in Python:
Exceptions in Python are handled using try, except, and optionally finally blocks. 

#### Example:
```
try:
    # Code that may raise an exception
except SomeException as e:
    # Handle the exception
```

### Handling Errors in API Integrations:
Robust error handling in API integrations involves checking ``HTTP`` status codes, handling timeouts, and logging errors for analysis.


## Data Formats:

### JSON vs. XML:
``JSON (JavaScript Object Notation)`` is lightweight and easier to read, while ``XML (eXtensible Markup Language)`` is more verbose. JSON is commonly preferred for its simplicity.

### Parsing JSON in Python:
The json module is used to parse JSON data. 

#### Example:
```
import json
data = '{"name": "John", "age": 30}'
parsed_data = json.loads(data)
```

#

### What is Python?
Python is a high-level, general-purpose programming language that is known for its readability and ease of use. 
It is often used for web development, data science, machine learning, and scripting.

### What are the key features of Python?
- Python is a dynamically typed language, which means that variable types are not explicitly declared. 
- Python is also garbage-collected, which means that the programmer does not need to manage memory allocation and deallocation.
- Python is further characterized by its ``object-oriented programming (OOP)`` paradigm, its extensive standard library, and its large community of active developers.

### What are the applications of Python?
Python is a versatile language with a wide range of applications. It is commonly used for:

- ``Web development``: Django, Flask
- ``Data science``: NumPy, Pandas, Matplotlib
- ``Machine learning``: TensorFlow, PyTorch, Scikit-learn
- ``Scripting``: automating tasks and automating repetitive tasks

### What is a dynamically typed language?
A dynamically typed language is a programming language in which variable types are not explicitly declared.

### Differentiate between classes, objects, and instances in Python?

- A ``class`` is a blueprint for creating ``objects``, which are instances of the class. 
- An ``instance`` is an object that has been created from a ``class``.

### Explain the concept of encapsulation in OOP?
- ``Encapsulation`` is the practice of bundling data and functions that operate on that data ``together as a unit``. 
- This helps to protect data from being accessed or modified in an unauthorized way.

### What is polymorphism in OOP?
- ``Polymorphism`` is the ability of an object to take on ``many forms``. 
- This means that objects of different classes can respond to the same message in different ways.

### Differentiate between lists, tuples, and dictionaries in Python?
- ``Lists`` are ordered collections of items. 
- ``Tuples`` are immutable ordered collections of items. 
- ``Dictionaries`` are unordered collections of ``key-value pairs``.

### What is recursion in programming?
- ``Recursion`` is a programming technique in which a ``function calls itself``. 
- This can be used to solve problems that ``involve self-similar structures``.

### Explain the difference between list and tuple?
- ``lists`` are mutable (can be changed).
- ``tuples`` are immutable (cannot be changed). 

### How do you debug Python code?
There are a number of tools and techniques for debugging Python code. These include using the ``print()`` statement, using a ``debugger``, and using ``linting tools``.

### What are the different ways to package and distribute Python code?
There are a number of different ways to package and distribute Python code. These include using the ``setuptools`` package, using the ``wheel`` package, 
and using a containerization platform such as ``Docker``.

#### Example:
```
# List
my_list = [1, 2, 3]
my_list.append(4)

print(my_list)

# Tuple
my_tuple = (1, 2, 3)
my_tuple.append(4)
print(my_tuple) #AttributeError: 'tuple' object has no attribute 'append'
```

### Explain the concept of list comprehensions?
List comprehensions provide a concise way to create lists. 
#### Example:

```
# Without list comprehension
squares = []
for i in range(5):
    squares.append(i**2)

# With list comprehension
squares = [i**2 for i in range(5)]
```

### What is the purpose of the __init__ method in Python classes?
The ``__init__`` method is a ``constructor`` in Python classes. It is called when an object is created, allowing you to initialize attributes. 
#### Example:
```
class MyClass:
    def __init__(self, x):
        self.x = x

obj = MyClass(5)
```

### What is the purpose of the if __name__ == "__main__": statement?
This statement is used to check whether the Python script is being run as the main program or 
if it is being imported as a module. Code within this block will only run if the script is the main program.
```
if __name__ == "__main__":
    # Code here will only run if the script is the main program
```

### 