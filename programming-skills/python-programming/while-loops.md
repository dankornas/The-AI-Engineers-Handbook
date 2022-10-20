# While Loops

Python loops are used to repeat a block of code a certain amount of times.&#x20;

Python has two primitive loop commands:

* `while` loops
* `for` loops

### While Loops

We can use the while loop to run a series of statements as long as a condition is true.

```python
i = 1
while i < 6:
  print(i)
  i += 1

### Output ###
# 1
# 2
# 3
# 4
# 5
```

> **Remember to increment i, or else the loop will continue forever.**

### Break Statement

You can use the `break` statement to stop a loop from continuing to iterate, even if the while condition is true:

```python
i = 1
while i < 6:
  print(i)
  if i == 3:
    break
  i += 1
  
### Output ###
# 1
# 2
# 3
```

### Continue Statement

Using the `continue` statement, you can stop the current iteration and skip to the next iteration of the loop:

```python
i = 0
while i < 6:
  i += 1
  if i == 3:
    continue
  print(i)

### Output ###
# 1
# 2
# 4
# 5
```

### Else Statement

You can use the `else` statement to run a block of code after the loop condition is no longer true:

```python
i = 1
while i < 6:
  print(i)
  i += 1
else:
  print("i is no longer less than 6")
  
### Output ###
# 1
# 2
# 3
# 4
# 5
# i is no longer less than 6
```

### For Loops
