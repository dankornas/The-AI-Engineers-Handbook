# Data Types

***

### Data Types in Python

By default Python have these data types:

* `strings` - used to represent text data, the text is given under quote marks. e.g. "ABCD"
* `integer` - used to represent integer numbers. e.g. -1, -2, -3
* `float` - used to represent real numbers. e.g. 1.2, 42.42
* `boolean` - used to represent True or False.
* `complex` - used to represent complex numbers. e.g. 1.0 + 2.0j, 1.5 + 2.5j

### Data Types in NumPy

NumPy has some extra data types, and refer to data types with one character, like `i` for integers, `u` for unsigned integers etc.

Below is a list of all data types in NumPy and the characters used to represent them.

* `i` - integer
* `b` - boolean
* `u` - unsigned integer
* `f` - float
* `c` - complex float
* `m` - timedelta
* `M` - datetime
* `O` - object
* `S` - string
* `U` - unicode string
* `V` - fixed chunk of memory for other type ( void )

NumPy supports a variety of data types, including integers, floating-point numbers, and complex numbers. By default, NumPy will choose the appropriate data type based on the values in the array. You can check the data type of an array using the `dtype` attribute:

```python
import numpy as np

# Create a 1-dimensional array of integers
arr = np.array([1, 2, 3, 4, 5])
print(arr.dtype) # Output: int64

# Create a 1-dimensional array of floating-point numbers
arr = np.array([1.0, 2.0, 3.0, 4.0, 5.0])
print(arr.dtype) # Output: float64

# Create a 1-dimensional array of complex numbers
arr = np.array([1+2j, 3+4j, 5+6j])
print(arr.dtype) # Output: complex128
```

### Creating Arrays with a Defined Data Type

You can also create arrays with a specific data type using the `dtype` parameter when creating the array:

```python
import numpy as np

# Create a 1-dimensional array of integers with a specific data type
arr = np.array([1, 2, 3, 4, 5], dtype='int32')
print(arr.dtype) # Output: int32

# Create a 1-dimensional array of floating-point numbers with a specific data type
arr = np.array([1.0, 2.0, 3.0, 4.0, 5.0], dtype='float16')
print(arr.dtype) # Output: float16

# Create a 1-dimensional array of complex numbers with a specific data type
arr = np.array([1+2j, 3+4j, 5+6j], dtype='complex64')
print(arr.dtype) # Output: complex64
```

### What if a Value Cannot be Converted?

If a value cannot be converted to the specified data type, NumPy will raise a `ValueError`. For example:

```python
import numpy as np

# Try to create a 1-dimensional array of integers with a specific data type
arr = np.array([1, 2, 3, 4, 5.5], dtype='int32')
# Raises ValueError: cannot convert float NaN to integer
```

### Converting Data Types on Existing Arrays

You can also convert the data type of an existing array using the `astype()` method:

```python
import numpy as np

# Create a 1-dimensional array of integers
arr = np.array([1, 2, 3, 4, 5])

# Convert the data type of the array to float
arr = arr.astype('float32')

# Check the data type of the array
print(arr.dtype) # Output: float32
```

In this example, we create a 1-dimensional array of integers with the values `[1, 2, 3, 4, 5]`. We then convert the data type of the array to floating-point using the `astype()` method. We check the data type of the array and see that it is now `float32`.
