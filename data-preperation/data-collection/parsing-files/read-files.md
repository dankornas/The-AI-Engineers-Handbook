# Read Files

## Open a File on the Server

```
# examplefile.txt

Hello! Welcome to demofile.txt
This file is for testing purposes.
Good Luck!
```

You can open files with the `open` method.

```python
f = open("demofile.txt", "r")
print(f.read())
```

If a file is located in a different location on the server, you need to specify the full path:

```python
f = open("D:\\myfiles\welcome.txt", "r")
print(f.read())
```

## Read only parts of a files

Using the `read()` method will return the entire content of a text file. By passing in a number you can specify the number of characters to read from the text file.

```python
f = open("demofile.txt", "r")
print(f.read(5))
```

## Read lines

You can return one line at a time using the `readline()` method.

```python
f = open("demofile.txt", "r")
print(f.readline())
```

By looping through the lines of the file, you can read the whole file, line by line.

```python
f = open("demofile.txt", "r")
for x in f:
  print(x)
```

## Close Files

It is a good practice to always close the file when you are done with it.

```python
f = open("demofile.txt", "r")
print(f.readline())
f.close()
```
