<h1 align="center">Python Functions</h1>

Python function is a code block or group of statements that perform a particular task. We use reuse functions whenever required.


This Python functions exercise aims to help Python developers to learn and practice how to define functions. Also, you will practice how to create and use the nested functions and the function arguments effectively.

#
### 01. Exercise - Create a function in Python
Write a program to create a function that takes two arguments, name and age, and print their value.
```
# demo is the function name
def demo(name, age):
    # print value
    print(name, age)

# call function
demo("Ben", 25)
```
#
### 02. Exercise - Create a function with variable length of arguments
Write a program to create function func1() to accept a variable length of arguments and print their value.

_**Note:**_ Create a function in such a way that we can pass any number of arguments to this function, and the function should process them and display each argument’s value.
```
def func1(*args):
    for i in args:
        print(i)

func1(20, 40, 60)
func1(80, 100)
```
#### Expected Output:
```
# call function with 3 arguments
func1(20, 40, 60)

# call function with 2 arguments
func1(80, 100)

# Printing values
20
40
60

# Printing values
80
100
```
#
### 03. Exercise - Return multiple values from a function
Write a program to create function calculation() such that it can accept two variables and calculate addition and subtraction.

Also, it must **return both addition and subtraction in a single return call.**
#### Given:
```
def calculation(a, b):
    # Your Code

res = calculation(40, 10)
print(res)
```

In Python, to return multiple values from a function, use a comma to separate them.
### Solution 1
```
def calculation(a, b):
    addition = a + b
    subtraction = a - b
    # return multiple values separated by comma
    return addition, subtraction

# get result in tuple format
res = calculation(40, 10)
print(res)
```
### Solution 2
```
def calculation(a, b):
    return a + b, a - b

# get result in tuple format
# unpack tuple
add, sub = calculation(40, 10)
print(add, sub)
```
#### Expected Output
```50, 30```
#
### 04. Exercise - Create a function with a default argument
Write a program to create a function ```show_employee()``` using the following conditions.

It should accept the employee’s name and salary and display both.
If the salary is missing in the function call then assign default value 9000 to salary
#### Given
```
showEmployee("Ben", 12000)
showEmployee("Jessa")
```
```
# function with default argument
def show_employee(name, salary=9000):
    print("Name:", name, "salary:", salary)

show_employee("Ben", 12000)
show_employee("Jessa")
```
#### Expected output:
```
Name: Ben salary: 12000
Name: Jessa salary: 9000
```
#
### 05. Exercise -  Create an inner function to calculate the addition in the following way
* Create an outer function that will accept two parameters, a and b
* Create an inner function inside an outer function that will calculate the addition of a and b
* At last, an outer function will add 5 into addition and return it

In Python, we can create a nested function inside a function. We can use the nested function to perform complex tasks multiple times within another function or avoid loop and code duplication.

```
# outer function
def outer_fun(a, b):
    square = a ** 2

    # inner function
    def addition(a, b):
        return a + b

    # call inner function from outer function
    add = addition(a, b)
    # add 5 to the result
    return add + 5

result = outer_fun(5, 10)
print(result)
```
#
### 06. Exercise - Create a recursive function
Write a program to create a recursive function to calculate the sum of numbers from 0 to 10.

A recursive function is a function that calls itself again and again.

```
def addition(num):
    if num:
        # call same function by reducing number by 1
        return num + addition(num - 1)
    else:
        return 0

res = addition(10)
print(res)
```
#### Expected Output:
```55```
#
### 07.Exercise - Assign a different name to function and call it through the new name
Below is the function ```display_student(name, age).``` Assign a new name show_tudent(name, age) to it and call it using the new name.

#### Given:
```
def display_student(name, age):
    print(name, age)

display_student("Emma", 26)
```
You should be able to call the same function using

```show_student(name, age)```

```
def display_student(name, age):
    print(name, age)

# call using original name
display_student("Emma", 26)

# assign new name
showStudent = display_student
# call using new name
showStudent("Emma", 26)
```
#### Expected Output:
```
Emma 26
Emma 26
```
#
### 08. Exercise - Generate a Python list of all the even numbers between 4 to 30
```
print(list(range(4, 30, 2)))
```
#### Expected Output:
```[4, 6, 8, 10, 12, 14, 16, 18, 20, 22, 24, 26, 28]```
#
### 09. Find the largest item from a given list
```
x = [4, 6, 8, 24, 12, 2]
print(max(x))
```
#### Expected Output:
```24```

























