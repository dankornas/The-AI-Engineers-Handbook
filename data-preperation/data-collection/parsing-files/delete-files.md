# Delete Files



To delete a file with Python, you will first need to import the os module. This module provides functions for interacting with the operating system. Here is an example of importing the os module:

```python
import os
```

Once the os module is imported, you can use the os.path.exists() function to check if a file or directory exists. This function takes the path of the file or directory as an argument and returns True if the file or directory exists, and False if it does not exist. Here is an example of using the os.path.exists() function:

```python
Copy codeimport os
if os.path.exists('my_file.txt'):
    print('The file exists')
else:
    print('The file does not exist')
```

You can use the os.remove() function to delete a file. This function takes the file path as an argument and deletes the file. Here is an example of using the os.remove() function:

```python
import os
os.remove('my_file.txt')
```

In this example, the file 'my\_file.txt' is deleted.

If you want to delete a directory and all of its contents, you can use the os.rmdir() function. This function takes the directory path as an argument and deletes the directory. Here is an example of using the os.rmdir() function:

```python
import os
os.rmdir('my_directory')
```

In this example, the directory 'my\_directory' is deleted.

It is important to note that the os.remove() and os.rmdir() functions do not move the file or directory to the trash or recycle bin. They permanently delete the file or directory.

In summary, to delete a file with Python you need to:

1. Import the os module
2. Use the os.remove() or os.rmdir() function to delete the file or directory
3. Be aware that the file or directory is permanently deleted and is not moved to the trash or recycle bin.
