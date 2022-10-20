# Strings

### Python Strings

Strings are arrays of bytes representing unicode characters.

Strings in python are surrounded by either single quotation marks, or double quotation marks.

You can assign a multiline string to a variable by using three quotes.

```python
str1 = "Welcome to complete Python Course" 
str2 = 'Welcome to the complete Python Course' 
str3 = """This is a 
       multiline 
       String"""

### Output ###
# Welcome to complete Python Course
# Welcome to the complete Python Course
# This is a 
#       multiline 
#       String
```

### Accessing Values in Strings

Indexing is used in Python to retrieve individual characters in a string.&#x20;

The index is used to retrieve the character of the string using square brackets.&#x20;

The index begins at 0.&#x20;

\-1 denotes the final character, -2 the second last character, and so on.

{% code title="Example" %}
```python
var[3]
var[-2]
```
{% endcode %}

Slicing is used in Python to access a range of characters in a string.&#x20;

The slicing operator colon " : " is utilized.

{% code title="Example" %}
```python
var[0:4]
var[:7]
```
{% endcode %}

**Indexing**&#x20;

&#x20;Example: get the 5th character from the string.

```python
s= "Captain America"
print(s[4])

### Output ###
# a
```

**Slicing**&#x20;

slice(start, stop, step), it returns a sliced object containing elements in the given range.

Example: Start from the 2nd character, stop at the 5th element, take every second character from that range.

```python
s = "Captain America"
print(s[1:5:2])

### Output ###
# at
```

### String Formatting

Python F-Strings are used to format python expressions by embedding them within string literals with minimum syntax. It is an expression that is evaluated during execution.&#x20;

They employ brackets to evaluate values and contain the f prefix.&#x20;

In order to format and output an expression in a formatted way, you should use curly braces {}.

```python
def max_no(x,y):
    return x if x>y else y
f_no = 12
s_no = 25
print(f'Max of {f_no} and {s_no} is {max(f_no,s_no)}')

### Output ###
# Max of 12 and 25 is 25
```

