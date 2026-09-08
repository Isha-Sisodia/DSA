https://www.geeksforgeeks.org/problems/max-consecutive-one/1
https://takeuforward.org/plus/dsa/problems/maximum-consecutive-ones?source=strivers-a2z-dsa-track

GFG Solution is - 
```python
class Solution:
    def maxConsecBits(self, arr):
        ans = 0
        count_0 = 0
        count_1 = 0
        max_count_0 = 0
        max_count_1 = 0
        n = len(arr)
        # Count longest Streak of 0
        for i in range(n):
            if arr[i] == 0:
                count_0 += 1
                max_count_0 = max(count_0, max_count_0)
            else:
                count_0 = 0
        # Count longest Streak of 1 #This is TUF Question 
        for i in range(n):
            if arr[i] == 1:
                count_1 += 1
                max_count_1 = max(count_1, max_count_1)
            else:
                count_1 = 0
        ans = max(max_count_0, max_count_1)
        return ans
```
TUF Solution is - 
```python
arr = [1, 1, 2, 1, 1, 1, 2]

count = 0
max_count = 0

for x in arr:
    if x == 1:
        count += 1
        max_count = max(max_count, count)
    else:
        count = 0
    #max_count = max(max_count, count)      #we can write this here also

print(max_count)   # 3
```
        
        
