# 704. Binary Search

## Java Solution

```java
class Solution {
    public int search(int[] nums, int target) {
        int l =0, r=nums.length-1;
        while(l<=r){
            int mid = l + (r-l)/2;
            if(nums[mid]>target){
                r = mid - 1;
            } else if(nums[mid]<target){
                l = mid + 1;
            } else {
                return mid;
            }
        }
        return -1;
    }
}
```
# JavaScript Solution

```js
function search(nums, target) {
    let l = 0, r = nums.length - 1;
    while (l <= r) {
        let mid = l + Math.floor((r - l) / 2);
        if (nums[mid] > target) {
            r = mid - 1;
        } else if (nums[mid] < target) {
            l = mid + 1;
        } else {
            return mid;
        }
    }
    return -1;
}
```

# C++ Solution 

```c++
class Solution {
public:
    int search(vector<int>& nums, int target) {
        int l = 0, r = nums.size() - 1;
        while (l <= r) {
            int mid = l + (r - l) / 2;
            if (nums[mid] > target) {
                r = mid - 1;
            } else if (nums[mid] < target) {
                l = mid + 1;
            } else {
                return mid;
            }
        }
        return -1;
    }
};
```

# Python Solution 

```python
class Solution:
    def search(self, nums, target):
        l, r = 0, len(nums) - 1
        while l <= r:
            mid = l + (r - l) // 2
            if nums[mid] > target:
                r = mid - 1
            elif nums[mid] < target:
                l = mid + 1
            else:
                return mid
        return -1
```
