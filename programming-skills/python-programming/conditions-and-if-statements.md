# Conditions and If statements

Python implements the standard mathematical logical conditions:

* Equals: `a == b`
* Not Equals: `a != b`
* Less than: `a < b`
* Less than or equal to: `a <= b`
* Greater than: `a > b`
* Greater than or equal to: `a >= b`

### IF Statements

These conditions may be utilized in a variety of ways, the most frequent of which being "if statements" and loops.&#x20;

The `if` keyword is used to create a "if statement."

Python uses indentation (whitespace at the start of a line) to define scope in code. Curly-brackets are frequently used for this purpose in other computer languages.

```python
a = 33
b = 200

if b > a:
  print("b is greater than a")

### Output ### 
# True
```

### ELIF Statements

The `elif` keyword in Python means "attempt this condition if the preceding conditions were not true."

```python
a = 33
b = 33
if b > a:
  print("b is greater than a")
elif a == b:
  print("a and b are equal")
  
### Output ###
# a and b are equal
```

### ELSE Statements

Anything that isn't covered by the previous conditions is caught by the `else` keyword.

```python
a = 200
b = 33
if b > a:
  print("b is greater than a")
elif a == b:
  print("a and b are equal")
else:
  print("a is greater than b")

### Output ### 
# a is greater than b
```

You can also have an `else` without the `elif`:

```python
a = 200
b = 33
if b > a:
  print("b is greater than a")
else:
  print("b is not greater than a")

### Output ###
# b is not greater than a
```

### Using AND in IF Statements

The `and` keyword is a logical operator for combining conditional statements:

```python
a = 200
b = 33
c = 500
if a > b and c > a:
  print("Both conditions are True")
  
### Output ###
# Both conditions are True
```

### Using OR in IF Statements

The `or` keyword is a logical operator for combining conditional statements as well:

```python
a = 200
b = 33
c = 500
if a > b or a > c:
  print("At least one of the conditions is True")

### Output ###
# At least one of the conditions is True
```

### Nested IF Statements

You can have `if` statements inside `if` statements, this is called _nested_ `if` statements.

```python
x = 41

if x > 10:
  print("Above ten,")
  if x > 20:
    print("and also above 20!")
  else:
    print("but not above 20.")

### Output ###
# Above ten,
# and also above 20!
```

### PASS Statement

`If` statements cannot be empty, but if you have an `if` statement with no content, include the `pass` statement to prevent an error.

```python
a = 33
b = 200

if b > a:
  pass
  
### There is no output ###
```
