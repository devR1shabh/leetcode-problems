# 217. Contains Duplicate

| Field | Value |
| --- | --- |
| **Difficulty** | Easy |
| **Topics** | Array, Hash Table, Sorting |
| **Folder** | `arrays` |
| **Language** | C++ |
| **Runtime** | 83 ms (beats 21.74%) |
| **Memory** | 111.5 MB (beats 28.98%) |
| **Submitted** | 2026-07-14 |
| **Problem** | [contains-duplicate](https://leetcode.com/problems/contains-duplicate/) |
| **Submission** | [#2067681841](https://leetcode.com/submissions/detail/2067681841/) |

## Problem Statement

Given an integer array `nums`, return `true` if any value appears **at least twice** in the array, and return `false` if every element is distinct.

**Example 1:**

**Input:** nums = \[1,2,3,1\]

**Output:** true

**Explanation:**

The element 1 occurs at the indices 0 and 3.

**Example 2:**

**Input:** nums = \[1,2,3,4\]

**Output:** false

**Explanation:**

All elements are distinct.

**Example 3:**

**Input:** nums = \[1,1,1,3,3,4,3,2,4,2\]

**Output:** true

**Constraints:**

- `1 <= nums.length <= 10^5`
- `-10^9 <= nums[i] <= 10^9`

## Solution

Accepted C++ solution: [`solution.cpp`](./solution.cpp)

```cpp
class Solution {
public:
    bool containsDuplicate(vector<int>& nums) {
        unordered_map<int,int> count;

       for(int i=0;i<nums.size();i++){
        count[nums[i]]++;

        if(count[nums[i]] > 1){
            return true;
        }
       } 

       return false;
    }
};
```

## My Notes

<!-- my-notes:start -->
_Add your approach, complexity and pitfalls here. This section is preserved when the problem is re-synced._
<!-- my-notes:end -->
