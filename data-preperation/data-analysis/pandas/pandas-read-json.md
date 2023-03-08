# Pandas Read JSON

Pandas also provides a way to read data from JSON (JavaScript Object Notation) files. JSON is a lightweight data interchange format commonly used for transmitting data between a server and a web application.

To read a JSON file in Pandas, you can use the `read_json()` function. Here's an example of how to use it:

```python
import pandas as pd

# read a JSON file into a DataFrame
df = pd.read_json('data.json')

# print the DataFrame
print(df)
```

In this example, we're reading a JSON file named 'data.json' into a Pandas DataFrame. The `read_json()` function takes the name of the file as its argument, and returns a DataFrame object.

By default, `read_json()` assumes that the JSON file has a "record-oriented" format, which means that each line in the file represents a separate JSON object. If your JSON file doesn't have this format, you can specify a different format using the `orient` parameter:

```python
# read a JSON file with a different orientation
df = pd.read_json('data.json', orient='columns')

# print the DataFrame
print(df)
```

In this example, we're reading a JSON file with a "column-oriented" format, which means that each column in the DataFrame corresponds to a key in the JSON objects. We're specifying the orientation using the `orient` parameter, which can take one of several values.

You can also read JSON data directly from a URL using the `read_json()` function. Here's an example:

```python
# read JSON data from a URL
url = 'https://example.com/data.json'
df = pd.read_json(url)

# print the DataFrame
print(df)
```

In this example, we're reading JSON data from the URL '[https://example.com/data.json](https://example.com/data.json)'. The `read_json()` function can read data from any URL that returns a valid JSON response.

`read_json()` has many other parameters that you can use to customize how your JSON file is read. You can find more information about these parameters in the Pandas documentation.
