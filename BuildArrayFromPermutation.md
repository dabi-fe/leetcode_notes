# Leetcode 1920. Build Array from Permutation

## Problem: 
Given a 0-indexed integer array nums which is a permutation of the first n natural numbers, return an array ans of the same length as nums such that ans[i] = nums[nums[i]] for each 0 <= i < nums.length and return ans.

A permutation of first n natural numbers is an array of length n where each integer from 1 to n appears exactly once.

## Examples:

```
Input: nums = [0,2,1,5,3,4]
Output: [0,1,2,4,5,3]
```

```
Input: nums = [5,0,1,2,3,4]
Output: [4,5,0,1,2,3]
```


## Constraints:

- 1 <= nums.length <= 1000
- 0 <= nums[i] < nums.length
- The elements in nums are distinct.

## Approach:
To Approach this problem we need to know a few things:
- The input array will be an array of integers.
- The output array will be an array of integers.
- The output array will be `ans` and will be the same length as the input array.

### Steps: `Python` and `Java`

**First create an empty array called `ans`.**

**Python**
```python
ans = []
```

**Java**
```java
int[] ans = new int[nums.length];
```

Then we need to iterate through the input array and for each element we need to add the value of the element at the index of the current element to the `ans` array.

**Python**
```python
for i in range(len(nums)):
    ans.append(nums[nums[i]])
```

**Java**
```java
for (int i = 0; i < nums.length; i++) {
    ans[i] = nums[nums[i]];
}
```


Finally we need to return the `ans` array.

**Python**
```python
return ans
```

**Java**
```java
return ans;
```


## Time and Space Complexity:
Time Complexity: $O(n)$ \
Space Complexity: $O(n)$


## Code:

**Python**
```python
class Solution:
    def buildArray(self, nums: List[int]) -> List[int]:
        ans = []
        for i in range(len(nums)):
            ans.append(nums[nums[i]])
        return ans
```

**Java**
```java
class Solution {
    public int[] buildArray(int[] nums) {
        int[] ans = new int[nums.length]; // Create an array of the same length as nums
        for (int i = 0; i < nums.length; i++) {
            ans[i] = nums[nums[i]]; // Add the value of the element at the index of the current element to the ans array
        }
        return ans;
    }
}
``` 
