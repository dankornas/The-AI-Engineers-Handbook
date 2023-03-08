# Creating Arrays

***

## Creating a NumPy ndarray Object

NumPy provides support for multi-dimensional arrays and matrices through the `ndarray` object. To create a NumPy ndarray object, you can use various functions provided by NumPy. Here are some ways to create a NumPy ndarray object:

### Using the `np.array()`&#x20;

The `np.array()` function is the most basic way to create a NumPy ndarray object. It takes a sequence-like object (such as a list or tuple) as input and returns a new ndarray object. Here's an example:

```python
import numpy as np

# Create a NumPy ndarray object from a list
arr = np.array([1, 2, 3, 4, 5])

# Print the array
print(arr)
```

This creates a NumPy ndarray object from a list of integers and assigns it to the variable `arr`. We then print the contents of the array using the `print()` function.

### Using the `np.zeros()`&#x20;

The `np.zeros()` function creates a NumPy ndarray object filled with zeros. It takes a shape tuple as input, which specifies the dimensions of the array. Here's an example:

```python
import numpy as np

# Create a 2D NumPy ndarray object filled with zeros
arr = np.zeros((3, 4))

# Print the array
print(arr)
```

This creates a 2D NumPy ndarray object with 3 rows and 4 columns, filled with zeros. We then print the contents of the array using the `print()` function.

### Using the `np.ones()`&#x20;

The `np.ones()` function creates a NumPy ndarray object filled with ones. It takes a shape tuple as input, which specifies the dimensions of the array. Here's an example:

```python
import numpy as np

# Create a 3D NumPy ndarray object filled with ones
arr = np.ones((2, 3, 4))

# Print the array
print(arr)
```

This creates a 3D NumPy ndarray object with 2 layers, 3 rows, and 4 columns, filled with ones. We then print the contents of the array using the `print()` function.

### Using the `np.arange()`&#x20;

The `np.arange()` function creates a NumPy ndarray object containing evenly spaced values within a given range. It takes the start, stop, and step values as input. Here's an example:

```python
import numpy as np

# Create a NumPy ndarray object containing values from 0 to 9
arr = np.arange(10)

# Print the array
print(arr)
```

This creates a NumPy ndarray object with values from 0 to 9. We then print the contents of the array using the `print()` function.

### Using the `np.random.rand()`

The `np.random.rand()` function creates a NumPy ndarray object filled with random values between 0 and 1. It takes the shape tuple as input, which specifies the dimensions of the array. Here's an example:

```python
import numpy as np

# Create a 2D NumPy ndarray object filled with random values
arr = np.random.rand(3, 4)

# Print the array
print(arr)
```

This creates a 2D NumPy ndarray object with 3 rows and 4 columns, filled with random values between 0 and 1. We then print the contents of the array using the `print()` function.

These are just a few examples of how to create NumPy ndarray objects. NumPy provides a wide range of functions tocreate NumPy ndarrays with different shapes and data types, as well as operations to manipulate and modify them.

### Using the `np.eye()`&#x20;

The `np.eye()` function creates a NumPy ndarray object with ones on the diagonal and zeros elsewhere. It takes the number of rows as input and returns a square matrix. Here's an example:

```python
import numpy as np

# Create a square NumPy ndarray object with ones on the diagonal
arr = np.eye(5)

# Print the array
print(arr)
```

This creates a square NumPy ndarray object with 5 rows and 5 columns, with ones on the diagonal and zeros elsewhere. We then print the contents of the array using the `print()` function.

### Using the `np.linspace()`&#x20;

The `np.linspace()` function creates a NumPy ndarray object containing evenly spaced values within a given interval. It takes the start, stop, and number of values as input. Here's an example:

```python
import numpy as np

# Create a NumPy ndarray object containing 5 evenly spaced values between 0 and 1
arr = np.linspace(0, 1, 5)

# Print the array
print(arr)
```

This creates a NumPy ndarray object with 5 values evenly spaced between 0 and 1. We then print the contents of the array using the `print()` function.

### Using the `np.full()`&#x20;

The `np.full()` function creates a NumPy ndarray object filled with a specified value. It takes the shape tuple and the value as input. Here's an example:

