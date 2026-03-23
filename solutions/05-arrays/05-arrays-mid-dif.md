# Mid Ones
1. [Spiral Matrix](https://leetcode.com/problems/spiral-matrix/)
```

```
2. [Spiral Matrix II](https://leetcode.com/problems/spiral-matrix-ii/)
```

```
3. [Spiral Matrix III](https://leetcode.com/problems/spiral-matrix-iii/)
```

```
4. [Set Matrix Zeroes](https://leetcode.com/problems/set-matrix-zeroes/)
```

```
5. [Product of Array Except Self](https://leetcode.com/problems/product-of-array-except-self/)
```
    public int[] productExceptSelf(int[] nums) {
        int[] result=new int[nums.length];
        result[0]=1;
        for(int i=1;i<nums.length;i++){
            result[i]=result[i-1]*nums[i-1];
        }
        int suffix=1;
        for(int i=nums.length-1;i>=0;i--){
            result[i]=result[i]*suffix;
            suffix=suffix*nums[i];
        }
        return result;
    }
```
6. [Find First and Last Position of Element in Sorted Array](https://leetcode.com/problems/find-first-and-last-position-of-element-in-sorted-array/)
```
    public static int[] searchRange(int[] nums, int target) {
        int[] res={-1,-1};
        int start=binarySearch(nums,target,true);
        int end=binarySearch(nums,target,false);
        int res[0]=start;
        int res[1]=end;
        return res;
        }

    static int binarySearch(int[] arr, int target, boolean findFirstIndex){
        int start=0;
        int end=arr.length-1;
        int res=-1;
        while(start<=end){
            int mid=start+(end-start)/2;
            if(arr[mid]>target){
                end=mid-1;
            }else if(arr[mid]<target){
                start=mid+1;
            }else{
                res=mid;
                if(findFirstIndex==true){
                    end=mid-1;
                }else{
                    start=mid+1;
                }
            }
        }
        return res;
    }

```
7. [Jump Game](https://leetcode.com/problems/jump-game/)
```
    public boolean canJump(int[] nums) {
        int position=0;
        for(int i=0;i<nums.length;i++){
            if(i>position) return false;
            position=Math.max(position,i+nums[i]);
        }
        return true;
    }
```
8. [Rotate Array](https://leetcode.com/problems/rotate-array/)
```
    public void rotate(int[] nums, int k) {
        int n=nums.length;
        k=k%n;
        reverse(nums, 0, n - 1);
        reverse(nums, 0, k - 1);
        reverse(nums, k, n - 1);
    }
      private void reverse(int[] nums, int left, int right) {
        while (left < right) {
            int temp = nums[left];
            nums[left] = nums[right];
            nums[right] = temp;
            left++;
            right--;
        }
    }
```
9. [Sort Colors](https://leetcode.com/problems/sort-colors/)
```
    public void sortColors(int[] nums) {
       int zero=0,one=0,n=nums.length;
       for(int num:nums){
            if(num==0) zero++;
            else if(num==1) one++;
       } 

       for(int i=0;i<zero;++i){
        nums[i]=0;
       }

       for(int i=zero;i<zero+one;++i){
        nums[i]=1;
       }

       for(int i =zero+one;i<n;++i){
        nums[i]=2;
       }
    }
```
10. [House Robber](https://leetcode.com/problems/house-robber/)
```
Input: nums = [1,2,3,1], alternate house robbery
Output: 4
Explanation: Rob house 1 (money = 1) and then rob house 3 (money = 3).
Total amount you can rob = 1 + 3 = 4.

    public int rob(int[] nums) {
        int start=0;
        int end=0;

        for(int n:nums){
            int temp=Math.max(end,start+n);
            start=end;
            end=temp;
        }
        return end;    
    } 

```

# Hard Ones
1. [Max Value of Equation](https://leetcode.com/problems/max-value-of-equation/)
```
    
```
2. [First Missing Positive](https://leetcode.com/problems/first-missing-positive/)
```
    class Solution {
    public int firstMissingPositive(int[] nums) {
    int i=0;
    while(i<nums.length){
        int correct= nums[i]-1;
        if(nums[i]>0 && nums[i]<=nums.length && nums[i]!=nums[correct]){
            swap(nums,i,correct);
        }else{
            i++;
        }
    }
    for(int j=0;j<nums.length;j++){
        if(nums[j]!=j+1){
            return j+1;
        }
    }
    return  nums.length+1;
    }

    void swap(int[] nums,int first,int second){
        int temp=nums[first];
        nums[first]=nums[second];
        nums[second]=temp;
    }
}
```
3. [Good Array](https://leetcode.com/problems/check-if-it-is-a-good-array/)
```
     public boolean isGoodArray(int[] nums) {
        int x=nums[0];
        int temp;

        for(int n:nums){
            while(n>0){
                temp=x%n;
                x=n;
                n=temp;
            }
            if(x==1) return true;
        }
        return false;
    }
```