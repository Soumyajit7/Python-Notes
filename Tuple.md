Let's go through the various tuple operations in Python using the examples you provided:

### 1. Creating a Tuple
You can create a tuple by enclosing elements in parentheses `()`.
```python
lunch_menu = ("Welcome Drink", "Veg Starter", "Non-Veg Starter", "Veg Main Course", "Non-Veg Main Course", "Dessert")
```

### 2. Valid Tuples
Tuples can also be created without parentheses, separated by commas.
```python
sample_tuple = "A", "B", "C"
sample_tuple1 = ("D",)
```

### 3. Length of the Tuple
Use the `len()` function to get the number of elements in the tuple.
```python
print("\nNumber of elements in the tuple, lunch_menu:", len(lunch_menu))
```

### 4. Direct Access
Access elements by their index. Indexing starts at 0.
```python
print("\nElement at 2nd index position in lunch_menu:", lunch_menu[2])
```

### 5. Concatenating Tuples
You can concatenate tuples using the `+` operator.
```python
sample_tuple = sample_tuple + sample_tuple1
print("\nConcatenating tuples:", sample_tuple)
```

### 6. Adding a Single Element
To add a single element, you need to create a new tuple with the element and concatenate it.
```python
sample_tuple = sample_tuple + ("E",)
print("\nAdding a single element to a tuple:", sample_tuple)
```

### 7. Adding Multiple Elements
Similarly, you can add multiple elements by creating a new tuple and concatenating it.
```python
sample_tuple = sample_tuple + ("F", "G")
print("\nAdding multiple elements to a tuple:", sample_tuple)
```

### 8. Iterating Tuple
#### Using `range()` and `len()`
Iterate over the tuple using a `for` loop with `range()`.
```python
print("\nIterating the tuple using range()")
for index in range(0, 3):
    print(lunch_menu[index])
```

#### Using `in`
Iterate directly over the elements.
```python
print("\nIterating the tuple using keyword in")
for food_type in lunch_menu:
    print(food_type)
```

### 9. Searching for an Element
Check if an element exists in the tuple using the `in` keyword.
```python
if "Dessert" in lunch_menu:
    print("Dessert is there")
else:
    print("Dessert is not there")
```

### 10. Slicing a Tuple
Extract a portion of the tuple using slicing.
```python
print("\nTuple slice using positive indices:", lunch_menu[1:5])
print("\nTuple slice using negative indices:", lunch_menu[-5:-1])
```

### 11. Immutability
Tuples are immutable, meaning their elements cannot be changed after creation. Attempting to modify a tuple will result in an error.
```python
# Uncomment the below code and try to visualize.
# lunch_menu[0] = "Pepper Mint"  # Direct MODIFICATION will result in an error
# print(lunch_menu)
```