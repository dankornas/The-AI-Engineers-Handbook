# Operators

Operators are the constructs which can manipulate the value of operands.

Consider the expression 4 + 5 = 9. Here, 4 and 5 are called operands and + is called operator.

Python language supports the following types of operators:

### Arithmetic Operators

<pre class="language-python"><code class="lang-python">x=10
y=4

#Addition
print("Addition:",x+y)

#Subtraction
print("Subtraction:",x-y)

#Multiply
print("Multiply: ",x*y)

#Division
print("Division:",x/y)

#Modulus
print("Modulus:",x%y)

#Floor Division
print("Floor Division:",x//y)

#Exponent
print("Exponent:",x**y)

### Output ###
# Addition: 14
# Subtraction: 6
# Multiply:  40
# Division: 2.5
# Modulus: 2
# Floor Division: 2
<strong># Exponent: 10000</strong></code></pre>

### Comparison Operators

```python
# Result is either True or False

x=5
y=3

#Greater than
print("Greater than:",x>y)

#Less than
print("Less than:",x<y)

#Greater than equal to 
print("Greater than equal to:",x>=y)

#less than equal to
print("Less than equal to:",x<=y)

#Not equal to 
print("Not equal to:",x!=y)

#Equal to
print("Equal to:",x==y)

### Output ###
# Greater than: True
# Greater than: False
# Greater than equal to: True
# Less than: False
# Not equal to: True
# Equal to: False
```

### Logical Operators

```python
# and, or, not [Result is either True or False]

x= True
y= False

#And
print("And result:",(x and y))

#Or
print("Or result:",(x or y))

#Not
print("Not result:",(not y))

### Output ###
# And result: False
# Or result: True
# Not result: True
```

### Bitwise Operators

```python
x = 1001
y = 1010

#And
print("And result:",(x & y))

#Or
print("Or result:",(x | y))

#Not
print("Not result:",(~y))

#Xor
print("XOR result:",(x^y))

#Bitwise right shift
print("Bitwise right shift result:",(x>>2))

#Bitwise left shift
print("Bitwise left shift result:",(x<<2))

### Output ###
# And result: 992
# Or result: 1019
# Not result: -1011
# XOR result: 27
# Bitwise right shift result: 250
# Bitwise left shift result: 4004
```

### Membership Operators

```python
# used in Python to assign values to variables
x = 'Python Course'
print('y' in x)
print('a' in x)

### Output ###
# True
# False
```

### Identity Operators

```python
# is and is not are the identity operators in Python
x=5
y=5
z='a'
print("Is - operator result:", (x is y))
print("Is Not - operator result:", (y is not z))

### Output ###
# Is operator result: True
# Not is operator result: True
```
