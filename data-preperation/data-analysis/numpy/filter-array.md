# Filter Array

In NumPy, you can filter an array based on a certain condition using boolean indexing. Boolean indexing means that you use a boolean array to index another array. The boolean array indicates which elements in the original array should be selected.

Here's an example:

```python
import numpy as np

# Create a 1-dimensional array
arr = np.array([1, 2, 3, 4, 5])

# Create a boolean array based on a condition
bool_arr = arr > 2

# Filter the original array using the boolean array
filtered_arr = arr[bool_arr]

# Print the filtered array
print(filtered_arr)
```

In this example, we create a 1-dimensional array with the values `[1, 2, 3, 4, 5]`. We then create a boolean array based on the condition that each element of the array is greater than 2. The resulting boolean array is `[False, False, True, True, True]`. Finally, we use the boolean array to filter the original array and select only the elements that satisfy the condition. The resulting filtered array is `[3, 4, 5]`.

You can also use boolean indexing to filter arrays with more than one dimension. Here's an example:

```python
import numpy as np

# Create a 2-dimensional array
arr = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])

# Create a boolean array based on a condition
bool_arr = arr > 5

# Filter the original array using the boolean array
filtered_arr = arr[bool_arr]

# Print the filtered array
print(filtered_arr)
```

In this example, we create a 2-dimensional array with the values `[[1, 2, 3], [4, 5, 6], [7, 8, 9]]`. We then create a boolean array based on the condition that each element of the array is greater than 5. The resulting boolean array is `[[False, False, False], [False, False, True], [True, True, True]]`. Finally, we use the boolean array to filter the original array and select only the elements that satisfy the condition. The resulting filtered array is `[6, 7, 8, 9]`.

You can also use boolean indexing to modify the values in an array that satisfy a certain condition. Here's an example:

```python
import numpy as np

# Create a 1-dimensional array
arr = np.array([1, 2, 3, 4, 5])

# Modify the values in the array based on a condition
arr[arr > 2] = 0

# Print the modified array
print(arr)
```

In this example, we create a 1-dimensional array with the values `[1, 2, 3, 4, 5]`. We then modify the values in the array based on the condition that each element of the array is greater than 2. The resulting modified array is `[1, 2, 0, 0, 0]`.
