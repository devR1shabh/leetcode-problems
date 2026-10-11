# 191. Number of 1 Bits

| Field | Value |
| --- | --- |
| **Difficulty** | Easy |
| **Topics** | Divide and Conquer, Bit Manipulation |
| **Folder** | `divide-and-conquer` |
| **Language** | C++ |
| **Runtime** | 0 ms (beats 100.00%) |
| **Memory** | 6.3 MB (beats 100.00%) |
| **Submitted** | 2024-01-09 |
| **Problem** | [number-of-1-bits](https://leetcode.com/problems/number-of-1-bits/) |
| **Submission** | [#1141396847](https://leetcode.com/submissions/detail/1141396847/) |

## Problem Statement

Given a positive integer `n`, write a function that returns the number of set bits in its binary representation (also known as the [Hamming weight](http://en.wikipedia.org/wiki/Hamming_weight)).

**Example 1:**

**Input:** n = 11

**Output:** 3

**Explanation:**

The input binary string **1011** has a total of three set bits.

**Example 2:**

**Input:** n = 128

**Output:** 1

**Explanation:**

The input binary string **10000000** has a total of one set bit.

**Example 3:**

**Input:** n = 2147483645

**Output:** 30

**Explanation:**

The input binary string **1111111111111111111111111111101** has a total of thirty set bits.

**Constraints:**

- `1 <= n <= 2^31 - 1`

**Follow up:** If this function is called many times, how would you optimize it?

## Solution

Accepted C++ solution: [`solution.cpp`](./solution.cpp)

```cpp
class Solution {
public:
    int hammingWeight(uint32_t n) {

        int count=0;

        while(n!=0)
        {
            if(n&1)
            {
                count++;
            }
            n=n>>1;
        }
        return count;
        
    }
};
```

## My Notes

<!-- my-notes:start -->
_Add your approach, complexity and pitfalls here. This section is preserved when the problem is re-synced._
<!-- my-notes:end -->
