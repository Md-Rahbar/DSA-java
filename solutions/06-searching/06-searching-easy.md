## Easy
- [Square Root](https://leetcode.com/problems/sqrtx/)
    ```
    //binary search approach
    public int mySqrt(int x) {
       if(x<2) return x;
        // sqrt will lie between 0 to half of number 
       int left=0,right= x/2; 
       while(left<=right){
        int mid=left+(right-left)/2;
        long sq=(long)mid*mid;

        if(sq<x){
            left=mid+1;
        }else if(sq>x){
            right=mid-1;
        }else{
            return mid;
        }
       }
       return right;
    }
    ```
- [Guess Number Higher or Lower](https://leetcode.com/problems/guess-number-higher-or-lower/)
    ```

    public class Solution extends GuessGame {
        public int guessNumber(int n) {
            int low=1;
            int high=n;
            while(low<=high)
            {
                int mid = low + (high-low)/2;
                if(guess(mid)==0) return mid;
                else if(guess(mid)==1) low=mid+1;
                else high=mid-1; 
            }
            return -1;
        }
    }
    ```
- [First Bad Version](https://leetcode.com/problems/first-bad-version/)
    ```
    public int firstBadVersion(int n) {
        int low=1,high=n;
        int res=0;

        while(low<=high){
            int mid=low+(high-low)/2;
            // isBadVersion(val) is an API which returns true or false based on version
            if(isBadVersion(mid) == true){
                res=mid;
                high=mid-1;
            }else{
                low=mid+1;
            }
        }
        return res;
    }
    ```
- [Two Sum II - Input array is sorted](https://leetcode.com/problems/two-sum-ii-input-array-is-sorted/)
    ```
    public int[] twoSum(int[] numbers, int target) {
        int low=0,high=numbers.length-1;

        while(low<=high){
            int sum = numbers[start]+numbers[end];
            if(sum==target) return new int[]{start+1,end+1};
            else if(sum>target) end--;
            else start++;
        }    
        return new int[]{0};
    }
    ```
- [Valid Perfect Square](https://leetcode.com/problems/valid-perfect-square/)
    ```
    public boolean isPerfectSquare(int num) {
        int low = 0, high = num;
        while (low <= high) {
            int mid = low + (high - low) / 2;
            long midSq = (long) mid * mid;
            if (midSq == num)
                return true;
            else if (midSq > num)
                high = mid - 1;
            else
                low = mid + 1;
        }
        return false;
    }
    ```
- [Arranging Coins(Easy)](https://leetcode.com/problems/arranging-coins/)
    ```
    public int arrangeCoins(int n) {
        long start = 1;
        long end = n;
        long ans = 0;
        long mid = 0;
        
        while(start <= end) {
            mid = start + (end-start)/2;
            
            long coinCount = (mid*(mid+1))/2;
                
                if(coinCount <= n){
                    ans = mid;
                    start = mid+1;
                } else {
                    end = mid-1;
                }
        }
    return (int)ans; 
    }
    ```
- [Find Smallest Letter Greater Than Target](https://leetcode.com/problems/find-smallest-letter-greater-than-target/)
    ```
    public char nextGreatestLetter(char[] letters, char target) {
        int low = 0;
        int high = letters.length - 1;
        while (low <= high) {
            int mid=low+(high-low)/2;
            if (letters[mid] > target) {
                high = mid - 1;
            } else {
                low = mid + 1;
            }
        }
        return letters[low % letters.length];
    }
    ```
- [Kth Missing Positive Number](https://leetcode.com/problems/kth-missing-positive-number/)
    ```
    public int findKthPositive(int[] arr, int k) {
        int low = 0, high = arr.length - 1;

        while (low <= high) {
            int mid = low + (high - low) / 2;
            if (arr[mid] - mid - 1 < k) {
                low = mid + 1;
            } else {
                high = mid - 1;
            }
        }
        return k + low;
    }
    ```
- [Search Insert Position](https://leetcode.com/problems/search-insert-position/)
    ```
    public int searchInsert(int[] nums, int target) {
        int low = 0, high = nums.length - 1;
        while (low <= high) {
            int mid = low + (high - low) / 2;
            if (nums[mid] > target) {
                high = mid - 1;
            } else if (nums[mid] < target) {
                low = mid + 1;
            } else {
                return mid;
            }
        }
        return low;
    }
    ```
- [Peak Index in a Mountain Array](https://leetcode.com/problems/peak-index-in-a-mountain-array/)
    ```
    public int peakIndexInMountainArray(int[] arr) {
        int low = 0, high = arr.length - 1;
        while (low < high) {
            int mid = low + (high - low) / 2;
            if (arr[mid] > arr[mid + 1]) {
                high = mid;
            } else {
                low = mid + 1;
            }
        }
        return low;
    }
    ```
- [Count Negative Numbers in a Sorted Matrix](https://leetcode.com/problems/count-negative-numbers-in-a-sorted-matrix/)
    ```

    ```
- [Intersection of Two Arrays](https://leetcode.com/problems/intersection-of-two-arrays/)
    ```

    ```
- [Intersection of Two Arrays II](https://leetcode.com/problems/intersection-of-two-arrays-ii/)
    ```

    ```
- [Fair Candy Swap](https://leetcode.com/problems/fair-candy-swap/)
    ```

    ```
- [Check If N and Its Double Exist](https://leetcode.com/problems/check-if-n-and-its-double-exist/)
    ```
    public boolean checkIfExist(int[] arr) {
        for(int i=0;i<arr.length;i++){
            for(int j=0;j<arr.length;j++){
                if(arr[i]==arr[j]*2 && i!=j){
                    return true;
                }
            }
        }

        return false;
    }
    ```
- [Special Array With X Elements Greater Than or Equal X](https://leetcode.com/problems/special-array-with-x-elements-greater-than-or-equal-x/)
    ```

    ```
- [Binary Search](https://leetcode.com/problems/binary-search/)
    ```
    public int search(int[] nums, int target) {
        int low = 0, high = nums.length - 1;
        while (low <= high) {
            int mid = low + (high - low) / 2;
            if (nums[mid] == target) {
                return mid;
            } else if (nums[mid] > target) {
                high = mid - 1;
            } else {
                low = mid + 1;
            }
        }
        return -1;
    }
    ```