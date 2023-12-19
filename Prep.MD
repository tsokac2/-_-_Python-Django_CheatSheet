<h1 align="center">Common Python Interview Questions</h1>

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
There are a number of tools and techniques for debugging Python code. These include using the print() statement, using a debugger, and using linting tools.

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