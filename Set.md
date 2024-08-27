Let's break down the set operations in Python using your examples:

### Creating Sets
1. **Using curly braces `{}`**:
    ```python
    flight_set = {500, 520, 600, 345, 520, 634, 600, 500, 200, 200}
    print(flight_set)  # Output: {200, 345, 600, 634, 500, 520}
    print(type(flight_set))  # Output: <class 'set'>
    ```
    - **Note**: Sets automatically remove duplicate values.

2. **Using the `set()` keyword**:
    ```python
    flights_at_src = ["AI230", "BA944", "EM395", "AI704", "BA944", "AI704"]
    flights_at_dest = ["SI107", "AI034", "EM395", "AI704", "BA802", "SI236"]
    print(set(flights_at_src))  # Output: {'AI230', 'BA944', 'EM395', 'AI704'}
    print(set(flights_at_dest))  # Output: {'SI107', 'AI034', 'EM395', 'AI704', 'BA802', 'SI236'}
    ```

### Set Operations
1. **Intersection (`&`)**:
    - Finds common elements between two sets.
    ```python
    set_1 = {500, 520, 600, 345, 634, "Annie", 200, "Henry", "Helen", "Maria", "George"}
    set_2 = {500, 520, 600, "George", "Annie", "Jack", 634, "Henry", "Helen", "Maria", "Remo"}
    new_set_1 = set_1 & set_2
    print("set_1 & set_2 =>", new_set_1)  # Output: {520, 634, 600, 'George', 'Annie', 'Henry', 'Helen', 'Maria', 500}
    ```

2. **Difference (`-`)**:
    - Finds elements that are in the first set but not in the second.
    ```python
    new_set_2 = set_1 - set_2
    print("set_1 - set_2 =>", new_set_2)  # Output: {200, 345}
    ```

3. **Union (`|`)**:
    - Merges two sets, removing duplicates.
    ```python
    new_set_3 = set_1 | set_2
    print("set_1 | set_2 =>", new_set_3)  # Output: {200, 345, 520, 634, 600, 'George', 'Annie', 'Jack', 'Henry', 'Helen', 'Maria', 'Remo', 500}
    ```

### Additional Set Operations
- **Symmetric Difference (`^`)**:
    - Finds elements that are in either of the sets, but not in both.
    ```python
    new_set_4 = set_1 ^ set_2
    print("set_1 ^ set_2 =>", new_set_4)  # Output: {200, 345, 'Jack', 'Remo'}
    ```

- **Subset (`<=`)**:
    - Checks if one set is a subset of another.
    ```python
    print(set_1 <= set_2)  # Output: False
    ```

- **Superset (`>=`)**:
    - Checks if one set is a superset of another.
    ```python
    print(set_1 >= set_2)  # Output: False
    ```

- **Disjoint (`isdisjoint()`)**:
    - Checks if two sets have no elements in common.
    ```python
    print(set_1.isdisjoint(set_2))  # Output: False
    ```