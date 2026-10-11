# 242. Valid Anagram

| Field | Value |
| --- | --- |
| **Difficulty** | Easy |
| **Topics** | Hash Table, String, Sorting |
| **Folder** | `hashing` |
| **Language** | C++ |
| **Runtime** | 1 ms (beats 53.20%) |
| **Memory** | 9.8 MB (beats 24.84%) |
| **Submitted** | 2026-07-14 |
| **Problem** | [valid-anagram](https://leetcode.com/problems/valid-anagram/) |
| **Submission** | [#2067773928](https://leetcode.com/submissions/detail/2067773928/) |

## Problem Statement

Given two strings `s` and `t`, return `true` if `t` is an anagram of `s`, and `false` otherwise.

**Example 1:**

**Input:** s = "anagram", t = "nagaram"

**Output:** true

**Example 2:**

**Input:** s = "rat", t = "car"

**Output:** false

**Constraints:**

- `1 <= s.length, t.length <= 5 * 10^4`
- `s` and `t` consist of lowercase English letters.

**Follow up:** What if the inputs contain Unicode characters? How would you adapt your solution to such a case?

## Solution

Accepted C++ solution: [`solution.cpp`](./solution.cpp)

```cpp
class Solution {
public:
    bool isAnagram(string s, string t) {
        unordered_map<char,int> count;

        if(s.size() != t.size()){
            return false;
        }
        for(int i=0;i<s.size();i++){
            count[s[i]]++;
        }

        for(int i=0;i<t.size();i++){
            count[t[i]]--;
        }

        for(auto it:count){
            if(it.second != 0){
                return false;
            }
        }

        return true;
    }
};
```

## My Notes

<!-- my-notes:start -->
_Add your approach, complexity and pitfalls here. This section is preserved when the problem is re-synced._
<!-- my-notes:end -->
