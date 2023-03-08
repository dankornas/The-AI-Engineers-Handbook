# Array Reshaping

### Array Reshaping

Array reshaping refers to the process of changing the shape of an existing array without changing its data. This can be useful for reorganizing data into different shapes or dimensions, which can be important for certain data processing tasks.

### **Reshaping Arrays**

You can reshape an array using the `reshape()` method, which takes in the desired shape of the new array as a tuple. For example:

```python
import numpy as np

# Create a 1-dimensional array of integers
arr = np.array([1, 2, 3, 4, 5, 6])

# Reshape the array into a 2-dimensional array with 3 rows and 2 columns
new_arr = arr.reshape((3, 2))

# Print the new array
print(new_arr)
```

This will output:

```lua
[[1 2]
 [3 4]
 [5 6]]
```

### **Reshape From 1-D to 2-D**

You can reshape a 1-dimensional array into a 2-dimensional array by specifying the number of rows and columns in the new array. For example:

```python
import numpy as np

# Create a 1-dimensional array of integers
arr = np.array([1, 2, 3, 4, 5, 6])

# Reshape the array into a 2-dimensional array with 3 rows and 2 columns
new_arr = arr.reshape((3, 2))

# Print the new array
print(new_arr)
```

This will output:

```lua
[[1 2]
 [3 4]
 [5 6]]
```

### **Reshape From 1-D to 3-D**

You can reshape a 1-dimensional array into a 3-dimensional array by specifying the number of rows, columns, and depth in the new array. For example:

```python
import numpy as np

# Create a 1-dimensional array of integers
arr = np.array([1, 2, 3, 4, 5, 6])

# Reshape the array into a 3-dimensional array with 1 depth, 2 rows, and 3 columns
new_arr = arr.reshape((1, 2, 3))

# Print the new array
print(new_arr)
```

This will output:

```lua
[[[1 2 3]
  [4 5 6]]]
```

### **Can We Reshape Into Any Shape?**

Not all arrays can be reshaped into every possible shape. The new shape must have the same number of elements as the original shape. For example, an array with 6 elements can be reshaped into a 2x3, 3x2, or 6x1 array, but it cannot be reshaped into a 3x3 array, as that would require 9 elements.

### **Returns Copy or View?**

Reshaping an array can either return a copy of the original array or a view of the original array. If the new shape has the same number of elements as the original shape, then the new array is a view of the original array. If the new shape has a different number of elements than the original shape, then the new array is a copy of the original array.

```python
import numpy as np

# Create a 2-dimensional array of integers
arr = np.array([[1, 2], [3, 4], [5, 6]])

# Reshape the array into a 1-dimensional array
new_arr = arr.reshape((6,))

# Check if the new array is a view or a copy of the original array
print(new_arr.base is arr) 
```

### Flattening an array

Flattening an array means converting a multidimensional array into a 1D array. We can use the `flatten()` method to achieve this.

```python
# Flattening an array
arr = np.array([[1, 2, 3], [4, 5, 6]])
newarr = arr.flatten()
print(newarr)
```

Output:

```csharp
[1 2 3 4 5 6]
```

Here, we first create a 2D array `arr`, and then use the `flatten()` method to convert it into a 1D array `newarr`.

Note that the `flatten()` method always returns a copy of the array, even if it is already a 1D array. If you want to modify the original array in place, you can use the `ravel()` method instead.
