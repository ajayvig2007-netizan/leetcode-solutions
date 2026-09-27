# 1644. Maximum Number of Non-Overlapping Substrings
  
<br>**Problem:** https://leetcode.com/problems/maximum-number-of-non-overlapping-substrings/<br>

**Difficulty:** Hard<br>
**Topics:** Hash Table, String, Greedy, Sorting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-18 11:28 local time

**Runtime:** 384 ms (beats 64.86490000000006%)
**Memory:** 16.7 MB (beats 24.324400000000004%)


<!-- leetgit:submissionId=2145422439 codeHash=fed8bb802a73cc9504455a2195898ed9d2609c71e092c2c92830cc6058d583b6 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution:
    def maxNumOfSubstrings(self, s):
        n = len(s)

        first = [n] * 26
        last = [-1] * 26

        # Find first and last occurrence of every character
        for i in range(n):
            ch = ord(s[i]) - ord('a')

            if first[ch] == n:
                first[ch] = i

            last[ch] = i

        intervals = []

        # Build valid intervals
        for ch in range(26):
            if last[ch] == -1:
                continue

            start = first[ch]
            end = last[ch]

            valid = True
            i = start

            # Keep checking even when end gets expanded
            while i <= end:
                current = ord(s[i]) - ord('a')

                # This character has an occurrence before start
                if first[current] < start:
                    valid = False
                    break

                # Include all occurrences of this character
                end = max(end, last[current])

                i += 1

            if valid:
                intervals.append((start, end))

        # Sort by ending position
        intervals.sort(key=lambda x: (x[1], x[1] - x[0]))

        answer = []
        previous_end = -1

        # Greedily choose non-overlapping intervals
        for start, end in intervals:
            if start > previous_end:
                answer.append(s[start:end + 1])
                previous_end = end

        return answer
        
```
