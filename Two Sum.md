---
Difficulty: Easy
Related Topics:
  "Array": https://leetcode.com/tag/array/
  "Hash Table": https://leetcode.com/tag/hash-table/
Similar Questions:
  "3Sum": https://leetcode.com/problems/3sum/
  "4Sum": https://leetcode.com/problems/4sum/
  "Two Sum II - Input array is sorted": https://leetcode.com/problems/two-sum-ii-input-array-is-sorted/
  "Two Sum III - Data structure design": https://leetcode.com/problems/two-sum-iii-data-structure-design/
  "Subarray Sum Equals K": https://leetcode.com/problems/subarray-sum-equals-k/
  "Two Sum IV - Input is a BST": https://leetcode.com/problems/two-sum-iv-input-is-a-bst/
  "Two Sum Less Than K": https://leetcode.com/problems/two-sum-less-than-k/
---

### Problem:

Given an array of integers `nums` and and integer `target`, return *the indices of the two numbers such that they add up to target*.

You may assume that each input would have **exactly one solution**, and you may not use the *same* element twice.

You can return the answer in any order.

**Example 1:**

```
Input: nums = [2,7,11,15], target = 9
Output: [0,1]
Output: Because nums[0] + nums[1] == 9, we return [0, 1]
```

**Example 2:**

```
Input: nums = [3,2,4], target = 6
Output: [1,2]
```

**Example 3:**

```
Input: nums = [3,3], target = 6
Output: [0,1]
```

**Constraints:**

- `1 <= nums.length <= 105`
- `-109 <= nums[i] <= 109`
- `-109 <= target <= 109`
- **Only one valid answer exists.**

### Solution:
```
/*
 * @param {number[]} nums
 * @param {number} target
 * @return {number[]}
*/
 
var twoSum = function(nums, target) {
    let keys = {};
    for (let i = 0 ; i<nums.length;i++){
        if(keys[target-nums[i]]!=null){
            return[keys[target-nums[i]],i];
        }
        keys[nums[i]] = i;    
    }
};
```


*Template generated via [Leetmark](https://github.com/crimx/crx-leetmark).*

