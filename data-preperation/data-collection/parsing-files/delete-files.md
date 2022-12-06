# Delete Files

### Delete a File

To delete a file, you must import the OS module, and run its `os.remove()` function.&#x20;

eRemove the file "demofile.txt":

```python
import os
os.remove("demofile.txt")
```

***

### Check if a File exists

To avoid getting an error, you might want to check if the file exists before you try to delete it.

Check if file exists, _then_ delete it:

```python
import os
if os.path.exists("demofile.txt"):
  os.remove("demofile.txt")
else:
  print("The file does not exist")
```

***

### Delete Folder

To delete an entire folder, use the `os.rmdir()` method.

Remove the folder "myfolder":

```python
import os
os.rmdir("myfolder")
```

**Note:** You can only remove _empty_ folders.

***

\
