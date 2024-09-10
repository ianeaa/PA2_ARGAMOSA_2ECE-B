# EXPERIMENT 2 - Numerical Python

This is for my Programming Assignment 2 containing my codes for Experiment 2 - Numerical Python 

**1. Normalization Problem** - Normalization is one of the most basic preprocessing techniques in
data analytics. This involves centering and scaling process. Centering means subtracting the data from the
mean and scaling means dividing with its standard deviation. Mathematically, normalization can be
expressed as: 𝑍 = 𝑋 − 𝑥̅/𝜎 

In Python, element-wise mean and element-wise standard deviation can be obtained by using .mean() and
.std() calls.

In this problem, create a random 5 x 5 ndarray and store it to variable X. Normalize X. Save your normalized ndarray as *X_normalized.npy*

**2. Divisible by 3 Problem** - Create the following 10 x 10 ndarray which are the squares of the first 100 positive integers. From this ndarray, determine all the elements that are divisible by 3. Save the result as *div_by_3.npy*

# CODES

# *Normalization Problem*

```python
import numpy as np

# generate random numbers in a 5x5 array
random = np.random.random((5,5))

# set the random array to variable X
X = random

# perform the formula: Z = (X - mean) / standev
Z = (X - np.mean(X)) / np.std(X)

# output
print(Z)

# save as .npy
np.save('X_normalized', Z)
```


# *Divisible by 3 Problem*
```python
import numpy as np

# create a 10x10 matrix with the squares of the number and use arange function to limit it from 1-100
numbers = np.arange(1,101)
squared = numbers**2

# use reshape to make it into a 10x10 table
table = squared.reshape(10,10)

# print the table
print(table)


# use modulo to separate the numbers that are divisible by 3
three = table[table % 3 == 0]
print(" ")

# print
print("Numbers divisible by 3")
print(" ")
print(three)

# save as .npy 
np.save("div_by_3", three)
```
