# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Start the program
2. Write the code appropriately
3. Check the code
4. Run the program.

## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: TAMIZHSELVAN B
RegisterNumber: 23013460
*/
import numpy as np
n=int(input())
arr=np.zeros((n,n+1))
res=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        arr[i][j] = int(input())
for i in range(n):
    for j in range(i+1,n):
        ratio=arr[j][i]/arr[i][i]
        for k in range(n+1):
            arr[j][k]=arr[j][k]-ratio*arr[i][k]
res[n-1] = arr[n-1][n]/arr[n-1][n-1]
for i in range(n-2,-1,-1):
    res[i]=arr[i][n]
    for j in range(i+1,n):
        res[i] = res[i]-arr[i][j]*res[j]
    res[i]=res[i]/arr[i][i]
for i in range(n):
    print("X%d = %0.2f"%(i,res[i]),end=" ")

```

## Output:
![GUSSIAN Output](https://github.com/tamizhselvan23013460/Gaussian/assets/150231370/f4b7c0a0-ad64-4089-89ec-9f293f41fdc2)



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

