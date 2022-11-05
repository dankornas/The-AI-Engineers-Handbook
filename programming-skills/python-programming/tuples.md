# Tuples

A tuple in Python is similar to a list. It is also an ordered collection of items.

The only difference between the two is that lists are mutable (elements of a list can be changed), whereas tuples are immutable (elements of a tuple cannot be changed).

Tuple items are ordered, unchangeable, and allow duplicate values.

To create a tuple, we need to wrap items inside parentheses () and separate items by a comma.

## Creating a tuple

```python
numbers = (21, -5, 6, 9)
print(numbers)

### Output ###
# (21, -5, 6, 9)
```

## Tuple length

```python
a = ('abc', 67, True, 3.14, "female")
print(len(a))

### Output ###
# 5
```

## A tuple with different data types

```python
a = ('abc', 67, True, 3.14, "female")
print(a)
### Output ###
# ('abc', 67, True, 3.14, 'female')
```

## Using tuple() constructor to create a tuple

```python
tuple_cons = tuple(("hello","World","Beautiful","Day"))
print(tuple_cons)

### Output ###
# ('hello', 'World', 'Beautiful', 'Day')
```

## Creating nested tuples

```python
tuple_nest= ("hello",(8,4,6),('World'))
print(tuple_nest)

### Output ###
# ("hello",(8,4,6),('World'))
```

## Accessing elements of a tuple

```python
numbers = (1, 5, 6, 3)
print(numbers[2])

### Output ###
# 6
```

## Accessing a range of elements of a tuple

```python
numbers = (1, 5, 6, 3)
print(numbers[1:4])

### Output ###
# (5, 6, 3)
```

## Updating Tuples (by Concatenating)

```python
tup1 = (12, 34.56)
tup2 = ('abc', 'xyz')

# Following action is not valid for tuples
# tup1[0] = 100

# Instead, you have to create a new tuple to update it
tup3 = tup1 + tup2
print tup3

### Output ###
# (12, 34.56, 'abc', 'xyz')
```

## Repetition

```python
tup1 = (12, 34.56);
print(tup1*3)

### Output ###
#  (12, 34.56, 12, 34.56, 12, 34.56)
```

## Check if an item exists in a list

```python
tup1 = ("sunday","monday","tuesday","wednesday","thursday");
print('tuesday' in tup1)

### Output ###
# True
```
