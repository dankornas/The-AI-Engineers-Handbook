# Inheritance

Inheritance allows us to create a class that inherits all of another class's methods and properties.

The class being inherited from is known as the parent class, sometimes known as the base class.

A child class is one that inherits from another class, often known as a derived class.

## Create a Parent Class

Because any class can be a parent class, the syntax is the same as it is for creating any other class:

```python
class Person:
  def __init__(self, fname, lname):
    self.firstname = fname
    self.lastname = lname

  def printname(self):
    print(self.firstname, self.lastname)

#Use the Person class to create an object, and then execute the printname method:

x = Person("John", "Doe")
x.printname()

### Output ###
# John Doe
```

## Create a Child Class

Send the parent class as a parameter when constructing the child class to build a class that inherits functionality from another class.

Create a class named Student, which will inherit the properties and methods from the Person class:

```python
class Student(Person):
  pass
```

Use the Student class to create an object, and then execute the printname method:

```python
x = Student("Mike", "Olsen")
x.printname()
### Output ###
# Mike Olsen
```

## Add the **init**() Function

```python
class Student(Person):
  def __init__(self, fname, lname):
    #add properties etc.
```

When you add the **init**() function, the child class will no longer inherit the parent's **init**() function.

To keep the inheritance of the parent's **init**() function, add a call to the parent's **init**() function:

```python
class Student(Person):
  def __init__(self, fname, lname):
    Person.__init__(self, fname, lname)
```

## Use the super() Function

Python also includes a super() function that will make the child class inherit all of its parent's methods and properties.

You don't have to mention the parent element's name when using the super() function; it will automatically inherit its parent's methods and properties.

```python
class Student(Person):
  def __init__(self, fname, lname):
    super().__init__(fname, lname)
```

## Add Properties

Add a property called graduationyear to the Student class:

```python
class Student(Person):
  def __init__(self, fname, lname):
    super().__init__(fname, lname)
    self.graduationyear = 2019
```

Add a year parameter, and pass the correct year when creating objects:

```python
class Student(Person):
  def __init__(self, fname, lname, year):
    super().__init__(fname, lname)
    self.graduationyear = year

x = Student("Mike", "Olsen", 2019)
```

## Add Methods

Add a method called welcome to the Student class:

```python
class Student(Person):
  def __init__(self, fname, lname, year):
    super().__init__(fname, lname)
    self.graduationyear = year

  def welcome(self):
    print("Welcome", self.firstname, self.lastname, "to the class of", self.graduationyear)
```

When you create a method in the child class with the same name as a function in the parent class, the parent method's inheritance is overridden.
