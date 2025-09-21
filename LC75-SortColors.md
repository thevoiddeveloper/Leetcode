# 75. Sort Colors

## Java Solution

```java
class Solution {
    public void sortColors(int[] nums) {
        // Nums only contains 0, 1 or 2
        int[] counts = {0, 0, 0};

        // Count the quantity of each val in nums
        for (int num: nums) {
            counts[num]++;
        }

        // Fill each bucket in the original array
        int index=0;
        for(int i=0;i<3;i++){
            for(int j=0;j<counts[i];j++){
                nums[index++]=i;
            }
        }
    }
}
```

## JavaScript Solution

```js
class Solution {
    /**
     * @param {number[]} nums
     * @return {void} Do not return anything, modify nums in-place instead.
     */
    sortColors(nums) {
        const count = new Int32Array(3);
        for (let num of nums) {
            count[num]++;
        }

        let index = 0;
        for (let i = 0; i < 3; i++) {
            while (count[i]-- > 0) {
                nums[index++] = i;
            }
        }
    }
}
```

## Python Solution

```python
class Solution:
    def sortColors(self, nums: List[int]) -> None:
        """
        Do not return anything, modify nums in-place instead.
        """
        count = [0] * 3
        for num in nums:
            count[num] += 1

        index = 0
        for i in range(3):
            while count[i]:
                count[i] -= 1
                nums[index] = i
                index += 1
```

## C++ Solution 

```
class Solution {
public:
    void sortColors(vector<int>& nums) {
        vector<int> count(3);
        for (int& num : nums) {
            count[num]++;
        }

        int index = 0;
        for (int i = 0; i < 3; i++) {
            while (count[i]-- > 0) {
                nums[index++] = i;
            }
        }
    }
}
```
