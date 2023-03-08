# Array Indexing

### Array Indexing

Array indexing refers to the process of accessing individual elements of an array. NumPy arrays can be indexed in several ways, depending on the number of dimensions and the structure of the array.

### Accessing Array Elements

To access individual elements of an array, you can use square brackets and specify the index or indices of the element(s) you want to access. Here's an example:

```python
import numpy as np

# Create a 1-dimensional array
arr = np.array([1, 2, 3, 4, 5])

# Access individual elements
print(arr[0]) # Output: 1
print(arr[2]) # Output: 3
```

In this example, we create a 1-dimensional array with the values `[1, 2, 3, 4, 5]`. We then use indexing to access the first and third elements of the array.

### Accessing 2-D Arrays

To access elements of a 2-dimensional array, you can use indexing with two indices. The first index refers to the row, and the second index refers to the column. Here's an example:

```python
import numpy as np

# Create a 2-dimensional array
arr = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])

# Access individual elements
print(arr[0, 0]) # Output: 1
print(arr[1, 2]) # Output: 6
```

In this example, we create a 2-dimensional array with the values:

```lua
[[1 2 3]
 [4 5 6]
 [7 8 9]]
```

We then use indexing to access the first element (in the first row and first column) and the sixth element (in the second row and third column) of the array.

### Accessing 3-D Arrays

To access elements of a 3-dimensional array, you can use indexing with three indices. The first index refers to the depth, the second index refers to the row, and the third index refers to the column. Here's an example:

```python
import numpy as np

# Create a 3-dimensional array
arr = np.array([[[1, 2], [3, 4]], [[5, 6], [7, 8]]])

# Access individual elements
print(arr[0, 1, 0]) # Output: 3
print(arr[1, 0, 1]) # Output: 6
```

In this example, we create a 3-dimensional array with the values:

```lua
[[[1 2]
  [3 4]]

 [[5 6]
  [7 8]]]
```

We then use indexing to access the third element (in the first depth, second row, and first column) and the sixth element (in the second depth, first row, and second column) of the array.

### Negative Indexing

In addition to positive indices, NumPy arrays also support negative indices. Negative indices count from the end of the array, with `-1` referring to the last element, `-2` referring to the second-to-last element, and so on. Here's an example:

```python
import numpy as np

# Create a 1-dimensional array
arr = np.array([1, 2, 3, 4, 5])

# Access individual elements using negative indices
print(arr[-1]) # Output: 5
print(arr[-3]) # Output: 3
```
