# Pandas Read CSV

One of the most common operations in data analysis is reading data from an external file. Pandas provides a convenient method for reading CSV files, which is a common file format used for storing tabular data.

To read a CSV file in Pandas, you can use the `read_csv()` function. Here's an example of how to use it:

```python
import pandas as pd

# read a CSV file into a DataFrame
df = pd.read_csv('data.csv')

# print the DataFrame
print(df)
```

In this example, we're reading a CSV file named 'data.csv' into a Pandas DataFrame. The `read_csv()` function takes the name of the file as its argument, and returns a DataFrame object.

By default, `read_csv()` assumes that the first row of the CSV file contains the column headers. If your CSV file doesn't have column headers, you can specify them using the `header` parameter:

```python
# read a CSV file without column headers
df = pd.read_csv('data.csv', header=None, names=['col1', 'col2', 'col3'])

# print the DataFrame
print(df)
```

In this example, we're reading a CSV file without column headers. We're specifying the column names using the `names` parameter, which takes a list of column names.

You can also specify the delimiter used in the CSV file using the `delimiter` parameter. By default, `read_csv()` assumes that the delimiter is a comma. Here's an example of how to specify a different delimiter:

```python
# read a CSV file with a different delimiter
df = pd.read_csv('data.csv', delimiter=';')

# print the DataFrame
print(df)
```

In this example, we're reading a CSV file with a semicolon (;) as the delimiter. We're specifying the delimiter using the `delimiter` parameter.

`read_csv()` has many other parameters that you can use to customize how your CSV file is read. You can find more information about these parameters in the Pandas documentation.
