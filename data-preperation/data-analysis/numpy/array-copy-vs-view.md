# Array Copy vs View

### Array Copy vs. View

When working with NumPy arrays, it's important to understand the difference between an array copy and an array view.

### Array Copy

An array copy is a new array object with new data that is created by copying the original array. Any changes made to the copy will not affect the original array. You can create a copy of an array using the `copy()` method:

```python
import numpy as np

# Create a 1-dimensional array of integers
arr1 = np.array([1, 2, 3, 4, 5])

# Create a copy of the array
arr2 = arr1.copy()

# Modify the copy
arr2[0] = 10

# Print both arrays
print(arr1) # Output: [1 2 3 4 5]
print(arr2) # Output: [10 2 3 4 5]
```

In this example, we create a 1-dimensional array of integers with the values `[1, 2, 3, 4, 5]`. We then create a copy of the array using the `copy()` method. We modify the copy by setting the first element to `10`, and we print both arrays. We can see that the modification only affected the copy and not the original array.

### Array View

An array view is a new array object that refers to the same data as the original array. Any changes made to the view will affect the original array. You can create a view of an array using the `view()` method:

```python
import numpy as np

# Create a 1-dimensional array of integers
arr1 = np.array([1, 2, 3, 4, 5])

# Create a view of the array
arr2 = arr1.view()

# Modify the view
arr2[0] = 10

# Print both arrays
print(arr1) # Output: [10 2 3 4 5]
print(arr2) # Output: [10 2 3 4 5]
```

In this example, we create a 1-dimensional array of integers with the values `[1, 2, 3, 4, 5]`. We then create a view of the array using the `view()` method. We modify the view by setting the first element to `10`, and we print both arrays. We can see that the modification affected both the original array and the view.

### Checking for Array Copy vs. View

You can use the `base` attribute to check if an array is a copy or a view:

```python
import numpy as np

# Create a 1-dimensional array of integers
arr1 = np.array([1, 2, 3, 4, 5])

# Create a view of the array
arr2 = arr1.view()

# Check if arr2 is a view of arr1
print(arr2.base is arr1) # Output: True

# Create a copy of the array
arr3 = arr1.copy()

# Check if arr3 is a copy of arr1
print(arr3.base is arr1) # Output: False
```

In this example, we create a view and a copy of a 1-dimensional array of integers. We use the `base` attribute to check if the view is a view of the original array, and we check if the copy is a copy of the original array. We can see that the view is a view of the original array, and the copy is not.

### Array Owns its Data

An array can either own its data or can view or reference data from another array. When an array owns its data, it means that the data is stored in a contiguous block of memory, and the array is the sole owner of that memory. If an array does not own its data, it means that it is referencing data owned by another array, and any modifications made to the array will also affect the original array.

You can use the `flags` attribute to check if an array owns its data:

```python
import numpy as np

# Create a 1-dimensional array of integers
arr1 = np.array([1, 2, 3, 4, 5])

# Create a view of the array
arr2 = arr1.view()

# Check if arr1 owns its data
print(arr1.flags.owndata) # Output: True

# Check if arr2 owns its data
print(arr2.flags.owndata) # Output: False
```

In this example, we create a view of a 1-dimensional array of integers. We use the `flags` attribute to check if the original array owns its data and if the view owns its data. We can see that the original array owns its data, and the view does not.

Knowing whether an array is a copy or a view, and whether it owns its data, can help you avoid unexpected behavior when working with NumPy arrays.
