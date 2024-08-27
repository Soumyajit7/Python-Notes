Let's go through the various list operations in Python, using the examples you provided:

### 1. Creating a List
You can create a list by enclosing elements in square brackets `[]`.
```python
sample_list = ["Mark", 5, "Jack", 9, "Chan", 5]
print("Sample List:", sample_list)
```

### 2. Length of the List
Use the `len()` function to get the number of elements in the list.
```python
print("\nNumber of elements in the list:", len(sample_list))
```

### 3. Direct Access
Access elements by their index. Indexing starts at 0.
```python
print("\nElement at 2nd index position:", sample_list[2])
```

### 4. Direct Modification
Modify elements by assigning a new value to a specific index.
```python
sample_list[2] = "James"
print("\nElement at 2nd index position after Direct MODIFICATION:", sample_list[2])
```

### 5. Adding & Extending an Element
Use the `append()` & `extend()` method to add an element & list to the end of the list.
```python
sample_list.append("James")
print("\nAfter adding element to list:", sample_list)

sample_list.extend(["Ram", "Sam"])
print("\nAfter adding a list to another list:", sample_list)
```

### 6. Combining Two Lists
You can concatenate lists using the `+=` operator or the `+` operator.
```python
new_list = ["Henry", "Tim"]
sample_list += new_list
print("\nAfter combining two lists:", sample_list)
```

### 7. List Iteration
#### Using `range()` and `len()`
Iterate over the list using a `for` loop with `range()`.
```python
list_of_airlines = ["AI", "SJ", "JA", "EM", "AA"]
print("\nIterating the list using range()")
for index in range(len(list_of_airlines)):
    print(list_of_airlines[index])
```

#### Using `in`
Iterate directly over the elements.
```python
print("\nIterating the list using keyword in")
for airline in list_of_airlines:
    print(airline)
```

### 8. List Searching
Check if an element exists in the list using the `in` keyword.
```python
airline = "AI"
if airline in list_of_airlines:
    print("Airline found")
else:
    print("Airline not found")
```

### 9. List Slicing
Extract a portion of the list using slicing.
```python
new_list = list_of_airlines[1:4]
print("\nList Slice:", new_list)
new_list = list_of_airlines[-4:-1]
print(new_list)
```

### 10. List of Lists
Lists can contain other lists, creating a nested structure.
```python
airline_details = [["AI", 8], ["EM", 10], ["BA", 7]]
print(airline_details[2][1])  # Accessing nested list elements
print(airline_details[1])     # Accessing a nested list
```

### 11. List Functions
#### `index()`
Find the index of the first occurrence of a value.
```python
mark_list = [78, 90, 90, 95, 83, 95]
mark_pos1 = mark_list.index(90)    # Find the index of the first occurrence of 90
print("Index position of mark 90:", mark_pos1)

mark_pos2 = mark_list.index(90, mark_pos1)    # Find the index of the second occurrence of 90, starting the search after the first occurrence
print(mark_pos2)
```

#### `append()`
Add an element to the end of the list.
```python
mark_list.append(54)
print("After adding new marks:", mark_list)
```

#### `insert()`
Insert an element at a specific index.
```python
mark_list.insert(2, 98)
print("After inserting 98 at the 2nd index position:", mark_list)
```

#### `pop()`
Remove and return an element at a specific index.
```python
mark_list.pop(1)
print("After removing the marks at the 1st index position:", mark_list)
```

#### `remove()`
Remove the first occurrence of a value.
```python
mark_list.remove(95)
print("After removing the first occurrence of 95 from the list:", mark_list)
```

#### `sort()`
Sort the list in ascending order.
```python
mark_list.sort()
print("After sorting the marks in the given list:", mark_list)
```

#### `reverse()`
Reverse the order of the list.
```python
mark_list.reverse()
print("After reversing the marks in the given list:", mark_list)
```
