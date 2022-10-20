# Sets

A set in Python is also similar to a list. It is also an unordered collection of items.

The only difference between the two is that lists are mutable (elements of a list can be changed), whereas sets are immutable (elements of a tuple cannot be changed).

The difference between sets and tuples is that a tuple is unordered and does not allow duplicates, while a tuple is ordered and allows duplicates

To create a set, we need to wrap items inside a bracket {} and separate items by a comma.

## Creating a set

```python
numbers = {21, -5, 6, 9}
print(numbers)

### Output ###
# {21, -5, 6, 9}
```

## Set length

```python
a = {'abc', 67, True, 3.14, "female"}
print(len(a))

### Output ###
# 5
```

## A set with different data types

```python
a = {'abc', 67, True, 3.14, "female"}
print(a)
### Output ###
# {True, 'female', 3.14, 67, 'abc'}
```

## Using set() constructor to create a set

```python
set_cons = set(("hello","World","Beautiful","Day"))
print(set_cons)

### Output ###
# {'Day', 'Beautiful', 'hello', 'World'}
```

## There cannot be nested sets

```python
set_nest= {"hello",{8,4,6},{'World'}}
print(set_nest)

### Output ###
# ---------------------------------------------------------------------------
# TypeError                                 Traceback (most recent call last)
# ----> 1 set_nest= {"hello",{8,4,6}}
#       2 print(set_nest)
# 
# TypeError: unhashable type: 'set'
```

## You cannot access a set using indexs

```python
numbers = {1, 5, 6, 3}
print(numbers[2])

### Output ###
# ---------------------------------------------------------------------------
# TypeError                                 Traceback (most recent call last)
# ----> 1 numbers[2]
# 
# TypeError: 'set' object is not subscriptable
```

## You can access a set by looping through it

```python
thisset = {"apple", "banana", "cherry"}

for x in thisset:
  print(x)

### Output ###
# banana
# cherry
# apple
```

## Updating Sets with update method

```python
thisset = {"apple", "banana", "cherry"}
tropical = {"pineapple", "mango", "papaya"}

thisset.update(tropical)

print(thisset)

### Output ###
# {'banana', 'apple', 'mango', 'pineapple', 'cherry', 'papaya'}
```

## Sets cannot be repeated

```python
set1 = {12, 34.56};
print(set1*2)

### Output ###
#  ---------------------------------------------------------------------------
# TypeError                                 Traceback (most recent call last)
# ----> 1 set1*2
#
# TypeError: unsupported operand type(s) for *: 'set' and 'int'
```

## Check if an item exists in a list

```python
set1 = {"sunday","monday","tuesday","wednesday","thursday"};
print('tuesday' in set1)

### Output ###
# True
```