```python
import numpy as np

# Create a NumPy ndarray object filled with the value 5.0
arr = np.full((2, 3), 5.0)

# Print the array
print(arr)
```

This creates a NumPy ndarray object with 2 rows and 3 columns, filled with the value 5.0. We then print the contents of the array using the `print()` function.

### Using the `np.reshape()`&#x20;

The `np.reshape()` function allows you to reshape an existing NumPy ndarray object to a new shape. It takes the existing ndarray object and the new shape as input. Here's an example:

```python
import numpy as np

# Create a NumPy ndarray object with values from 0 to 11
arr = np.arange(12)

# Reshape the ndarray object to a 3x4 matrix
arr = arr.reshape((3, 4))

# Print the array
print(arr)
```

This creates a NumPy ndarray object with values from 0 to 11 and reshapes it into a 3x4 matrix. We then print the contents of the array using the `print()` function.

These are just a few examples of how to create and manipulate NumPy ndarray objects. NumPy provides many more functions for creating, manipulating, and performing operations on ndarrays. With the right knowledge, you can efficiently work with large arrays and matrices in Python using NumPy.

***

## Dimensions in Arrays

NumPy arrays can have any number of dimensions, from 0 to N. The number of dimensions is also known as the rank of the array. In this section, we'll cover the basics of working with arrays of different dimensions, including 0, 1, 2, 3, and 4-dimensional arrays.

### 0-Dimensional Arrays

A 0-dimensional array, also known as a scalar, contains only one element. You can create a 0-dimensional array by passing a single value to the `np.array()` function. Here's an example:

```python
import numpy as np

# Create a 0-dimensional array
arr = np.array(42)

# Print the array
print(arr)
```

This creates a 0-dimensional array with the value 42. We then print the contents of the array using the `print()` function.

### 1-Dimensional Arrays

A 1-dimensional array, also known as a vector, contains a sequence of elements. You can create a 1-dimensional array by passing a list of values to the `np.array()` function. Here's an example:

```python
import numpy as np

# Create a 1-dimensional array
arr = np.array([1, 2, 3, 4, 5])

# Print the array
print(arr)
```

This creates a 1-dimensional array with the values 1, 2, 3, 4, and 5. We then print the contents of the array using the `print()` function.

### 2-Dimensional Arrays

A 2-dimensional array, also known as a matrix, contains a sequence of vectors. You can create a 2-dimensional array by passing a list of lists to the `np.array()` function. Here's an example:

```python
import numpy as np

# Create a 2-dimensional array
arr = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])

# Print the array
print(arr)
```

This creates a 2-dimensional array with the values:

```lua
[[1 2 3]
 [4 5 6]
 [7 8 9]]
```

We then print the contents of the array using the `print()` function.

### 3-Dimensional Arrays

A 3-dimensional array contains a sequence of matrices. You can create a 3-dimensional array by passing a list of 2-dimensional arrays to the `np.array()` function. Here's an example:

```python
import numpy as np

# Create a 3-dimensional array
arr = np.array([[[1, 2], [3, 4]], [[5, 6], [7, 8]]])

# Print the array
print(arr)
```

This creates a 3-dimensional array with the values:

```lua
[[[1 2]
  [3 4]]

 [[5 6]
  [7 8]]]
```

We then print the contents of the array using the `print()` function.

### 4-Dimensional Arrays

A 4-dimensional array contains a sequence of 3-dimensional arrays. You can create a 4-dimensional array by passing a list of 3-dimensional arrays to the `np.array()` function. Here's an example:

```python
pythonCopy codeimport numpy as np

# Create a 4-dimensional array
arr = np.array([[[[1, 2], [3, 4]], [[5, 6], [7, 8]]], [[[9, 10], [11, 12]], [[13, 14], [15, 16]]]])

# Print the array
print(arr)
```

This creates a 4-dimensional array with the values:

```lua
[[[[ 1  2]
   [ 3  4]]

  [[ 5  6]
   [ 7  8]]]


 [[[ 9 10]
   [11 12]]

  [[13 14]
   [15 16]]]]
```

We then print the contents of the array using the `print()` function.
