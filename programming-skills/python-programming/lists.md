# Lists

## &#x20;Python List

* One of most adaptable data types in Python. Lists can store various different types of elements (homogeneous or non-homogeneous).
* To create a list of items, you need to use square brackets `[ ]`&#x20;
* Any items can be added to lists.
* Lists are defined as objects with the data type `‘list’`.
* Items in lists can be sorted, changed, and duplicated.
* The `link()` constructor can be used when creating a new list.
* Accessing elements within a list is done the same way as accessing characters within a string - by using indexing and slicing methods.
* Items inside a list are indexed, the first item has an index \[0], the second item has an index \[1], etc.

### Create a List

```python
list_one = ["sunday","monday","tuesday","wednesday","thursday"]
print(list_one)

### Output ###
# ['sunday', 'monday', 'tuesday', 'wednesday', 'thursday']
```

### List Length

```python
print(len(list_one))

### Output ###
# 5
```

### List with different data types

```python
list_two = ['abc', 67, True, 3.14, "female"] 
print(list_two)

### Output ###
# ['abc', 67, True, 3.14, 'female']
```

### Check the type of the list

```python
print(type(list_two))

### Output ###
# <class 'list'>
```

### Use list() constructor to create a list

```python
list_cons = list(("hello","World","Beautiful","Day"))
print(list_cons)

### Output ###
# ['hello', 'World', 'Beautiful', 'Day']
```

### Creating nested lists

```python
list_nest= ["hello",[8,4,6],['World']]
print(list_nest)

### Output ###
# ['hello', [8, 4, 6], ['World']]
```

### Slice lists in Python

```python
list_one = ["sunday","monday","tuesday","wednesday","thursday"]
print(list_one[1:4])

### Output ###
# ['monday', 'tuesday', 'wednesday']
```

### Add/Change list elements

```python
list_one = ["sunday","monday","tuesday","wednesday","thursday"]
list_one[3] = 'friday'
print(list_one)

### Output ###
# ['sunday', 'monday', 'tuesday', 'friday', 'thursday']
```

### Appending and Extending list

```python
list_one = ["sunday","monday","tuesday","wednesday","thursday"]
list_one.append('friday')
print(list_one)

### Output ###
# ['sunday', 'monday', 'tuesday', 'wednesday', 'thursday', 'friday']

list_one.extend(['saturday'])
print(list_one)

### Output ###
# ['sunday', 'monday', 'tuesday', 'wednesday', 'thursday', 'friday', 'saturday']
```

### Concatenating and repeat lists

```python
# use + operator to concate two #lists 
list_one = ["sunday","monday","tuesday","wednesday","thursday"]
print(list_one + [0,1,2,3,4])

### Output ###
# ['sunday', 'monday', 'tuesday', 'wednesday', 'thursday', 0, 1, 2, 3, 4]

# use * operator to repeat lists
print(['a','b']*2)

### Output ###
# ['a', 'b', 'a', 'b']
```

### Delete/Remove list elements

```python
# delete one or more items or the entire list using the keyword del
del list_one[2]
print(list_one)

### Output ###
# ['sunday', 'monday', 'thursday']

# remove the given item 
list_one = ["sunday","monday","tuesday","wednesday","thursday"]
list_one.remove("tuesday")
print(list_one)

### Output ###
# ['sunday', 'monday', 'wednesday', 'thursday']

# pop() method to remove an item at the given index location
list_one = ["sunday","monday","tuesday","wednesday","thursday"]
list_one.pop(2)
print("Pop result:", list_one)

### Output ###
Pop result: ['sunday', 'monday', 'wednesday', 'thursday']
```

### Getting elements in a list with index()

```python
# Returns the index of the first matched item
list_one = ["sunday","monday","tuesday","wednesday","thursday"]
print(list_one.index("tuesday"))

### Output ###
# 2
```

### Sorting elements in a list

```python
# Sort items in a list in ascending order
list_one = ["sunday","monday","tuesday","wednesday","thursday"]
list_one.sort()
print(list_one)


### Output ###
# ['monday', 'sunday', 'thursday', 'tuesday', 'wednesday']
```

### Reversing a list

```python
# Reverse the order of items in the list
list_one = ["sunday","monday","tuesday","wednesday","thursday"]
list_one.reverse()
print(list_one)

### Output ###
# ['thursday', 'wednesday', 'tuesday', 'monday', 'sunday']
```

### Copying a list

```python
# Returns a shallow copy of the list
list_one = ["sunday","monday","tuesday","wednesday","thursday"]
list_two = list_one.copy()
print(list_two)

### Output ###
# ['sunday', 'monday', 'tuesday', 'wednesday', 'thursday']
```

### Check if an item exists in a list

```python
list_one = ["sunday","monday","tuesday","wednesday","thursday"]
print('tuesday' in list_one)

### Output ###
# True
```

### Insert an item at the desired location in a list

```python
list_one = ["sunday","monday","tuesday","wednesday","thursday"]
list_one.insert(2,'friday')
print(list_one)

### Output ###
# ['sunday', 'monday', 'friday', 'tuesday', 'wednesday', 'thursday']
```



## List Comprehension

List comprehension **consists of brackets containing the expression, which is executed for each element along with the for loop to iterate over each element in the Python list**. Python List comprehension provides a much more short syntax for creating a new list based on the values of an existing list.

#### Create a list of numbers whose result is 2 to the power of a certain number, where the numbers are in a range from 1 to 20

```python
sqr = [2**x for x in range(20)]
print(sqr)

### Output ###
# [1, 2, 4, 8, 16, 32, 64, 128, 256, 512, 1024, 2048, 4096, 8192, 16384, 32768, 65536, 131072, 262144, 524288]
```

