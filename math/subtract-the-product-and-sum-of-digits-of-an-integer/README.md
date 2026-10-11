# 1281. Subtract the Product and Sum of Digits of an Integer

| Field | Value |
| --- | --- |
| **Difficulty** | Easy |
| **Topics** | Math |
| **Folder** | `math` |
| **Language** | C++ |
| **Runtime** | 0 ms (beats 100.00%) |
| **Memory** | 6.5 MB (beats 100.00%) |
| **Submitted** | 2024-01-09 |
| **Problem** | [subtract-the-product-and-sum-of-digits-of-an-integer](https://leetcode.com/problems/subtract-the-product-and-sum-of-digits-of-an-integer/) |
| **Submission** | [#1141387364](https://leetcode.com/submissions/detail/1141387364/) |

## Problem Statement

Given an integer number `n`, return the difference between the product of its digits and the sum of its digits.

**Example 1:**

```
Input: n = 234
Output: 15
Explanation:
Product of digits = 2 * 3 * 4 = 24
Sum of digits = 2 + 3 + 4 = 9
Result = 24 - 9 = 15
```

**Example 2:**

```
Input: n = 4421
Output: 21
Explanation:
Product of digits = 4 * 4 * 2 * 1 = 32
Sum of digits = 4 + 4 + 2 + 1 = 11
Result = 32 - 11 = 21
```

**Constraints:**

- `1 <= n <= 10^5`

## Solution

Accepted C++ solution: [`solution.cpp`](./solution.cpp)

```cpp
class Solution {
public:
    int subtractProductAndSum(int n) 
    {

        int prod=1,sum=0;

        while(n>0)
        {
            int dig=n%10;
            prod=prod*dig;
            sum=sum+dig;
            n=n/10;

        }

        int ans = prod-sum;
        return ans;
        
    }
};
```

## My Notes

<!-- my-notes:start -->
_Add your approach, complexity and pitfalls here. This section is preserved when the problem is re-synced._
<!-- my-notes:end -->
