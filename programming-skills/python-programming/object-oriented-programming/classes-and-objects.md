# Classes and Objects

Python is a programming language that is object oriented.

In Python, almost everything is an object with properties and methods.

A Class functions similarly to an object constructor or a "blueprint" for creating objects.

## Create a Class

To create a class, use the keyword `class`.

Create a class named MyClass, with a property named x:

```python
class MyClass:
  x = 5
```

## Create an Object

We can use the class named MyClass to create objects.

Create an object named p1, and print the value of x:

```python
p1 = MyClass()
print(p1.x)

### Output ###
# 5
```

## The **init**() Function

The examples above are classes and objects in their most basic form, and they are not particularly useful in real-world applications.

Every class has a function called **init**() that is always executed when the class is launched.

Use the **init**() function to assign values to object properties or to perform other operations required when the object is created.

Create a class named Person, use the **init**() function to assign values for name and age:

```python
class Person:
  def __init__(self, name, age):
    self.name = name
    self.age = age

p1 = Person("John", 36)

print(p1.name)
print(p1.age)

### Output ###
# John
# 36
```

## Object Methods

Objects can also contain methods. Methods in objects are functions that belong to the object.

Create a method in the Person class. Insert a function that prints a greeting, and execute it on the p1 object:

```python
class Person:
  def __init__(self, name, age):
    self.name = name
    self.age = age

  def myfunc(self):
    print("Hello my name is " + self.name)

p1 = Person("John", 36)
p1.myfunc()

### Output ###
# Hello my name is John"
```

## The `self` parameter

The self parameter refers to the current instance of the class and is used to access class variables.

It does not have to be named self; you can call it whatever you like, but it must be the first parameter of any method in the class.

Use the words mysillyobject and abc instead of self:

```python
class Person:
  def __init__(mysillyobject, name, age):
    mysillyobject.name = name
    mysillyobject.age = age

  def myfunc(abc):
    print("Hello my name is " + abc.name)

p1 = Person("John", 36)
p1.myfunc()

### Output ###
# Hello my name is John
```

## Modify object properties

You can modify properties on objects just like modifying any other python variable:

```python
p1.age = 40
```

## Delete Object Properties and Objects

You can delete properties on objects by using the `del` keyword:

```python
del p1.age # delete property
del p1 # delete object
```

## The `pass` statement

Class definitions cannot be empty, however if you have a class definition with no content for some reason, use the pass statement to avoid an error.

```python
class Person:
  pass
```
