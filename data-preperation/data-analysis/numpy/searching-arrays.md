# Searching Arrays

### Searching Arrays

NumPy provides several functions to search for specific values or elements in an array. These functions include:

* `where()`: Returns the indices of elements in an array where a given condition is true.
* `searchsorted()`: Finds the indices where elements should be inserted to maintain order in a sorted array.
* `extract()`: Extracts elements from an array that satisfy a given condition.

### **`where()`**

The `where()` function takes a single argument, which is a Boolean condition, and returns the indices of the elements in the array where the condition is `True`. Here's an example:

```python
import numpy as np

# Create a 1-dimensional array
arr = np.array([1, 2, 3, 4, 5, 6, 7, 8])

# Find the indices of the elements where the value is greater than 5
indices = np.where(arr > 5)

# Print the indices
print(indices)
```

In this example, we create a 1-dimensional array with the values `[1, 2, 3, 4, 5, 6, 7, 8]`. We then use the `where()` function to find the indices of the elements where the value is greater than 5. The output of the code will be:

```c
(array([5, 6, 7]),)
```

Note that the output is a tuple containing a single element, which is an array of indices.

### **`searchsorted()`**

The `searchsorted()` function takes two arguments: the array to be searched, and the value to be searched for. It returns the index at which the value should be inserted in order to maintain the sorted order of the array. Here's an example:

```python
import numpy as np

# Create a sorted 1-dimensional array
arr = np.array([1, 2, 3, 4, 5, 6, 7, 8])

# Find the index where the value 6 should be inserted to maintain order
index = np.searchsorted(arr, 6)

# Print the index
print(index)
```

In this example, we create a 1-dimensional array with the values `[1, 2, 3, 4, 5, 6, 7, 8]`, which is sorted in ascending order. We then use the `searchsorted()` function to find the index where the value 6 should be inserted to maintain the sorted order. The output of the code will be:

```
5
```

### **`extract()`**

The `extract()` function takes two arguments: the array to be searched, and a Boolean condition that determines which elements to extract. It returns an array containing only the elements that satisfy the condition. Here's an example:

```python
import numpy as np

# Create a 1-dimensional array
arr = np.array([1, 2, 3, 4, 5, 6, 7, 8])

# Extract the elements where the value is greater than 5
new_arr = np.extract(arr > 5, arr)

# Print the new array
print(new_arr)
```

In this example, we create a 1-dimensional array with the values `[1, 2, 3, 4, 5, 6, 7, 8]`. We then use the `extract()` function to extract the elements where the value is greater than 5. The output of the code will be:

```csharp
[6 7 8]
```
