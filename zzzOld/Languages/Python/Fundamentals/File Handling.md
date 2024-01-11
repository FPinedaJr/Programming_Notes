- File handling is an important part of any web application.
- Python has several functions for creating, reading, updating, and deleting files.

## Open

The key function for working with files in Python is the `open()` function.
The `open()` function takes two parameters; *filename*, and *mode*.

There are **four** different methods (modes) for opening a file:
	`"r"` - Read - Default value. Opens a file for reading, error if the file does not exist
	`"a"` - Append - Opens a file for appending, creates the file if it does not exist
	`"w"` - Write - Opens a file for writing, creates the file if it does not exist
	`"x"` - Create - Creates the specified file, returns an error if the file exists

In addition you can specify if the file should be handled as binary or text mode:
	`"t"` - Text - Default value. Text mode
	`"b"` - Binary - Binary mode (e.g. images)

To open a file for reading it is enough to specify the name of the file:
```python
f = open("meow.txt")
f = open("meow.txt", "rt")
```
   *opens the file in read and text mode (defaults)*

## Reading a File
Assume we have the following file "meow.txt", located in the same folder as Python and it contains:
```
in "meow.txt":
meow meow meow
```
then

```python
f = open("demofile.txt", "r")
print(f.read())
```

```output
>>>meow meow meow
```

## Reading a File in a Different Location

If the file is located in a different location, you will have to specify the file path, like this:
This is known as **Absolute Pathing**:

		The python file is in "C:\Users\USER\Desktop\meowLab" while
		The txt file is in "C:\Users\USER\Desktop"

```python
f = open("C:/Users/USER/Desktop/meowx.txt", "r")
print(f.read())
```
***NOTE:** You have to put an "r" before the path since python reads "\\" as an escape character.*

As an alternative, you can also use forward slashes "/"
```python
f = open("C:/Users/USER/Desktop/meowx.txt", "r")
print(f.read())
```

```output
>>>meow meow meow
```

## Reading Only Part of the file

By default the `read()` method returns the whole text, but you can also specify how many characters you want to return:

```python
f = open("meow.txt", "r")  
print(f.read(4))
```

```output
meow
```
***Note:** the counting here does not start with 0 so '4' means 4 letters—"meow"*

## Reading Lines

You can return one line by using the `readline()` method:
	line as in line 1, 2, 3, ..., line 69 in  vs code

For example this time "meow.txt" contains
```
in "meow.txt":
meow meow meow
arf arf arf
hiss hiss hiss
```

```python
f = open("meow.txt", "r")
print(f.readline())
```

```output
meow meow meow

```

then,

```python
f = open("meow.txt", "r")
print(f.readline())
print(f.readline())
print(f.readline())
```

```ouput
meow meow meow

arf arf arf

hiss hiss hiss
```
***Note:** For some reason there's an empty line after each* `readline()`

## Closing a File (always)

It is a **good practice** to always close the file when you are done with it.
```python
f = open("meow.txt", "r")  
print(f.read())  
# other codes...
# other codes...
# other codes...
f.close()
```

## Writing in a file

To write to an existing file, you must use the modes 
	`"a"` - Append - will append to the end of the file
	`"w"` - Write - will overwrite any existing content

***Note:** You cannot use the* `read()` *in these modes*

### Error
if you use the normal `"r"` mode which is the default, then
you will get an error if you write:

```python
f = open("meow.txt", "r")
f.write("hello world")
print(f.read())
```

```output
io.UnsupportedOperation: not writable
```


### write( ) using mode "a" mode
- appending is like adding to the text file

```
in "meow.txt": [BEFORE]
meow meow meow
```

```python
f = open("meow.txt", "a")
f.write("hello world")
```

```
in "meow.txt": [AFTER]
meow meow meowhello world
```

to avoid this, then
```python
f = open("meow.txt", "a")
f.write("\nhello world")
```

```
in "meow.txt": [AFTER]
meow meow meow
hello world
```

### write ( ) using "w" mode
- using the `"w"` mode will overwrite the file

```
in "meow.txt": [BEFORE]
meow meow meow
```

```python
f = open("meow.txt", "w")
f.write("hello world")
```

```
in "meow.txt": [AFTER]
hello world
```

### Creating a File using "x" mode
```python
f = open("arf.txt", "x")
```

Result: a new empty text file "arf.txt" was created!

### error
If the file is already existed
```python
f = open("arf.txt", "x")
```

```output
FileExistsError: [Errno 17] File exists: 'arf.txt'
```

## Deleting a File
- To delete a file, you must import the OS module, and run its `os.remove()` function:

```python
import os  
os.remove("arf.txt")
```
Result: the text file "arf.txt" was deleted!

### error
- if the file does note exist
```python
import os  
os.remove("arf.txt")
# theres no "arf.txt" file
```

```output
FileNotFoundError: [WinError 2] The system cannot find the file specified: 'arf.txt'
```

## Delete an Entire Directory(folder)

```python
import os  
os.rmdir("myfolder")
```
Result: the folder "myfolder" was deleted!

### error
- if the file does note exist
```python
import os  
os.rmdir("myfolder")
# theres no folder named "myfolder"
```

```output
FileNotFoundError: [WinError 2] The system cannot find the file specified: 'myfolder'
```

## Check if File Exist
- To avoid getting an error, you might want to check if the file exists before you try to delete it:

```python
import os
os.path.exists("meow.txt") # returns True if file exist
```

