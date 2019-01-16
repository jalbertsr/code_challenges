## NUM1BITS
#### Python
#### 8 min

Write a function that takes an unsigned integer and returns the number of 1 bits it has.

Example:

The 32-bit integer 11 has binary representation
```python
00000000000000000000000000001011
```
so the function should return 3.

_Note that since Java does not have unsigned int, use long for Java_



My solution:

```python
from collections import Counter
class Solution:
    # @param A : integer
    # @return an integer
    def numSetBits(self, A):
         return Counter('{0:b}'.format(A))['1']

```