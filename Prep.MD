<h1 align="center">Common Python Interview Questions</h1>

### What is Python?

Python is a high-level, general-purpose programming language that is known for its readability and ease of use. 
It is often used for web development, data science, machine learning, and scripting.

### Explain the difference between list and tuple?

- ``lists`` are mutable (can be changed).
- ``tuples`` are immutable (cannot be changed). 

Example:
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

The ``__init__`` method is a constructor in Python classes. It is called when an object is created, allowing you to initialize attributes. 

Example:

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