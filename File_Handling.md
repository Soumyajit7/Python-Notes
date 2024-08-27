File handling in Python allows you to create, read, write, and manipulate files. Here are the key operations with examples:

### 1. Opening a File
You can open a file using the `open()` function. It requires a filename and a mode.

- **Modes**:
  - `'r'`: Read (default)
  - `'w'`: Write (creates a new file or truncates an existing file)
  - `'a'`: Append (adds to the end of the file)
  - `'b'`: Binary mode
  - `'t'`: Text mode (default)

```python
# Open a file for reading
file = open('example.txt', 'r')
```

### 2. Reading from a File
You can read the contents of a file using methods like `read()`, `readline()`, and `readlines()`.

```python
# Read the entire file
content = file.read()
print(content)

# Read one line at a time
line = file.readline()
print(line)

# Read all lines into a list
lines = file.readlines()
print(lines)

file.close()
```

### 3. Writing to a File
You can write to a file using the `write()` and `writelines()` methods.

```python
# Open a file for writing
file = open('example.txt', 'w')

# Write a string to the file
file.write("Hello, World!\n")

# Write multiple lines
lines = ["Line 1\n", "Line 2\n", "Line 3\n"]
file.writelines(lines)

file.close()
```

### 4. Appending to a File
You can append data to the end of a file using the `'a'` mode.

```python
# Open a file for appending
file = open('example.txt', 'a')

# Append a string to the file
file.write("This is an appended line.\n")

file.close()
```

### 5. Using `with` Statement
The `with` statement is used for file handling to ensure that the file is properly closed after its suite finishes.

```python
# Using with statement
with open('example.txt', 'r') as file:
    content = file.read()
    print(content)
```

### 6. Binary Files
You can handle binary files by using the `'b'` mode.

```python
# Writing to a binary file
with open('example.bin', 'wb') as file:
    file.write(b'\x00\x01\x02\x03')

# Reading from a binary file
with open('example.bin', 'rb') as file:
    content = file.read()
    print(content)
```

### 7. File Methods
- **`file.seek(offset, whence)`**: Moves the file pointer to a specific position.
- **`file.tell()`**: Returns the current position of the file pointer.

```python
with open('example.txt', 'r') as file:
    file.seek(5)  # Move to the 5th byte
    print(file.tell())  # Output: 5
    content = file.read()
    print(content)
```

### 8. Deleting a File
You can delete a file using the `os` module.

```python
import os

# Delete a file
os.remove('example.txt')
```

File handling in Python is versatile and straightforward, making it easy to work with files across different platforms.