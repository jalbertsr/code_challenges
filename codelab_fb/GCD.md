## GCD
#### Javascript
#### 16 min

Given 2 non negative integers m and n, find gcd(m, n)

GCD of 2 integers m and n is defined as the greatest integer g such that g is a divisor of both m and n.
Both m and n fit in a 32 bit signed integer.

My solution:

```javascript
module.exports = { 
//param A : integer
//param B : integer
//return an integer
  gcd : function(A, B){
    if(B !== 0) {
      return this.gcd(B, A%B);
    }
    return A;
  }
};
```