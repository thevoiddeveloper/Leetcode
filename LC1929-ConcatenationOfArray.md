# Leetcode 1929 - Concatenation of Array

## Java Solution 
```java
class Solution {
    public int[] getConcatenation(int[] nums) {
        int n = nums.length;
        int[] ans = new int[2*n];
        for(int i=0; i<nums.length; i++){
            ans[i]=ans[i+n]=nums[i];
        }
        return ans;
    }
}
```

## JavaScript Solution
```js
function getConcatenation(nums) {
    const n = nums.length;
    const ans = new Array(2 * n);
    for (let i = 0; i < n; i++) {
        ans[i] = ans[i + n] = nums[i];
    }
    return ans;
}
```

## Python Solution
```python
def getConcatenation(nums):
    n = len(nums)
    ans = [0] * (2 * n)
    for i in range(n):
        ans[i] = ans[i + n] = nums[i]
    return ans
```

## C++ Solution
```c++
#include <vector>
using namespace std;

class Solution {
public:
    vector<int> getConcatenation(vector<int>& nums) {
        int n = nums.size();
        vector<int> ans(2 * n);
        for (int i = 0; i < n; ++i) {
            ans[i] = ans[i + n] = nums[i];
        }
        return ans;
    }
};
```
