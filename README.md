# 1389.-Create-Target-Array-in-the-Given-Order
Given two arrays of integers, nums and index. Your task is to create a target array under the following rules:

Initially, the target array is empty.
From left to right, read nums[i] and index[i], insert at index index[i] the value nums[i] in the target array.
Repeat the previous step until there are no elements to read in nums and index.
Return the target array.

It is guaranteed that the insertion operations will be valid.

 

```py

class Solution:
    def restoreString(self, s: str, indices: List[int]) -> str:
        p = [0] * len(s)  # it is used only bounded array
        for i, n in zip(indices, s):
            p[i] = n
        return ''.join(p)   # join used when p is an array

```
