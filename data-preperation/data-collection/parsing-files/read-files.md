# Read Files

##

To read a file with Python, you will first need to open the file using the open() function. This function takes the file path and the access mode as arguments, and returns a file object.

To open a file for reading, you will use the 'r' access mode. Here is an example of opening a file for reading:

```python
file = open('my_file.txt', 'r')
```

Once the file is opened, you can use the read() method to read the entire contents of the file. The read() method returns the contents of the file as a string. Here is an example of using the read() method:

```python
file = open('my_file.txt', 'r')
file_contents = file.read()
```

If you only want to read a specific portion of the file, you can use the read() method with the length argument. This argument specifies the number of characters to read from the file. Here is an example of using the read() method with the length argument:

```python
file = open('my_file.txt', 'r')
file_contents = file.read(10)
```

In this example, the read() method will only return the first 10 characters of the file.

If you want to read each line of the file separately, you can use the readline() method. This method returns the next line of the file as a string. Here is an example of using the readline() method:

```python
file = open('my_file.txt', 'r')
line1 = file.readline()
line2 = file.readline()
```

In this example, the readline() method will return the first line of the file in the line1 variable, and the second line in the line2 variable.

After you are finished reading the file, it is important to close the file using the close() method. This method frees up resources and ensures that any changes made to the file are saved. Here is an example of closing a file:

```python
file = open('my_file.txt', 'r')
file_contents = file.read()
file.close()
```

In this example, the file is opened, read, and then closed using the close() method.

In summary, to read a file with Python you need to:

1. Open the file using the open() function
2. Read the contents of the file using the read() method
3. Close the file using the close() method
