# Filter Array

***

### Filtering Arrays

Getting some elements out of an existing array and creating a new array out of them is called _filtering_.

In NumPy, you filter an array using a _boolean index list_.

A _boolean index list_ is a list of booleans corresponding to indexes in the array.

If the value at an index is `True` that element is contained in the filtered array, if the value at that index is `False` that element is excluded from the filtered array.

#### Example

Create an array from the elements on index 0 and 2:

import numpy as np

arr = np.array(\[41, 42, 43, 44])

x = \[True, False, True, False]

newarr = arr\[x]

print(newarr)

Try it Yourself »

The example above will return `[41, 43]`, why?

Because the new array contains only the values where the filter array had the value `True`, in this case, index 0 and 2.

***

### Creating the Filter Array

In the example above we hard-coded the `True` and `False` values, but the common use is to create a filter array based on conditions.

#### Example

Create a filter array that will return only values higher than 42:

import numpy as np

arr = np.array(\[41, 42, 43, 44])

\# Create an empty list\
filter\_arr = \[]

\# go through each element in arr\
for element in arr:\
&#x20; \# if the element is higher than 42, set the value to True, otherwise False:\
&#x20; if element > 42:\
&#x20;   filter\_arr.append(True)\
&#x20; else:\
&#x20;   filter\_arr.append(False)

newarr = arr\[filter\_arr]

print(filter\_arr)\
print(newarr)

Try it Yourself »

***

***

#### Example

Create a filter array that will return only even elements from the original array:

import numpy as np

arr = np.array(\[1, 2, 3, 4, 5, 6, 7])

\# Create an empty list\
filter\_arr = \[]

\# go through each element in arr\
for element in arr:\
&#x20; \# if the element is completely divisble by 2, set the value to True, otherwise False\
&#x20; if element % 2 == 0:\
&#x20;   filter\_arr.append(True)\
&#x20; else:\
&#x20;   filter\_arr.append(False)

newarr = arr\[filter\_arr]

print(filter\_arr)\
print(newarr)

Try it Yourself »

***

### Creating Filter Directly From Array

The above example is quite a common task in NumPy and NumPy provides a nice way to tackle it.

We can directly substitute the array instead of the iterable variable in our condition and it will work just as we expect it to.

#### Example

Create a filter array that will return only values higher than 42:

import numpy as np

arr = np.array(\[41, 42, 43, 44])

filter\_arr = arr > 42

newarr = arr\[filter\_arr]

print(filter\_arr)\
print(newarr)

Try it Yourself »

#### Example

Create a filter array that will return only even elements from the original array:

import numpy as np

arr = np.array(\[1, 2, 3, 4, 5, 6, 7])

filter\_arr = arr % 2 == 0

newarr = arr\[filter\_arr]

print(filter\_arr)\
print(newarr)

Try it Yourself »

***

\
