# 1145. Number of Submatrices That Sum to Target
  
<br>**Problem:** https://leetcode.com/problems/number-of-submatrices-that-sum-to-target/<br>

**Difficulty:** Hard<br>
**Topics:** Array, Hash Table, Matrix, Prefix Sum<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-18 13:46 local time

**Runtime:** 641 ms (beats 14.286699999999957%)
**Memory:** 13 MB (beats 71.4286%)


<!-- leetgit:submissionId=2145533018 codeHash=4deca80bebc464287ac398e8398727eaf4a9c8ed6103f60f5bd4ed0512bf5826 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
        def numSubmatrixSumTarget(self, A, target):
            m, n = len(A), len(A[0])
            for row in A:
                for i in xrange(n - 1):
                    row[i + 1] += row[i]
            res = 0
            for i in xrange(n):
                for j in xrange(i, n):
                    c = collections.defaultdict(int)
                    cur, c[0] = 0, 1
                    for k in xrange(m):
                        cur += A[k][j] - (A[k][i - 1] if i > 0 else 0)
                        res += c[cur - target]
                        c[cur] += 1
            return res
        
```
