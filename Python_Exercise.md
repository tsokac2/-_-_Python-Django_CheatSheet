<h1 align="center">Python Exercises</h1>

## The exercise contains 15 programs to solve.
#
### 01. Exercise - Calculate the multiplication and sum of two numbers
Given two integer numbers return their product only if the product is equal to or lower than 1000, else return their sum.
```
def multiplication_or_sum(num1, num2):
    # calculate product of two number
    product = num1 * num2
    # check if product is less then 1000
    if product <= 1000:
        return product
    else:
        # product is greater than 1000 calculate sum
        return num1 + num2

# First condition
result = multiplication_or_sum(20, 30)
print("The result is", result)

# Second condition
result = multiplication_or_sum(40, 30)
print("The result is", result)
```
|Given 1     |      
|------------|
|number1 = 20|
|number2 = 30|
#### Expected Output:
```
The result is 600
```
|Given 2     |      
|------------|
|number1 = 40|
|number2 = 30|
#### Expected Output:
```
The result is 70
```
#
### 02. Exercise - Print the sum of the current number and the previous number
Write a program to iterate the first 10 numbers and in each iteration, print the sum of the current and previous number.
```
print("Printing current and previous number and their sum in a range(10)")
previous_num = 0

# loop from 1 to 10
for i in range(1, 11):
    x_sum = previous_num + i
    print("Current Number", i, "Previous Number ", previous_num, " Sum: ", x_sum)
    # modify previous number
    # set it to the current number
    previous_num = i
```
#### Expected Output:
```
Printing current and previous number sum in a range(10)
Current Number 0 Previous Number  0  Sum:  0
Current Number 1 Previous Number  0  Sum:  1
Current Number 2 Previous Number  1  Sum:  3
Current Number 3 Previous Number  2  Sum:  5
Current Number 4 Previous Number  3  Sum:  7
Current Number 5 Previous Number  4  Sum:  9
Current Number 6 Previous Number  5  Sum:  11
Current Number 7 Previous Number  6  Sum:  13
Current Number 8 Previous Number  7  Sum:  15
Current Number 9 Previous Number  8  Sum:  17
```
#
### 03. Exercise - Print characters from a string that are present at an even index number
Write a program to accept a string from the user and display characters that are present at an even index number.

For example, ```str = "pynative"``` so you should display ‘p’, ‘n’, ‘t’, ‘v’.
```
# accept input string from a user
word = input('Enter word ')
print("Original String:", word)

# get the length of a string
size = len(word)

# iterate a each character of a string
# start: 0 to start with first character
# stop: size-1 because index starts with 0
# step: 2 to get the characters present at even index like 0, 2, 4
print("Printing only even index chars")
for i in range(0, size - 1, 2):
    print("index[", i, "]", word[i])    
```
### Expected Output:
```
Orginal String is  pynative
Printing only even index chars
p
n
t
v
```
#
### 04. Exercise - Remove first ```n``` characters from a string
Write a program to remove characters from a string starting from zero up to n and return a new string.

#### For example:

* ```remove_chars("pynative", 4)``` so output must be tive. Here we need to remove first four characters from a string.

* ```remove_chars("pynative", 2)``` so output must be native. Here we need to remove first two characters from a string.

**_Note_:** ```n``` must be less than the length of the string.
```
def remove_chars(word, n):
    print('Original string:', word)
    x = word[n:]
    return x

print("Removing characters from a string")
print(remove_chars("pynative", 4))
print(remove_chars("pynative", 2))
```
#
### 05. Check if the first and last number of a list is the same
Write a function to return True if the first and last number of a given list is same. If numbers are different then return ```False```.
```
def first_last_same(numberList):
    print("Given list:", numberList)
    
    first_num = numberList[0]
    last_num = numberList[-1]
    
    if first_num == last_num:
        return True
    else:
        return False

numbers_x = [10, 20, 30, 40, 10]
print("result is", first_last_same(numbers_x))

numbers_y = [75, 65, 35, 75, 30]
print("result is", first_last_same(numbers_y))
```

|Given|
|--------|
|numbers_x = [10, 20, 30, 40, 10]|
|numbers_y = [75, 65, 35, 75, 30]|

### Expected Output:
```
Given list: [10, 20, 30, 40, 10]
result is True

numbers_y = [75, 65, 35, 75, 30]
result is False
```
#
### 06. Exercise - Display numbers divisible by 5 from a list
Iterate the given list of numbers and print only those numbers which are divisible by 5.
```
num_list = [10, 20, 33, 46, 55]
print("Given list:", num_list)
print('Divisible by 5:')
for num in num_list:
    if num % 5 == 0:
        print(num)
```
### Expected Output:
```
Given list is  [10, 20, 33, 46, 55]
Divisible by 5
10
20
55
```
#
### 07. Exercise - Return the count of a given substring from a string
Write a program to find how many times substring “Emma” appears in the given string.
```
# Solution 1: Use the count() method

str_x = "Emma is good developer. Emma is a writer"
# use count method of a str class
cnt = str_x.count("Emma")
print(cnt)

Solution 2: Without string method

def count_emma(statement):
    print("Given String: ", statement)
    count = 0
    for i in range(len(statement) - 1):
        count += statement[i: i + 4] == 'Emma'
    return count

count = count_emma("Emma is good developer. Emma is a writer")
print("Emma appeared ", count, "times")

```
### Expected Output:
```
Emma appeared 2 times
```
#
### 08. Exercise - Print the following pattern
#### Expected Output:
```
1 
2 2 
3 3 3 
4 4 4 4 
5 5 5 5 5
```
```
for num in range(10):
    for i in range(num):
        print (num, end=" ") #print number
    # new line after each row to display pattern correctly
    print("\n")
```
#
### 09. Exercise - Check Palindrome Number
Write a program to check if the given number is a palindrome number.

