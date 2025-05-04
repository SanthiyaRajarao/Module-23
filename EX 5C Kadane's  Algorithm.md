# EX 5C Kadane's Algorithm
## DATE: 06/04/25
## AIM:
To write a python program to find the maximum contiguous subarray.


## Algorithm

1. Initialize `max_sum = a[0]`, `curr_sum = 0`.
2. Loop through each element `x` in the array:
3. Add `x` to `curr_sum`.
4.If `curr_sum > max_sum`, update `max_sum`.
5.If `curr_sum < 0`, reset `curr_sum = 0`.

## Program:
```
/*
To implement the program to find the maximum contiguous subarray.


Developed by: SANTHIYA R
Register Number:  212223230192
*/
```
```
def maxSubArraySum(a,size):
    max_till_now=a[0]
    max_ending=0
    for i in range(0,size):
        max_ending = max_ending+a[i]
        if max_ending < 0:
            max_ending=0
        elif(max_till_now < max_ending):
            max_till_now=max_ending
    return max_till_now

n=int(input())
a=[]
for i in range(n):
    a.append(int(input()))
print("Maximum contiguous sum is", maxSubArraySum(a,n))

```
## Output:

![image](https://github.com/user-attachments/assets/fb66d52b-b719-417b-8ac6-148414d1cb77)


## Result:
Thus the program was executed successfully for finding the maximum contiguous sum of subarray..
