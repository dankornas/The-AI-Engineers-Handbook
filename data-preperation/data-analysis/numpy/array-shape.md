# Array Shape

Array shape is an important concept in NumPy, as it refers to the dimensions of an array. The shape of an array is defined by the number of elements in each dimension.

To get the shape of an array, you can use the `shape` attribute:

```python
import numpy as np

# Create a 2-dimensional array of integers
arr = np.array([[1, 2, 3], [4, 5, 6]])

# Get the shape of the array
print(arr.shape) # Output: (2, 3)
```

In this example, we create a 2-dimensional array of integers and use the `shape` attribute to get its shape. The output shows that the array has 2 rows and 3 columns.
