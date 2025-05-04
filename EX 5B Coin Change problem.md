# EX 5B Coin Change Problem
## DATE: 06/04/25
## AIM:
To compute the fewest number of coins that we need to make up the amount given.


## Algorithm

1. Create a table `dp[n+1]`, initialize `dp[0] = 1`.
2. For each coin in the list:
3. For each amount `i` from coin to `n`:
4. Update `dp[i] += dp[i - coin]`
5. Return `dp[n]` as the total number of ways.

## Program:
```
/*
Create a python function to compute the fewest number of coins that we need to make up the amount given.

.
Developed by: SANTHIYA R
Register Number:  212223230192
*/
```
```
def count(S, m, n):
    table = [[0 for x in range(m)] for x in range(n+1)]
    for i in range(m):
        table[0][i] = 1
    for i in range(1, n+1):
        for j in range(m):
            x = table[i - S[j]][j] if i - S[j] >= 0 else 0
            y = table[i][j - 1] if j >= 1 else 0
            table[i][j] = x + y
    return table[n][m - 1]
 
arr = []      
m = int(input())
n = int(input())
for i in range(m):
    arr.append(int(input()))
print(count(arr, m, n))
```
## Output:

![image](https://github.com/user-attachments/assets/4012e29a-482b-4eaf-a5cc-55aec89e2128)


## Result:
Thus the program was executed successfully for finding the minimum number of coins required to make amount.
