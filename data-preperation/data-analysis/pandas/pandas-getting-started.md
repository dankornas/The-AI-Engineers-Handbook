# Pandas Getting Started

Pandas is a Python library used for data manipulation and analysis. It provides powerful data structures for handling structured and time-series data

### Installing Pandas

Pandas can be installed using pip, the Python package manager. Open your terminal or command prompt and run the following command:

```
pip install pandas
```

This will download and install the latest version of Pandas on your system.

### Importing Pandas

Once Pandas is installed, you can import it into your Python script using the `import` statement. It is a convention to use the alias `pd` when importing Pandas:

```python
import pandas as pd
```

### Using Pandas as pd

In the above import statement, we used `as pd` to create an alias for Pandas. This is a commonly used convention, as it makes it easier to refer to the library throughout your code. Instead of typing out `pandas` every time you want to use it, you can simply type `pd`. For example:

```python
import pandas as pd

# create a pandas series
s = pd.Series([1, 3, 5, np.nan, 6, 8])

# print the series
print(s)
```

In this example, we create a Pandas Series object using the `pd.Series()` function, and assign it to the variable `s`. By using `pd` as an alias for Pandas, we are able to call the `pd.Series()` function without having to type out `pandas.Series()`.
