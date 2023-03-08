# Splitting Array

#### Splitting Arrays

NumPy allows you to split an array into multiple sub-arrays using the `split()` function. The `split()` function takes three arguments:

* The array to be split.
* The number of equally shaped sub-arrays to be created.
* The axis along which to split the array.

Here's an example:

```python
import numpy as np

# Create a 1-dimensional array
arr = np.array([1, 2, 3, 4, 5, 6, 7, 8])

# Split the array into three sub-arrays
sub_arrays = np.split(arr, 3)

# Print the sub-arrays
for sub_arr in sub_arrays:
    print(sub_arr)
```

In this example, we create a 1-dimensional array with the values `[1, 2, 3, 4, 5, 6, 7, 8]`. We then use the `split()` function to split the array into three equally shaped sub-arrays along the first axis. The output of the code will be:

```csharp
[1 2 3]
[4 5 6]
[7 8]
```

If you want to split an array into sub-arrays of unequal size, you can pass a list of indices to the `split()` function instead of the number of sub-arrays. Here's an example:

```python
import numpy as np

# Create a 1-dimensional array
arr = np.array([1, 2, 3, 4, 5, 6, 7, 8])

# Split the array into sub-arrays of unequal size
sub_arrays = np.split(arr, [3, 5, 6])

# Print the sub-arrays
for sub_arr in sub_arrays:
    print(sub_arr)
```

In this example, we split the array into sub-arrays of sizes 3, 2, and 1, respectively. The output of the code will be:

```csharp
[1 2 3]
[4 5]
[6]
[7 8]
```

The `split()` function returns a list of sub-arrays, rather than a single array. If you want to concatenate the sub-arrays into a single array again, you can use the `concatenate()` function. Here's an example:

```python
import numpy as np

# Create a 1-dimensional array
arr = np.array([1, 2, 3, 4, 5, 6, 7, 8])

# Split the array into sub-arrays of unequal size
sub_arrays = np.split(arr, [3, 5, 6])

# Concatenate the sub-arrays into a single array
new_arr = np.concatenate(sub_arrays)

# Print the new array
print(new_arr)
```

In this example, we split the array into sub-arrays of sizes 3, 2, and 1, respectively, using the `split()` function. We then concatenate the sub-arrays into a single array using the `concatenate()` function. The output of the code will be:

```csharp
[1 2 3 4 5 6 7 8]
```
