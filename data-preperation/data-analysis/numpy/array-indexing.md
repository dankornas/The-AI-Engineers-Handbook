# Array Indexing

***

### Access Array Elements

Array indexing is the same as accessing an array element.

You can access an array element by referring to its index number.

The indexes in NumPy arrays start with 0, meaning that the first element has index 0, and the second has index 1 etc.

#### Example

Get the first element from the following array:

import numpy as np

arr = np.array(\[1, 2, 3, 4])

print(arr\[0])

Try it Yourself »

#### Example

Get the second element from the following array.

import numpy as np

arr = np.array(\[1, 2, 3, 4])

print(arr\[1])

Try it Yourself »

#### Example

Get third and fourth elements from the following array and add them.

import numpy as np

arr = np.array(\[1, 2, 3, 4])

print(arr\[2] + arr\[3])

Try it Yourself »

***

***

### Access 2-D Arrays

To access elements from 2-D arrays we can use comma separated integers representing the dimension and the index of the element.

Think of 2-D arrays like a table with rows and columns, where the row represents the dimension and the index represents the column.

#### Example

Access the element on the first row, second column:

import numpy as np

arr = np.array(\[\[1,2,3,4,5], \[6,7,8,9,10]])

print('2nd element on 1st row: ', arr\[0, 1])

Try it Yourself »

#### Example

Access the element on the 2nd row, 5th column:

import numpy as np

arr = np.array(\[\[1,2,3,4,5], \[6,7,8,9,10]])

print('5th element on 2nd row: ', arr\[1, 4])

Try it Yourself »

***

### Access 3-D Arrays

To access elements from 3-D arrays we can use comma separated integers representing the dimensions and the index of the element.

#### Example

Access the third element of the second array of the first array:

import numpy as np

arr = np.array(\[\[\[1, 2, 3], \[4, 5, 6]], \[\[7, 8, 9], \[10, 11, 12]]])

print(arr\[0, 1, 2])

Try it Yourself »

#### Example Explained

`arr[0, 1, 2]` prints the value `6`.

And this is why:

The first number represents the first dimension, which contains two arrays:\
\[\[1, 2, 3], \[4, 5, 6]]\
and:\
\[\[7, 8, 9], \[10, 11, 12]]\
Since we selected `0`, we are left with the first array:\
\[\[1, 2, 3], \[4, 5, 6]]

The second number represents the second dimension, which also contains two arrays:\
\[1, 2, 3]\
and:\
\[4, 5, 6]\
Since we selected `1`, we are left with the second array:\
\[4, 5, 6]

The third number represents the third dimension, which contains three values:\
4\
5\
6\
Since we selected `2`, we end up with the third value:\
6

***

### Negative Indexing

Use negative indexing to access an array from the end.

#### Example

Print the last element from the 2nd dim:

import numpy as np

arr = np.array(\[\[1,2,3,4,5], \[6,7,8,9,10]])

print('Last element from 2nd dim: ', arr\[1, -1])

Try it Yourself »

***

### Test Yourself With Exercises

### Exercise:

Insert the correct syntax for printing the first item in the array.

```
arr = np.array([1, 2, 3, 4, 5])

print(arr)
```

Start the Exercise

\
