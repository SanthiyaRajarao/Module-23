# EX 5A Minimum Cost Path
## DATE: 25/03/25
## AIM:
To write a Python program using A Naive recursive implementation of Minimum Cost Path Problem.

## Algorithm

1. Initialize a table tc[R][C] with tc[0][0] = cost[0][0].
2. Fill first row and first column by accumulating cost from the left (for rows) and top (for columns).
3. For all other cells tc[i][j]
4. Iterate through the grid, row by row and column by column, applying the above step.
5. Return the value at tc[m][n], which is the minimum cost to reach cell `(m, n)`.

## Program:
```
/*
A program to implement to find the Minimum Cost Path Problem using a  Naive recursive Approach.

Developed by: SANTHIYA R
Register Number:  212223230192
*/
```
```
R = int(input())
C = int(input())
def minCost(cost, m, n):
 
    tc = [[0 for x in range(C)] for x in range(R)]
    tc[0][0] = cost[0][0]
    for i in range(1, m+1):
        tc[i][0] = tc[i-1][0] + cost[i][0]
    for j in range(1, n+1):
        tc[0][j] = tc[0][j-1] + cost[0][j]
    for i in range(1, m+1):
        for j in range(1, n+1):
            tc[i][j] = min(tc[i-1][j-1], tc[i-1][j], tc[i][j-1]) + cost[i][j]
    return tc[m][n]
 
# Driver program to test above functions
cost = [[1, 2, 3],
        [4, 8, 2],
        [1, 5, 3]]
print(minCost(cost, 2, 2))
```

## Output:
![image](https://github.com/user-attachments/assets/d48b725d-6edb-4519-8132-04227eba87c6)


## Result:
Thus the above program was executed successfully for finding the minimum cost.