A palindrome number is a number that is same after reverse. For example 545, is the palindrome numbers.
```
def palindrome(number):
    print("original number", number)
    original_num = number
    
    # reverse the given number
    reverse_num = 0
    while number > 0:
        reminder = number % 10
        reverse_num = (reverse_num * 10) + reminder
        number = number // 10

    # check numbers
    if original_num == reverse_num:
        print("Given number palindrome")
    else:
        print("Given number is not palindrome")

palindrome(121)
palindrome(125)
```

#### Expected Output:
```
original number 121
Yes. given number is palindrome number

original number 125
No. given number is not palindrome number
```
#
### 10. Exercise - Create a new list from a two list using the following condition
Given a two list of numbers, write a program to create a new list such that the new list should contain odd numbers from the first list and even numbers from the second list.

|Given list                  |
|----------------------------|
|list1 = [10, 20, 25, 30, 35]|
|list2 = [40, 45, 60, 75, 90]|
```
def merge_list(list1, list2):
    result_list = []
    
    # iterate first list
    for num in list1:
        # check if current number is odd
        if num % 2 != 0:
            # add odd number to result list
            result_list.append(num)
    
    # iterate second list
    for num in list2:
        # check if current number is even
        if num % 2 == 0:
            # add even number to result list
            result_list.append(num)
    return result_list

list1 = [10, 20, 25, 30, 35]
list2 = [40, 45, 60, 75, 90]
print("result list:", merge_list(list1, list2))
```
#### Expected Output:
```
result list: [25, 35, 40, 60, 90]
```
#
### 11. Exercise - Write a Program to extract each digit from an integer in the reverse order.
For example, If the given int is 7536, the output shall be “6 3 5 7“, with a space separating the digits.
```
# Use while loop

number = 7536
print("Given number", number)
while number > 0:
    # get the last digit
    digit = number % 10
    # remove the last digit and repeat the loop
    number = number // 10
    print(digit, end=" ")
```
#### Expected Output:
```
???
```
#
### 12. Exercise - Calculate income tax for the given income by adhering to the below rules

|Taxable Income|Rate (in %)    |
|--------------|---------------|
|First $10,000 |0              |
|Next $10,000  |10             |
|The remaining |20             |

```
income = 45000
tax_payable = 0
print("Given income", income)

if income <= 10000:
    tax_payable = 0
elif income <= 20000:
    # no tax on first 10,000
    x = income - 10000
    # 10% tax
    tax_payable = x * 10 / 100
else:
    # first 10,000
    tax_payable = 0

    # next 10,000 10% tax
    tax_payable = 10000 * 10 / 100

    # remaining 20%tax
    tax_payable += (income - 20000) * 20 / 100

print("Total tax to pay is", tax_payable)
```
#### Expected Output:
```
# For example, suppose the taxable income is 45000 the income tax payable is

10000*0% + 10000*10%  + 25000*20% = $6000.
```
#
### 13. Exercise - Print multiplication table form 1 to 10
```
for i in range(1, 11):
    for j in range(1, 11):
        print(i * j, end=" ")
    print("\t\t")
```

#### Expected Output:
```
1  2 3 4 5 6 7 8 9 10 		
2  4 6 8 10 12 14 16 18 20 		
3  6 9 12 15 18 21 24 27 30 		
4  8 12 16 20 24 28 32 36 40 		
5  10 15 20 25 30 35 40 45 50 		
6  12 18 24 30 36 42 48 54 60 		
7  14 21 28 35 42 49 56 63 70 		
8  16 24 32 40 48 56 64 72 80 		
9  18 27 36 45 54 63 72 81 90 		
10 20 30 40 50 60 70 80 90 100
```
#
### 14. Exercise - Print downward Half-Pyramid Pattern with Star (asterisk)
```
for i in range(6, 0, -1):
    for j in range(0, i - 1):
        print("*", end=' ')
    print(" ")
```
#### Expected Output:
```
* * * * *  
* * * *  
* * *  
* *  
*
```
#
### 15. Exercise - Write a function called ```exponent(base, exp)``` that returns an int value of base raises to the power of exp.

**_Note_:** here ```exp``` is a non-negative integer, and the base is an integer.

```
def exponent(base, exp):
    num = exp
    result = 1
    while num > 0:
        result = result * base
        num = num - 1
    print(base, "raises to the power of", exp, "is: ", result)

exponent(5, 4)
```
#### Expected output:
#### Case 1:
```
base = 2
exponent = 5

2 raises to the power of 5: 32 i.e. (2 *2 * 2 *2 *2 = 32)
```
#### Case 2:
```
base = 5
exponent = 4

5 raises to the power of 4 is: 625 
i.e. (5 *5 * 5 *5 = 625)
```