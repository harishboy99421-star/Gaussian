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

```
/*
'''Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by: Harish N
RegisterNumber: 212225220037

```
import os
os.environ["OPENBLAS_NUM_THREADS"]="1"
import numpy as np
import sys

n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
for i in range(n):
    if a[i][i]==0.0:
        sys.exit('Divide by Zero detected!')
    for j in range(i+1,n):
        ratio=a[j][i]/a[i][i]
        for k in range(n+1):
            a[j][k]=a[j][k]-ratio * a[i][k]
x[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]
    x[i]=x[i]/a[i][i]
for i in range(n):
    print('X%d = %0.2f' %(i,x[i]), end=' ')
*/
```

## Output:
<img width="1276" height="786" alt="image" src="https://github.com/user-attachments/assets/6c3439ad-d3fd-4f16-9852-dc1e3f0fd431" />



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

