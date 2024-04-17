# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Import the numpy module to use the built-in function.
2. Create a zero matrix for the solution by using np.zeros().
3. Find the ratios and form the row echelon form.
4. Using Back substitution, solve the matrix and display the solution.
5. End the program.

## Program:
```
Developed by: Kartikeyan P
RegisterNumber: 212223230102
```
```
import numpy as np
n=int(input())
matrix=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        matrix[i][j]=int(input())
for i in range(n):
    for j in range(i+1,n):
        ratio=matrix[j][i]/matrix[i][i]
        for k in range(n+1):
            matrix[j][k]=matrix[j][k]-ratio*matrix[i][k]
#BACK SUBSTIUTION
x[n-1]=matrix[n-1][n]/matrix[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=matrix[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-matrix[i][j]*x[j]
    x[i]=x[i]/matrix[i][i]
for i in range(n):
    print("X%d = %0.2f" %(i,x[i]),end=" ")
```
## Output:
![Screenshot 2024-04-17 114936](https://github.com/karthikeyanpachiyappan/Gaussian/assets/155143878/34c08ffb-e7cb-4ec2-99f1-ea2a73b04798)


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

