# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. 
2. 
3. 
4. 

## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: monesh s 
RegisterNumber: 212225040256<img width="1223" height="471" alt="Screenshot 2026-06-02 180806" src="https://github.com/user-attachments/assets/efd14e0d-2cc8-423c-bffc-03ba6ba12f73" />

*/

import os
os.environ["OPENBLAS_NUM_THREADS"]="1"
import numpy as np
n = int(input())

a = []
for i in range(n):
    row = []
    for j in range(n + 1):
        row.append(float(input()))
    a.append(row)


for k in range(n - 1):
    for i in range(k + 1, n):
        factor = a[i][k] / a[k][k]
        for j in range(k, n + 1):
            a[i][j] -= factor * a[k][j]

x = [0] * n
x[n - 1] = a[n - 1][n] / a[n - 1][n - 1]

for i in range(n - 2, -1, -1):
    s = 0
    for j in range(i + 1, n):
        s += a[i][j] * x[j]
    x[i] = (a[i][n] - s) / a[i][i]

for i in range(n):
    print(f"X{i} = {x[i]:.2f}", end=" ")
```

## Output:
<img width="1223" height="471" alt="Screenshot 2026-06-02 180806" src="https://github.com/user-attachments/assets/615d7fa1-3611-40e9-9f7f-8195e69419e7" />



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

