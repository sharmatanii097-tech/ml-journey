# NumPy Notes

## What is NumPy?
Numerical Python - a library for fast math operations on large data.

## Why use NumPy?
- Normal Python lists are slow for math
- NumPy arrays are 50x faster
- All ML libraries use NumPy under the hood
- Images, datasets, neural networks = all NumPy arrays

## Key Concept
NumPy Array = like a Python list but:
- Much faster
- Can do math on entire array at once
- Can be multi-dimensional (1D, 2D, 3D)

## Real Life Example
1000 student marks → find average
Normal Python = 10 lines of code
NumPy = 1 line of code


# NumPy Complete Notes

## What is a Library?
Ready made tools someone else built so we don't start from scratch.
Example: np.mean() instead of writing average calculation ourselves.

## What is import?
Brings the library into our program so we can use it.
Without import = library exists but we cannot use it.

## Why as np?
Short nickname for numpy. Everyone in the world uses np.
Saves typing numpy every single time.

## What is version?
Which generation/update of NumPy is installed.
np.__version__ tells us this.

## Why NumPy?
- 50x faster than normal Python for math
- Processes entire arrays at once (vectorization)
- All ML libraries built on top of NumPy
- Images = numbers, datasets = numbers, NumPy handles them all

## What happens when we run import numpy as np?
1. Python finds NumPy on computer
2. Loads it into RAM
3. Creates nickname 'np' for it
4. Now we can use np.anything



## NumPy Speed vs Normal Python

NumPy is 50x faster because:
- Normal Python = processes numbers ONE BY ONE
- NumPy = processes ALL numbers AT SAME TIME
- Called Vectorization
- Uses computer processor's special math units (SIMD)

Why this matters in ML:
- Neural networks = millions of math operations
- Without NumPy speed = training takes weeks
- With NumPy = training takes hours

import time → library to measure speed
time.time() → snapshot of current time
end - start → how long code took



## Array Properties

### shape
- Tells how array is organised
- (5,) = 1D array with 5 elements
- (2,3) = 2D array with 2 rows 3 columns
- Most important property in ML!

### ndim
- Number of dimensions
- 1 = single row
- 2 = table with rows and columns
- 3 = multiple tables stacked (like images)

### size
- Total number of elements
- (2,3) array → size = 6 (2×3)

### dtype
- Type of numbers stored
- int64 = whole numbers
- float64 = decimal numbers
- bool = True or False
- Always convert to float64 before feeding to ML model!

### How to convert dtype
a.astype(float) → converts to float64

## Common Mistake
Feeding int64 data to ML model → can cause errors
Always convert: data = data.astype(float)



1. Image shape = (height, width, channels)
   NOT (channels, channels)

2. Both astype(float) and direct 1.0 give float64

3. NumPy arrays = ONE data type only
   Mixed types → NumPy converts all to text

4. == works in NumPy
   .equals() is Pandas thing




## Common Mistakes to Remember

1. Image shape = (height, width, color_channels)
   Example: 224×224 RGB image = (224, 224, 3)

2. MNIST dataset shape = (num_images, 28, 28)
   Example: 1000 images = (1000, 28, 28)

3. NumPy arrays store ONE type only
   Mixed types → all converted to text/string

4. NumPy uses == for comparison
   Pandas uses .equals()

5. Two ways to get float64:
   Way 1: a.astype(float)
   Way 2: np.array([1.0, 2.0, 3.0])



   1. Color image dataset shape = (samples, height, width, 3)
   Black/white dataset shape = (samples, height, width)

2. All rows must have same length in 2D array!
   Different lengths = object dtype, not numeric

3. Mixed types in NumPy = no error
   BUT converts everything to string
   DANGEROUS for ML!

4. To compare array sizes always use .shape
   Never use .ndim for comparison

5. (3,4) and (4,3) = different shape, same size, same ndim



## Important Things Learned from Quiz

### Mixed types in NumPy
np.array([1, 2, 3, "hello"])
→ No error! Converts all to string!
→ dtype becomes string
→ Dangerous in ML - always check dtype!

### Unequal row lengths
np.array([[1,2,3],[4,5]])
→ Rows have different lengths
→ Creates object dtype array
→ Cannot do math on it
→ Always make rows equal length!

### Shape vs ndim for comparison
→ Always compare .shape not .ndim
→ (3,4) and (4,3) have same ndim but different shape!

### Color image dataset shape
→ (num_images, height, width, 3)
→ 3 = RGB channels
→ Black/white = (num_images, height, width)

### Neural network input
→ Shape (100, 784) means:
→ 100 images in one batch
→ 784 = 28×28 pixels flattened