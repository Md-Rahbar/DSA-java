## Medium
- [Find First and Last Position of Element in Sorted Array](https://leetcode.com/problems/find-first-and-last-position-of-element-in-sorted-array/)
    ```
    public int[] searchRange(int[] nums, int target) {
        int[] res = { -1, -1 };
        int start = binarySearch(nums, target, true);
        int end = binarySearch(nums, target, false);
        res[0] = start;
        res[1] = end;
        return res;
    }

    public int binarySearch(int[] nums, int target, boolean findFirstIndex) {
        int start = 0, end = nums.length - 1;
        int res = -1;
        while (start <= end) {
            int mid = start + (end - start) / 2;
            if (nums[mid] > target) {
                end = mid - 1;
            } else if (nums[mid] < target) {
                start = mid + 1;
            } else {
                res = mid;
                if (findFirstIndex == true) {
                    end = mid - 1;
                } else {
                    start = mid + 1;
                }
            }
        }
        return res;
    }
    ```
- [Single Element in a Sorted Array](https://leetcode.com/problems/single-element-in-a-sorted-array/)
    ```
    public int singleNonDuplicate(int[] nums) {
        int low=0,high=nums.length-1;
        while(low<high){
            int mid=low+(high-low)/2;
            if(mid%2 == 1){
                mid--;
            }
            if(nums[mid]==nums[mid+1]){
                low=mid+2;
            }else{
                high=mid;
            }
        }
        return nums[low];
    }
    ```
- [Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/)
    ```
    public int search(int[] nums, int target) {
        for(int i=0;i<nums.length;i++){
            if(nums[i]==target){
                return i;
            }
        }
        return -1;
    }
    ```
- [Search in Rotated Sorted Array II](https://leetcode.com/problems/search-in-rotated-sorted-array-ii/)
    ```
    
    ```
- [Find Minimum in Rotated Sorted Array](https://leetcode.com/problems/find-minimum-in-rotated-sorted-array/)
    ```
    public int findMin(int[] nums) {
        int start=0,end=nums.length-1;
        while(start<end){
            int mid=start+(end-start)/2;
            if(nums[mid]<nums[end]){
                end=mid;
            }else{
                start=mid+1;
            }
        }
        return nums[start];
    }
    ```
- [Find Peak Element](https://leetcode.com/problems/find-peak-element/)
    ```

    ```
- [Find Right Interval](https://leetcode.com/problems/find-right-interval/)
    ```

    ```
- [Reach a Number](https://leetcode.com/problems/reach-a-number/)
    ```

    ```
- [Maximum Value at a Given Index in a Bounded Array](https://leetcode.com/problems/maximum-value-at-a-given-index-in-a-bounded-array/)
    ```

    ```
- [Koko Eating Bananas](https://leetcode.com/problems/koko-eating-bananas/)
    ```

    ```
- [Minimum Absolute Sum Difference](https://leetcode.com/problems/minimum-absolute-sum-difference/)
    ```

    ```
- [Search a 2D Matrix](https://leetcode.com/problems/search-a-2d-matrix/)
    ```

    ```
- [Find a Peak Element II](https://leetcode.com/problems/find-a-peak-element-ii/)
    ```

    ```
- [Frequency of the Most Frequent Element](https://leetcode.com/problems/frequency-of-the-most-frequent-element/)
    ```

    ```
- [Find the Duplicate Number](https://leetcode.com/problems/find-the-duplicate-number/)
    ```

    ```
- [Capacity To Ship Packages Within D Days](https://leetcode.com/problems/capacity-to-ship-packages-within-d-days/)
    ```

    ```
- [4 Sum](https://leetcode.com/problems/4sum/)
    ```

    ```