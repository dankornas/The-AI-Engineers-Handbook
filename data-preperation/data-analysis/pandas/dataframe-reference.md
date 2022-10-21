# DataFrame Reference

All properties and methods of the DataFrame object, with explanations and examples:

| Property/Method    | Description                                                                                                                                |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------ |
| abs()              | Return a DataFrame with the absolute value of each value                                                                                   |
| add()              | Adds the values of a DataFrame with the specified value(s)                                                                                 |
| add\_prefix()      | Prefix all labels                                                                                                                          |
| add\_suffix()      | Suffix all labels                                                                                                                          |
| agg()              | Apply a function or a function name to one of the axis of the DataFrame                                                                    |
| aggregate()        | Apply a function or a function name to one of the axis of the DataFrame                                                                    |
| align()            | Aligns two DataFrames with a specified join method                                                                                         |
| all()              | Return True if all values in the DataFrame are True, otherwise False                                                                       |
| any()              | Returns True if any of the values in the DataFrame are True, otherwise False                                                               |
| append()           | Append new columns                                                                                                                         |
| applymap()         | Execute a function for each element in the DataFrame                                                                                       |
| apply()            | Apply a function to one of the axis of the DataFrame                                                                                       |
| assign()           | Assign new columns                                                                                                                         |
| astype()           | Convert the DataFrame into a specified dtype                                                                                               |
| at                 | Get or set the value of the item with the specified label                                                                                  |
| axes               | Returns the labels of the rows and the columns of the DataFrame                                                                            |
| bfill()            | Replaces NULL values with the value from the next row                                                                                      |
| bool()             | Returns the Boolean value of the DataFrame                                                                                                 |
| columns            | Returns the column labels of the DataFrame                                                                                                 |
| combine()          | Compare the values in two DataFrames, and let a function decide which values to keep                                                       |
| combine\_first()   | Compare two DataFrames, and if the first DataFrame has a NULL value, it will be filled with the respective value from the second DataFrame |
| compare()          | Compare two DataFrames and return the differences                                                                                          |
| convert\_dtypes()  | Converts the columns in the DataFrame into new dtypes                                                                                      |
| corr()             | Find the correlation (relationship) between each column                                                                                    |
| count()            | Returns the number of not empty cells for each column/row                                                                                  |
| cov()              | Find the covariance of the columns                                                                                                         |
| copy()             | Returns a copy of the DataFrame                                                                                                            |
| cummax()           | Calculate the cumulative maximum values of the DataFrame                                                                                   |
| cummin()           | Calculate the cumulative minmum values of the DataFrame                                                                                    |
| cumprod()          | Calculate the cumulative product over the DataFrame                                                                                        |
| cumsum()           | Calculate the cumulative sum over the DataFrame                                                                                            |
| describe()         | Returns a description summary for each column in the DataFrame                                                                             |
| diff()             | Calculate the difference between a value and the value of the same column in the previous row                                              |
| div()              | Divides the values of a DataFrame with the specified value(s)                                                                              |
| dot()              | Multiplies the values of a DataFrame with values from another array-like object, and add the result                                        |
| drop()             | Drops the specified rows/columns from the DataFrame                                                                                        |
| drop\_duplicates() | Drops duplicate values from the DataFrame                                                                                                  |
| droplevel()        | Drops the specified index/column(s)                                                                                                        |
| dropna()           | Drops all rows that contains NULL values                                                                                                   |
| dtypes             | Returns the dtypes of the columns of the DataFrame                                                                                         |
| duplicated()       | Returns True for duplicated rows, otherwise False                                                                                          |
| empty              | Returns True if the DataFrame is empty, otherwise False                                                                                    |
| eq()               | Returns True for values that are equal to the specified value(s), otherwise False                                                          |
| equals()           | Returns True if two DataFrames are equal, otherwise False                                                                                  |
| eval               | Evaluate a specified string                                                                                                                |
| explode()          | Converts each element into a row                                                                                                           |
| ffill()            | Replaces NULL values with the value from the previous row                                                                                  |
| fillna()           | Replaces NULL values with the specified value                                                                                              |
| filter()           | Filter the DataFrame according to the specified filter                                                                                     |
| first()            | Returns the first rows of a specified date selection                                                                                       |
| floordiv()         | Divides the values of a DataFrame with the specified value(s), and floor the values                                                        |
| ge()               | Returns True for values greater than, or equal to the specified value(s), otherwise False                                                  |
| get()              | Returns the item of the specified key                                                                                                      |
| groupby()          | Groups the rows/columns into specified groups                                                                                              |
| gt()               | Returns True for values greater than the specified value(s), otherwise False                                                               |
| head()             | Returns the header row and the first 10 rows, or the specified number of rows                                                              |
| iat                | Get or set the value of the item in the specified position                                                                                 |
| idxmax()           | Returns the label of the max value in the specified axis                                                                                   |
| idxmin()           | Returns the label of the min value in the specified axis                                                                                   |
| iloc               | Get or set the values of a group of elements in the specified positions                                                                    |
| index              | Returns the row labels of the DataFrame                                                                                                    |
| infer\_objects()   | Change the dtype of the columns in the DataFrame                                                                                           |
| info()             | Prints information about the DataFrame                                                                                                     |
| insert()           | Insert a column in the DataFrame                                                                                                           |
| interpolate()      | Replaces not-a-number values with the interpolated method                                                                                  |
| isin()             | Returns True if each elements in the DataFrame is in the specified value                                                                   |
| isna()             | Finds not-a-number values                                                                                                                  |
| isnull()           | Finds NULL values                                                                                                                          |
| items()            | Iterate over the columns of the DataFrame                                                                                                  |
| iteritems()        | Iterate over the columns of the DataFrame                                                                                                  |
| iterrows()         | Iterate over the rows of the DataFrame                                                                                                     |
| itertuples()       | Iterate over the rows as named tuples                                                                                                      |
| join()             | Join columns of another DataFrame                                                                                                          |
| last()             | Returns the last rows of a specified date selection                                                                                        |
| le()               | Returns True for values less than, or equal to the specified value(s), otherwise False                                                     |
| loc                | Get or set the value of a group of elements specified using their labels                                                                   |
| lt()               | Returns True for values less than the specified value(s), otherwise False                                                                  |
| keys()             | Returns the keys of the info axis                                                                                                          |
| kurtosis()         | Returns the kurtosis of the values in the specified axis                                                                                   |
| mask()             | Replace all values where the specified condition is True                                                                                   |
| max()              | Return the max of the values in the specified axis                                                                                         |
| mean()             | Return the mean of the values in the specified axis                                                                                        |
| median()           | Return the median of the values in the specified axis                                                                                      |
| melt()             | Reshape the DataFrame from a wide table to a long table                                                                                    |
| memory\_usage()    | Returns the memory usage of each column                                                                                                    |
| merge()            | Merge DataFrame objects                                                                                                                    |
| min()              | Returns the min of the values in the specified axis                                                                                        |
| mod()              | Modules (find the remainder) of the values of a DataFrame                                                                                  |
| mode()             | Returns the mode of the values in the specified axis                                                                                       |
| mul()              | Multiplies the values of a DataFrame with the specified value(s)                                                                           |
| ndim               | Returns the number of dimensions of the DataFrame                                                                                          |
| ne()               | Returns True for values that are not equal to the specified value(s), otherwise False                                                      |
| nlargest()         | Sort the DataFrame by the specified columns, descending, and return the specified number of rows                                           |
| notna()            | Finds values that are not not-a-number                                                                                                     |
| notnull()          | Finds values that are not NULL                                                                                                             |
| nsmallest()        | Sort the DataFrame by the specified columns, ascending, and return the specified number of rows                                            |
| nunique()          | Returns the number of unique values in the specified axis                                                                                  |
| pct\_change()      | Returns the percentage change between the previous and the current value                                                                   |
| pipe()             | Apply a function to the DataFrame                                                                                                          |
| pivot()            | Re-shape the DataFrame                                                                                                                     |
| pivot\_table()     | Create a spreadsheet pivot table as a DataFrame                                                                                            |
| pop()              | Removes an element from the DataFrame                                                                                                      |
| pow()              | Raise the values of one DataFrame to the values of another DataFrame                                                                       |
| prod()             | Returns the product of all values in the specified axis                                                                                    |
| product()          | Returns the product of the values in the specified axis                                                                                    |
| quantile()         | Returns the values at the specified quantile of the specified axis                                                                         |
| query()            | Query the DataFrame                                                                                                                        |
| radd()             | Reverse-adds the values of one DataFrame with the values of another DataFrame                                                              |
| rdiv()             | Reverse-divides the values of one DataFrame with the values of another DataFrame                                                           |
| reindex()          | Change the labels of the DataFrame                                                                                                         |
| reindex\_like()    | ??                                                                                                                                         |
| rename()           | Change the labels of the axes                                                                                                              |
| rename\_axis()     | Change the name of the axis                                                                                                                |
| reorder\_levels()  | Re-order the index levels                                                                                                                  |
| replace()          | Replace the specified values                                                                                                               |
| reset\_index()     | Reset the index                                                                                                                            |
| rfloordiv()        | Reverse-divides the values of one DataFrame with the values of another DataFrame                                                           |
| rmod()             | Reverse-modules the values of one DataFrame to the values of another DataFrame                                                             |
| rmul()             | Reverse-multiplies the values of one DataFrame with the values of another DataFrame                                                        |
| round()            | Returns a DataFrame with all values rounded into the specified format                                                                      |
| rpow()             | Reverse-raises the values of one DataFrame up to the values of another DataFrame                                                           |
| rsub()             | Reverse-subtracts the values of one DataFrame to the values of another DataFrame                                                           |
| rtruediv()         | Reverse-divides the values of one DataFrame with the values of another DataFrame                                                           |
| sample()           | Returns a random selection elements                                                                                                        |
| sem()              | Returns the standard error of the mean in the specified axis                                                                               |
| select\_dtypes()   | Returns a DataFrame with columns of selected data types                                                                                    |
| shape              | Returns the number of rows and columns of the DataFrame                                                                                    |
| set\_axis()        | Sets the index of the specified axis                                                                                                       |
| set\_flags()       | Returns a new DataFrame with the specified flags                                                                                           |
| set\_index()       | Set the Index of the DataFrame                                                                                                             |
| size               | Returns the number of elements in the DataFrame                                                                                            |
| skew()             | Returns the skew of the values in the specified axis                                                                                       |
| sort\_index()      | Sorts the DataFrame according to the labels                                                                                                |
| sort\_values()     | Sorts the DataFrame according to the values                                                                                                |
| squeeze()          | Converts a single column DataFrame into a Series                                                                                           |
| stack()            | Reshape the DataFrame from a wide table to a long table                                                                                    |
| std()              | Returns the standard deviation of the values in the specified axis                                                                         |
| sum()              | Returns the sum of the values in the specified axis                                                                                        |
| sub()              | Subtracts the values of a DataFrame with the specified value(s)                                                                            |
| swaplevel()        | Swaps the two specified levels                                                                                                             |
| T                  | Turns rows into columns and columns into rows                                                                                              |
| tail()             | Returns the headers and the last rows                                                                                                      |
| take()             | Returns the specified elements                                                                                                             |
| to\_xarray()       | Returns an xarray object                                                                                                                   |
| transform()        | Execute a function for each value in the DataFrame                                                                                         |
| transpose()        | Turns rows into columns and columns into rows                                                                                              |
| truediv()          | Divides the values of a DataFrame with the specified value(s)                                                                              |
| truncate()         | Removes elements outside of a specified set of values                                                                                      |
| update()           | Update one DataFrame with the values from another DataFrame                                                                                |
| value\_counts()    | Returns the number of unique rows                                                                                                          |
| values             | Returns the DataFrame as a NumPy array                                                                                                     |
| var()              | Returns the variance of the values in the specified axis                                                                                   |
| where()            | Replace all values where the specified condition is False                                                                                  |
| xs()               | Returns the cross-section of the DataFrame                                                                                                 |
| \_\_iter\_\_()     | Returns an iterator of the info axes                                                                                                       |

***

\
