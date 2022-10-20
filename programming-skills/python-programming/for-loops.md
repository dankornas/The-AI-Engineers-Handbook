# For Loops

A for loop is used to iterate through a sequence (that is either a list, a tuple, a dictionary, a set, or a string).

This behaves more like an iterator method in other object-oriented programming languages than the for keyword in other programming languages.

The for loop allows us to run a sequence of statements once for each item in a list, tuple, set, and so on.

### For Loops

```python
fruits = ["apple", "banana", "cherry"]
for x in fruits:
  print(x)
  
### Output ###
# apple
# banana 
# cherry
```

> The for loop does not require an indexing variable to set beforehand.

### **Break Statement**

With the break statement we can stop the loop before it has looped through all the items:

```python
fruits = ["apple", "banana", "cherry"]
for x in fruits:
  print(x)
  if x == "banana":
    break

### Output ###
# apple
# banana
```

### Continue Statement

We may use the continue statement to end the current iteration of the loop and begin the next:

```python
fruits = ["apple", "banana", "cherry"]
for x in fruits:
  if x == "banana":
    continue
  print(x)

### Output ###
# apple
# cherry
```

### Using `range()` to loop a certain amount of times

The range() function can be used to cycle through a set of code a specified number of times.&#x20;

The range() function returns a sequence of numbers that starts at 0 and advances by 1 (by default) until it reaches a specified value.

```python
for x in range(6):
  print(x)
  
### Output ###
# 0
# 1
# 2
# 3
# 4
# 5
```

> **Note that range(6) is not the values of 0 to 6, but the values 0 to 5.**

### Else in For Loops

The `else` keyword in a `for` loop specifies a block of code to be executed when the loop is finished:

```python
for x in range(6):
  print(x)
else:
  print("Finally finished!")
  
### Output ###
# 0
# 1
# 2
# 3
# 4
# 5
# Finally finished!
```

### Nested Loops

A nested loop is a loop that is contained within another loop.

For each iteration of the "outer loop," the "inner loop" will be run once:

```python
adj = ["red", "big", "tasty"]
fruits = ["apple", "banana", "cherry"]

for x in adj:
  for y in fruits:
    print(x, y)
    
### Output ###
# red apple
# red banana
# red cherry
# big apple
# big banana
# big cherry
# tasty apple
# tasty banana
# tasty cherry
```

### Pass Statement

`for` loops cannot be empty, but if you have a for loop with no content, use the `pass` statement to prevent an error.

```python
for x in [0, 1, 2]:
  pass
  
### No Output ###
```
