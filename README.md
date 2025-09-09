# Programming-Assignment-2

A Programming Assignment of Shinade T. Cancino from 2ECEC for her class, Advanced Computer Programming. 

# About the Code

## Problem 1: Normalization Problem
  ####   The task is to create a 5x5 NumPy array filled with random numbers, then normalize its values using the formula: 
  
    Z = X - x̄ / σ
      where:
       X = original data
       x̄ = mean of the data
       σ = standard deviation 
       
  ####   After normalization, the resulting array will have a mean of 0 and a standard deviation of 1. Finally, the normalized array must be saved as a .npy file named X_normalized.npy for future use.

| Step | Code | Purpose |
|------|------|---------|
|Import NumPy| import numpy as np | Use NumPy functions|
|Create array| np.random.rand(5,5)| Generate random numbers|
|Calculate mean| X.mean()| Get average value|
|Calculate std| X.std()| Get spread of data|
|Normalize| (X-mean)/std|Transform values to mean=0, std=1|
|Save file|np.save("X_normalized.npy", X_normalized)|Store normalized array|
|Load file| np.load("X_normalized.npy")| Retrieve saved data|

## Problem 2: Divisible by 3
  #### This program generates a 10×10 NumPy array containing the squares of the first 100 positive integers. It then identifies all numbers that are divisible by 3 using a modulo operation and saves the result in a .npy file named div_by_3.npy.

| Step | Code | Description |
|------|------|---------|
| Import NumPy| import numpy as np |  To use NumPy functions|
| Create a 10x10 array| A = np.arange(1,101) ** 2 | Generate the squares of numbers 1-100|
| Reshape array| A = A.reshape(10,10) | Reshapes them into a 10x10 matrix |
| Display the array| print("10x10 Array A:", A)| Prints the generated 10x10 array|
| Find numbers divisible by 3| div_by_3 = A[A%3==0] |Filters out all numbers divisible by 3|
| Display divisible numbers| print("Elements Divisible by 3:", div_by_3) | Shows all numbers that are divisible by 3|
| Save result to file| np.save("div_by_3.npy", div_by_3)| Saves the filters numbers into a NumPy file .npy|
| Verify saved file| loaded = np.loaded("div_by_3.npy")| Loads the saved file to confirm tha the correct numbers were stored|

    Example Output:
    Elements Divisible by 3:
    [ 9 36 81 144 225 324 441 576 729 900 1089 1296 1521 1764 
    2025 2304 2601 2916 3249 3600 3969 4356 4761 5184 5625 6084 6561 7056 
    7569 8100 8649 9216 9801]
    


