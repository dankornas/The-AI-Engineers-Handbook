# Functions

A function is a block of code which only runs when it is called.

You can pass data, known as parameters, into a function.

A function can return data as a result.

### Creating a Function

In Python a function is defined using the `def` keyword:

```python
def my_function():
  print("Hello from a function")
```

### Calling a Function

```python
def my_function():
  print("Hello from a function")

my_function()

### Output ###
# Hello from a function
```

### Arguments

Functions can take information as arguments.

Arguments are included in parentheses following the function name. You can enter as many parameters as you wish, separated by a comma.

A function with one argument is shown in the following example (fname). When we call the function, we feed it a first name, which is utilized within the function to output the whole name:

```python
def my_function(fname):
  print(fname + " Refsnes")

my_function("Emil")
my_function("Tobias")
my_function("Linus")

### Output ###
# Emil Refsnes
# Tobias Refsnes
# Linus Refsnes
```
