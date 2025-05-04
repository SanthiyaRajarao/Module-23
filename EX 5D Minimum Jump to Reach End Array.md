# EX 5D Minimum Jump to Reach End Array
## DATE: 06/04/25
## AIM:
To write a python program for finding the minimum number of jumps needed to reach end of the array using Dynamic Programming.


## Algorithm

1. If start == end, return 0 (no jump needed).
2. If current element is 0, return infinity (can’t move forward).
3. Initialize `min_jumps = ∞`.
4. For all reachable indices from current position
5. Return `min_jumps + 1 for the current step.

## Program:
```
/*
To implement the program to finding the minimum number of jumps needed to reach end of the array.
Developed by: SANTHIYA R
Register Number:  212223230192
*/
```
```
def minJumps(arr, l, h):
    if (h==l):
        return 0
    if (arr[l] ==0):
        return float('inf')
    min =float('inf')
    for i in range(l+1, h+1):
        if(i<l+arr[l]+1):
            jumps = minJumps(arr,i,h)
            if(jumps!=float('inf') and jumps +1 <min):
                min = jumps+1
    return min
arr = []
n = int(input()) 
for i in range(n):
    arr.append(int(input()))
print('Minimum number of jumps to reach','end is', minJumps(arr, 0, n-1))
 
```
## Output:

![image](https://github.com/user-attachments/assets/bd5a2ad9-d008-40f2-87f3-96b8b8597b68)


## Result:
Thus the program was executed successfully for finding the minimum number of jumps to reach end.
