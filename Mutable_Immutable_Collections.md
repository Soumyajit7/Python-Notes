In Python, collections can be categorized as mutable or immutable based on whether their contents can be changed after creation.

### Mutable Collections
1. **Lists**: Ordered, changeable, and allow duplicate elements.
   ```python    
   my_list = [1, 2, 3]
   my_list.append(4)  # my_list is now [1, 2, 3, 4]
   ```
2. **Dictionaries**: Unordered, changeable, and indexed by keys.
   ```python
   my_dict = {'a': 1, 'b': 2}
   my_dict['c'] = 3  # my_dict is now {'a': 1, 'b': 2, 'c': 3}
   ```
3. **Sets**: Unordered, changeable, and do not allow duplicate elements.
   ```python
   my_set = {1, 2, 3}
   my_set.add(4)  # my_set is now {1, 2, 3, 4}
   ```
4. **Byte Arrays**: Mutable sequence of bytes.
   ```python
   my_byte_array = bytearray(b"Hello")
   my_byte_array[0] = 72  # my_byte_array is now bytearray(b'Hello')
   ```

### Immutable Collections
1. **Tuples**: Ordered, unchangeable, and allow duplicate elements.
   ```python
   my_tuple = (1, 2, 3)
   # my_tuple cannot be changed
   ```
2. **Strings**: Ordered, unchangeable, and allow duplicate elements.
   ```python
   my_string = "Hello"
   # my_string cannot be changed
   ```
3. **Frozen Sets**: Unordered, unchangeable, and do not allow duplicate elements.
   ```python
   my_frozen_set = frozenset([1, 2, 3])
   # my_frozen_set cannot be changed
   ```
4. **Bytes**: Immutable sequence of bytes.
   ```python
   my_bytes = b"Hello"
   # my_bytes cannot be changed
   ```
