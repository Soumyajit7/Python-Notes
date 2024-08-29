# Numpy

  ```python
 pip install numpy
  ```

### Creating Arrays
- **`np.arange(start, stop, step)`**: Creates an array with values ranging from `start` to `stop` with a step size of `step`.
  ```python
  x = np.arange(1, 10)  # Creates an array [1, 2, 3, 4, 5, 6, 7, 8, 9]
  ```

### Array Attributes
- **`array.shape`**: Returns the shape of the array (dimensions).
  ```python
  car_attributes_arr.shape  # Example output: (10, 5)
  ```

- **`array.dtype`**: Returns the data type of the array elements.
  ```python
  car_attributes_arr.dtype  # Example output: dtype('float64')
  ```

### Array Creation with Specific Data Type
- **`np.array(object, dtype)`**: Creates an array from an object (like a list) with a specified data type.
  ```python
  car_attributes_arr = np.array(car_attributes, dtype='float')
  ```

### Indexing and Slicing
- **Indexing**: Accessing elements using indices.
  ```python
  print(car_hp_arr[0][1])  # Accesses the element at row 0, column 1
  ```

- **Slicing**: Accessing a sub-array using slice notation.
  ```python
  print(car_hp_acc_arr[0:2, 3:5])  # Accesses rows 0 to 1 and columns 3 to 4
  ```

### Statistical Operations
- **`np.mean(array)`**: Computes the mean (average) of the array elements.
  ```python
  np.mean(horsepower_arr)
  ```

- **`np.median(array)`**: Computes the median of the array elements.
  ```python
  np.median(horsepower_arr)
  ```

- **`np.min(array)`**: Finds the minimum value in the array.
  ```python
  np.min(horsepower_arr)
  ```

- **`np.max(array)`**: Finds the maximum value in the array.
  ```python
  np.max(horsepower_arr)
  ```

- **`np.argmin(array)`**: Returns the index of the minimum value in the array.
  ```python
  np.argmin(horsepower_arr)
  ```

- **`np.argmax(array)`**: Returns the index of the maximum value in the array.
  ```python
  np.argmax(horsepower_arr)
  ```

### Conditional Operations
- **`np.where(condition)`**: Returns the indices of elements that satisfy the condition.
  ```python
  np.where(horsepower_arr >= 150)
  ```

### Sorting and Summation
- **`np.sort(array)`**: Returns a sorted copy of the array.
  ```python
  np.sort(horsepower_arr)
  ```

- **`np.sum(array)`**: Computes the sum of the array elements.
  ```python
  np.sum(student_marks_arr)
  ```

### Element-wise Operations
- **`np.add(array1, array2)`**: Adds corresponding elements of two arrays.
  ```python
  np.add(student_marks_arr, additional_marks)
  ```

### Additional Common Operations
- **`np.zeros(shape)`**: Creates an array filled with zeros.
  ```python
  np.zeros((3, 4))  # Creates a 3x4 array filled with zeros
  ```

- **`np.ones(shape)`**: Creates an array filled with ones.
  ```python
  np.ones((2, 3))  # Creates a 2x3 array filled with ones
  ```

- **`np.linspace(start, stop, num)`**: Creates an array of `num` evenly spaced values between `start` and `stop`.
  ```python
  np.linspace(0, 1, 5)  # Creates an array [0. , 0.25, 0.5 , 0.75, 1. ]
  ```

- **`np.eye(N)`**: Creates an identity matrix of size `N`.
  ```python
  np.eye(3)  # Creates a 3x3 identity matrix
  ```

- **`np.random.rand(shape)`**: Creates an array of the given shape with random values between 0 and 1.
  ```python
  np.random.rand(2, 3)  # Creates a 2x3 array with random values
  ```

### Importing Libraries and Reading the Image

```python
import os.path
from skimage.io import imread

# Reading the astronaut image
img = imread(os.path.join('assets', 'astronaut.png'))
print(img)
```

- **`import os.path`**: This imports the `os.path` module, which provides functions for interacting with the file system.
- **`from skimage.io import imread`**: This imports the `imread` function from the `skimage.io` module, which is used to read images.
- **`imread(os.path.join('assets', 'astronaut.png'))`**: This reads the image file located at `'assets/astronaut.png'` and stores it in the variable `img`.
- **`print(img)`**: This prints the array representation of the image.

### Visualizing the Image

```python
import matplotlib.pyplot as plt

# Using matplotlib to visualize the image
plt.imshow(img)
plt.axis('on')  # Show axes for better visualization
plt.show()  # Display the plot
```

- **`import matplotlib.pyplot as plt`**: This imports the `pyplot` module from `matplotlib`, which is used for plotting and visualizing data.
- **`plt.imshow(img)`**: This displays the image stored in `img`.
- **`plt.axis('on')`**: This ensures that the axes are shown (you can use `'off'` to hide them).
- **`plt.show()`**: This displays the plot.

### Image Properties

```python
print('Type of image: ', type(img))
print('Dimensions of image: ', img.ndim)
print('Shape of image:', img.shape)
```

- **`type(img)`**: This prints the type of the image object, which is typically a NumPy array.
- **`img.ndim`**: This prints the number of dimensions of the image array.
- **`img.shape`**: This prints the shape of the image array, which gives the dimensions (height, width, and number of color channels).

### Slicing Out the Rocket

```python
# Slicing out the rocket
img_slice = img.copy()
img_slice = img_slice[0:300, 360:480]
plt.figure()
plt.imshow(img_slice)
plt.show()
```

- **`img.copy()`**: This creates a copy of the image array to avoid modifying the original image.
- **`img_slice[0:300, 360:480]`**: This slices out a portion of the image from rows 0 to 299 and columns 360 to 479. This portion presumably contains the rocket.
- **`plt.figure()`**: This creates a new figure for plotting.
- **`plt.imshow(img_slice)`**: This displays the sliced portion of the image.
- **`plt.show()`**: This displays the plot.

### Modifying and Displaying the Sliced Image

```python
img[0:300, 360:480, :] = 0
img_slice = img.copy()
img_slice = img_slice[0:300, 360:480, :]
plt.imshow(img_slice)
plt.show()
```

- **`img[0:300, 360:480, :] = 0`**: This sets the pixel values in the specified slice (rows 0 to 299, columns 360 to 479, and all color channels) to 0, effectively blacking out that portion of the image.
- **`img_slice = img.copy()`**: This creates another copy of the modified image.
- **`img_slice[0:300, 360:480, :]`**: This slices out the same portion of the image again.
- **`plt.imshow(img_slice)`**: This displays the newly sliced portion of the image.
- **`plt.show()`**: This displays the plot.

