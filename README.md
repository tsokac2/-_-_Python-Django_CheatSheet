<h1 align="center">Python and Django</h1>

### 01. Reverse a list in Python

```
list1 = [100,200,300,400,500]
list1.list1.reverse()
print(list1)

# Solution 2: Using negative slicing

list1 = [100, 200, 300, 400, 500]
list1 = list1[::-1]
print(list1)
```

####c Expected output:

[500, 400, 300, 200, 100]



### 02. Concatenate two lists index-wise

```
# Use the zip() function. This function takes two or more iterables (like list, dict, string).
# Aggregates them in a tuple, and returns it.

list1 = ["M", "na", "i", "Ke"] 
list2 = ["y", "me", "s", "lly"]
list3 = [i + j for i, j in zip(list1, list2)]
print(list3)
```

#### Expected output:
```
['My', 'name', 'is', 'Kelly']
```

