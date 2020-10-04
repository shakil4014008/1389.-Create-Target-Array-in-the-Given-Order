# 1389.-Create-Target-Array-in-the-Given-Order
Given two arrays of integers nums and index. Your task is to create target array under the following rules:

Initially target array is empty.
From left to right read nums[i] and index[i], insert at index index[i] the value nums[i] in target array.
Repeat the previous step until there are no elements to read in nums and index.
Return the target array.

It is guaranteed that the insertion operations will be valid.

 idea: insert method in c#

```c#


public class Solution {
    public int[] CreateTargetArray(int[] nums, int[] index) {
         
        List<int> res = new List<int>();
        
        int i=0;
        while(i<nums.Length){
            res.Insert(index[i], nums[i]);
            i++;
        }
        
        return res.ToArray();
        
    }
}

```
