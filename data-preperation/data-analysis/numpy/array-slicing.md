# Array Slicing

### Array Slicing

Array slicing is the process of accessing a subset of elements from an array. In NumPy, slicing is done using the `:` operator, which allows you to specify a range of indices.

### Slicing 1-D Arrays

To slice a 1-dimensional array, you can use the `:` operator to specify the start and end indices of the slice. Here's an example:

```python
import numpy as np

# Create a 1-dimensional array
arr = np.array([1, 2, 3, 4, 5])

# Slice the array
print(arr[1:4]) # Output: [2 3 4]
```

In this example, we create a 1-dimensional array with the values `[1, 2, 3, 4, 5]`. We then use slicing to access a subset of the array containing the second, third, and fourth elements.

### Slicing 2-D Arrays

To slice a 2-dimensional array, you can use the `:` operator with two indices. The first index refers to the rows to be sliced, and the second index refers to the columns to be sliced. Here's an example:

```python
import numpy as np

# Create a 2-dimensional array
arr = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])

# Slice the array
print(arr[:2, 1:]) # Output: [[2 3] [5 6]]
```

In this example, we create a 2-dimensional array with the values:

```lua
luaCopy code[[1 2 3]
 [4 5 6]
 [7 8 9]]
```

We then use slicing to access a subset of the array containing the first two rows and the second and third columns.

### Slicing 3-D Arrays

To slice a 3-dimensional array, you can use the `:` operator with three indices. The first index refers to the depth to be sliced, the second index refers to the rows to be sliced, and the third index refers to the columns to be sliced. Here's an example:

```python
import numpy as np

# Create a 3-dimensional array
arr = np.array([[[1, 2], [3, 4]], [[5, 6], [7, 8]]])

# Slice the array
print(arr[:1, 1:, :1]) # Output: [[[3]]]
```

In this example, we create a 3-dimensional array with the values:

```lua
[[[1 2]
  [3 4]]

 [[5 6]
  [7 8]]]
```

We then use slicing to access a subset of the array containing the first depth, the second row, and the first column.

### Omitting Indices

If you omit the start index, the slice will start from the beginning of the array. If you omit the end index, the slice will go to the end of the array. Here's an example:

```python
import numpy as np

# Create a 1-dimensional array
arr = np.array([1, 2, 3, 4, 5])

# Slice the array
print(arr[2:]) # Output: [3 4 5]
print(arr[:3]) # Output: [1 2 3]
```

In this example, we create a 1-dimensional array with the values `[1, 2, 3, 4, 5]`. We then use slicing to access a subset of the array containing all elements from the third element to the end, and all elements up to the third element.
