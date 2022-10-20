# Dictionaries

* In python, dictionary is an unordered collection of data values in which data values are stored in key:value pairs
* Created by placing sequence of elements within curly {} braces, separated by ‘ , ‘
* Values can be of any datatype and can be duplicated, whereas keys are immutable and can’t be repeated
* Can be created by the built-in function dict()
* Dictionaries are defined as objects with the data type ‘dict
* dict() constructor can be used when creating a new dict
* To access values in dict, use the keys
* Key Value format makes dictionary one of the most optimized and efficient data type in Python

## Create a dictionary

```python
#empty dictionary
dict_emp = {}
#dict with items
dict_one = {0:'sunday', 1: 'monday', 2: 'tuesday', 3: 'wednesday', 4: 'thursday'}
print(dict_one)

### Output ###
# {0: 'sunday', 1: 'monday', 2: 'tuesday', 3: 'wednesday', 4: 'thursday'}
```

## Accessing elements from a dictionary

```python
dict_one = {0:'sunday', 1: 'monday', 2: 'tuesday', 3: 'wednesday', 4: 'thursday'}
print(dict_one[1])
#get() method
print(dict_one.get(2))

### Output ###
# monday
# tuesday
```

## Length of a dictionary

```python
dict_one = {0:'sunday', 1: 'monday', 2: 'tuesday', 3: 'wednesday', 4: 'thursday'}
print(len(dict_one))

### Output ###
# 5
```

## Changing and Adding dictionary elements

```python
dict_one = {0:'sunday', 1: 'monday', 2: 'tuesday', 3: 'wednesday', 4: 'thursday'}
#change element
dict_one[2] = 'friday'
print("After changing the element", dict_one)
#Add element
dict_one[5] = 'saturday'
print("After adding the element :", dict_one)

### Output ###
# After changing the element {0: 'sunday', 1: 'monday', 2: 'friday', 3: 'wednesday', 4: 'thursday'}
# After adding the element : {0: 'sunday', 1: 'monday', 2: 'friday', 3: 'wednesday', 4: 'thursday', 5: 'saturday'}
```

## Removing elements from a dictionary

```python
dict_one = {0:'sunday', 1: 'monday', 2: 'tuesday', 3: 'wednesday', 4: 'thursday'}
print(dict_one.pop(2))
#popitem : remove an arbitrary item and return (key,value)
print(dict_one.popitem())

### Output ###
# tuesday
# (4, 'thursday')
```

## Remove all items in a dictionary

```python


### Output ###
#
```

## Create a dictionary with keys from a list

```python
subjects = {}.fromkeys(['Computer Science','Space Science','Math','English'])
print(subjects)

### Output ###
# {'Computer Science': None, 'Space Science': None, 'Math': None, 'English': None}
```

## Displays a list of a dictionary's (key, value) tuple pairs

```python
dict_one = {0:'sunday', 1: 'monday', 2: 'tuesday', 3: 'wednesday', 4: 'thursday'}
print(dict_one.items())

### Output ###
# dict_items([(0, 'sunday'), (1, 'monday'), (2, 'tuesday'), (3, 'wednesday'), (4, 'thursday')])
```

## Displays a list of all the keys in the dictionary

```python
dict_one = {0:'sunday', 1: 'monday', 2: 'tuesday', 3: 'wednesday', 4: 'thursday'}
print(dict_one.keys())

### Output ###
# dict_keys([0, 1, 2, 3, 4])
```

## Displays a list of all the values in the dictionary

```python
dict_one = {0:'sunday', 1: 'monday', 2: 'tuesday', 3: 'wednesday', 4: 'thursday'}
print(dict_one.values())

### Output ###
# dict_values(['sunday', 'monday', 'tuesday', 'wednesday', 'thursday'])
```

## Return the value of a key in a dictionary. If it is not available, insert a key with a value to the dictionary

```python
dict_one = {0:'sunday', 1: 'monday', 2: 'tuesday', 3: 'wednesday', 4: 'thursday'}
element = dict_one.setdefault(3)
print(element)

### Output ###
# wednesday

#If key not present 
element = dict_one.setdefault(6)
print("If key is not present:", dict_one.items())

### Output ###
# If key is not present: dict_items([(0, 'sunday'), (1, 'monday'), (2, 'tuesday'), (3, 'wednesday'), (4, 'thursday'), (6, None)])
```

## Nested Dictionaries

```python
people = {"subject": {0:"Maths",1:"English",3:"Science"},
          "marks": {0:42,1:36,2: 78},
          "Age": {0:12,1:34,2:19}
         }

print(people["Age"][0])

### Output ###
# 12
```

## Return a new sorted list of keys in the dictionary

```python
dict_one = {0:'sunday', 1: 'monday', 2: 'tuesday', 3: 'wednesday', 4: 'thursday'}
print(sorted(dict_one))

### Output ###
# [0, 1, 2, 3, 4]
```

## Iterate through a dictionay

```python
dict_one = {0:'sunday', 1: 'monday', 2: 'tuesday', 3: 'wednesday', 4: 'thursday'}
for i in dict_one.items():
    print(i)

### Output ###
# (0, 'sunday')
# (1, 'monday')
# (2, 'tuesday')
# (3, 'wednesday')
# (4, 'thursday')
```

## Dictionary Comprehension

```python
cubes = {x: x*x*x for x in range(10)}
print(cubes)

### Output ###
# {0: 0, 1: 1, 2: 8, 3: 27, 4: 64, 5: 125, 6: 216, 7: 343, 8: 512, 9: 729}
```

## Updates the dictionary with the elements from another dictionary object or from any other key/value pairs

```python
dict1 ={0:"zero",4:"four",5:"five"}
dict2={2:"two"}
# updates the value of key 2
dict1.update(dict2)
print(dict1)
### Output ###
# {0: 'zero', 4: 'four', 5: 'five', 2: 'two'}
```

## Check if a key is in a dictionary or not using the keyword

```python
dict_one = {0:'sunday', 1: 'monday', 2: 'tuesday', 3: 'wednesday', 4: 'thursday'}
print(0 in dict_one.keys())

### Output ###
# True
```
