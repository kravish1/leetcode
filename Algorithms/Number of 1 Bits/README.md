# [Number of 1 Bits](https://leetcode.com/problems/number-of-1-bits/)
###### No:`191`
###### Difficulty:`Easy`
#### Solution 1
```js
/**
 * @param {number} n - a positive integer
 * @return {number}
 */
var hammingWeight = function(n) {
  var count = 0;
  while (n) {
    n = n & (n - 1);
    count++;
  }
  
  return count;
};
```
#### Solution 2
```javascript
/**
 * @param {number} n - a positive integer
 * @return {number}
 */
var hammingWeight = function(n) {
    var ret = 0;
    const base = 2;
    const bitnum = 32;
    var power = bitnum -1;

    for(var i = 0; i < bitnum; i++) {
        if(n >= Math.pow(base, power)) {
            ret++;
            n -= Math.pow(base, power);
        }
        power--;
    }

    return ret;
};

```
