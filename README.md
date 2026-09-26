# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
## 1Import the required libraries such as NumPy. 
## 2.Create the coefficient matrix and constant matrix using NumPy arrays. 
## 3.Apply Gaussian Elimination to convert the matrix into row echelon form and solve the equations.
## 4.Display the solution of the system of equations.
## Program:
```
Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by: Harish N
RegisterNumber: 212225220037

import os
import sys
os.environ["OPENBLAS_NUM_THREADS"] = "1"

import numpy as np

n = int(input())

a = np.zeros((n, n + 1))

for i in range(n):
    for j in range(n + 1):
        a[i][j] = float(input())

for i in range(n):
    if a[i][i] == 0:
        sys.exit("Divide by zero detected")

    for j in range(i + 1, n):
        ratio = a[j][i] / a[i][i]

        for k in range(n + 1):
            a[j][k] = a[j][k] - ratio * a[i][k]

x = np.zeros(n)

for i in range(n - 1, -1, -1):
    x[i] = a[i][n]

    for j in range(i + 1, n):
        x[i] = x[i] - a[i][j] * x[j]

    x[i] = x[i] / a[i][i]

for i in range(n):
    print(f"X{i} = {x[i]:.2f}", end=" ")

```
'''Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by:HARISH N 
RegisterNumber:212225220037 
'''


## Output:

<img width="1340" height="857" alt="Screenshot 2026-08-24 201135" src="https://github.com/user-attachments/assets/5c1d04dc-9dd2-4a16-985a-23a8a901eb6b" />




## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

