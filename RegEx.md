It looks like you might be referring to the `re` library in Python, which is used for regular expression operations. Here are the main functions and operations you can perform with the `re` library:

### Basic Functions
1. **`re.match(pattern, string, flags=0)`**:
    - Checks for a match only at the beginning of the string.
    ```python
    import re
    result = re.match(r'\d+', '123abc')
    print(result.group())  # Output: 123
    ```

2. **`re.search(pattern, string, flags=0)`**:
    - Searches the string for a match to the pattern.
    ```python
    result = re.search(r'\d+', 'abc123')
    print(result.group())  # Output: 123
    ```

3. **`re.findall(pattern, string, flags=0)`**:
    - Returns a list of all non-overlapping matches in the string.
    ```python
    result = re.findall(r'\d+', 'abc123def456')
    print(result)  # Output: ['123', '456']
    ```

4. **`re.finditer(pattern, string, flags=0)`**:
    - Returns an iterator yielding match objects for all non-overlapping matches.
    ```python
    matches = re.finditer(r'\d+', 'abc123def456')
    for match in matches:
        print(match.group())  # Output: 123, 456
    ```

5. **`re.sub(pattern, repl, string, count=0, flags=0)`**:
    - Replaces occurrences of the pattern with `repl` in the string.
    ```python
    result = re.sub(r'\d+', '#', 'abc123def456')
    print(result)  # Output: abc#def#
    ```

6. **`re.subn(pattern, repl, string, count=0, flags=0)`**:
    - Similar to `re.sub`, but returns a tuple with the new string and the number of replacements.
    ```python
    result = re.subn(r'\d+', '#', 'abc123def456')
    print(result)  # Output: ('abc#def#', 2)
    ```

7. **`re.split(pattern, string, maxsplit=0, flags=0)`**:
    - Splits the string by occurrences of the pattern.
    ```python
    result = re.split(r'\d+', 'abc123def456')
    print(result)  # Output: ['abc', 'def', '']
    ```

### Compiling Regular Expressions
1. **`re.compile(pattern, flags=0)`**:
    - Compiles a regular expression pattern into a regex object, which can be used for matching.
    ```python
    pattern = re.compile(r'\d+')
    result = pattern.match('123abc')
    print(result.group())  # Output: 123
    ```

### Flags
- **`re.IGNORECASE` or `re.I`**: Ignore case.
- **`re.MULTILINE` or `re.M`**: Multi-line matching, affecting `^` and `$`.
- **`re.DOTALL` or `re.S`**: Make `.` match any character, including newlines.
- **`re.VERBOSE` or `re.X`**: Allow verbose regexps (useful for commenting).

### Match Object Methods
1. **`group()`**:
    - Returns the string matched by the regex.
    ```python
    match = re.search(r'(\d+)', 'abc123')
    print(match.group())  # Output: 123
    ```

2. **`start()` and `end()`**:
    - Return the start and end positions of the match.
    ```python
    print(match.start())  # Output: 3
    print(match.end())    # Output: 6
    ```

3. **`span()`**:
    - Returns a tuple containing the start and end positions of the match.
    ```python
    print(match.span())  # Output: (3, 6)
    ```

### Example Usage
Here's a comprehensive example demonstrating some of these operations:
```python
import re

text = "The rain in Spain falls mainly in the plain."

# Search for 'rain' in the text
match = re.search(r'rain', text)
if match:
    print(f"Found '{match.group()}' at position {match.start()}")

# Find all words starting with 'S'
words = re.findall(r'\bS\w+', text)
print("Words starting with 'S':", words)

# Replace 'Spain' with 'France'
new_text = re.sub(r'Spain', 'France', text)
print("Modified text:", new_text)

# Split the text by spaces
split_text = re.split(r'\s+', text)
print("Split text:", split_text)
```

The `re` library is powerful for text processing and pattern matching in Python.