# 1929. Concatenation of Array

| Field | Value |
| --- | --- |
| **Difficulty** | Easy |
| **Topics** | Array, Simulation |
| **Folder** | `arrays` |
| **Language** | C++ |
| **Runtime** | 0 ms (beats 100.00%) |
| **Memory** | 16.8 MB (beats 60.59%) |
| **Submitted** | 2026-07-13 |
| **Problem** | [concatenation-of-array](https://leetcode.com/problems/concatenation-of-array/) |
| **Submission** | [#2066490871](https://leetcode.com/submissions/detail/2066490871/) |

## Problem Statement

Given an integer array `nums` of length `n`, you want to create an array `ans` of length `2n` where `ans[i] == nums[i]` and `ans[i + n] == nums[i]` for `0 <= i < n` (**0-indexed**).

Specifically, `ans` is the **concatenation** of two `nums` arrays.

Return *the array* `ans`.

**Example 1:**

```
Input: nums = [1,2,1]
Output: [1,2,1,1,2,1]
Explanation: The array ans is formed as follows:
- ans = [nums[0],nums[1],nums[2],nums[0],nums[1],nums[2]]
- ans = [1,2,1,1,2,1]
```

**Example 2:**

```
Input: nums = [1,3,2,1]
Output: [1,3,2,1,1,3,2,1]
Explanation: The array ans is formed as follows:
- ans = [nums[0],nums[1],nums[2],nums[3],nums[0],nums[1],nums[2],nums[3]]
- ans = [1,3,2,1,1,3,2,1]
```

**Constraints:**

- `n == nums.length`
- `1 <= n <= 1000`
- `1 <= nums[i] <= 1000`

## Solution

Accepted C++ solution: [`solution.cpp`](./solution.cpp)

```cpp
class Solution {
public:
    vector<int> getConcatenation(vector<int>& nums) {
        int n = nums.size();
        vector<int> ans(2*n);
        for(int i=0 ; i<2*n ; i++){
            ans[i] = nums[(i+n) % n];
        }

        return ans;
    }
};
```

## My Notes

<!-- my-notes:start -->
_Add your approach, complexity and pitfalls here. This section is preserved when the problem is re-synced._
<!-- my-notes:end -->
