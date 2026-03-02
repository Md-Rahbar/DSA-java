#Easy Ones

1. [Build Array from Permutation](https://leetcode.com/problems/build-array-from-permutation/)
```
    public int[] buildArray(int[] nums) {
        int[] res=new int[nums.length];
        for(int i=0;i<nums.length;i++){
            res[i]=nums[nums[i]];
        }
        return res;
    }
```
2. [Concatenation of Array](https://leetcode.com/problems/concatenation-of-array/)
```
    public int[] getConcatenation(int[] nums) {
        int n=nums.length;
        int[] res=new int[2*n];
        for(int i=0;i<n;i++){
            res[i]=nums[i];
            res[i+n]=nums[i];
        }
        return res;
    }
```
3. [Running Sum of 1d Array](https://leetcode.com/problems/running-sum-of-1d-array/)
```
    public int[] runningSum(int[] nums) {
        for(int i=1;i<nums.length;i++){
            nums[i]=nums[i-1]+nums[i];
        }
        return nums;
    }
```
4. [Richest Customer Wealth](https://leetcode.com/problems/richest-customer-wealth/)
```
    public int maximumWealth(int[][] accounts) {
        int maxSum=0;
        for(int[] persons: accounts){
            int sum=0;
            for(int person: persons){
                sum+=person;
            }
            if(sum>maxSum){
                maxSum=sum;
            }
        }
        return maxSum;
    }
```
5. [Shuffle the Array](https://leetcode.com/problems/shuffle-the-array/)
```
    public int[] shuffle(int[] nums, int n) {
        int[] res=new int[2*n];
        int idx=0;
        for(int i=0;i<n;i++){
            res[idx++]=nums[i];
            res[idx++]=nums[i+n];
        }
        return res;
    }
```
6. [Kids With the Greatest Number of Candies](https://leetcode.com/problems/kids-with-the-greatest-number-of-candies/)
```
    public List<Boolean> kidsWithCandies(int[] candies, int extraCandies) {
        List<Boolean> res= new ArrayList<>();
        int maxCandy=0;
        for(int candy:candies){
            maxCandy=Math.max(candy,maxCandy);
        }
        for(int i=0;i<candies.length;i++){
            if(candies[i]+extraCandies>=maxCandy){
                res.add(true);
            }else{
                res.add(false);
            }
        }
        return res;
    }
```
7. [Number of Good Pairs](https://leetcode.com/problems/number-of-good-pairs/)
```

```
8. [How Many Numbers Are Smaller Than the Current Number](https://leetcode.com/problems/how-many-numbers-are-smaller-than-the-current-number/)
```

```
9. [How Many Numbers Are Smaller Than the Current Number](https://leetcode.com/problems/how-many-numbers-are-smaller-than-the-current-number/)
```

```
10. [Check if the Sentence Is Pangram](https://leetcode.com/problems/check-if-the-sentence-is-pangram/)
```

```
11. [Count Items Matching a Rule](https://leetcode.com/problems/count-items-matching-a-rule/)
```

```
12. [Find the Highest Altitude](https://leetcode.com/problems/find-the-highest-altitude/)
```

```
13. [Flipping an Image](https://leetcode.com/problems/flipping-an-image/)
```

```
14. [Cells with Odd Values in a Matrix](https://leetcode.com/problems/cells-with-odd-values-in-a-matrix/)
```

```
15. [Matrix Diagonal Sum](https://leetcode.com/problems/matrix-diagonal-sum/)
```

```
16. [Find Numbers with Even Number of Digits](https://leetcode.com/problems/find-numbers-with-even-number-of-digits/)
```

```
17. [Transpose Matrix](https://leetcode.com/problems/transpose-matrix/)
```

```
18. [Add to Array-Form of Integer](https://leetcode.com/problems/add-to-array-form-of-integer/)
```

```
19. [Maximum Population Year](https://leetcode.com/problems/maximum-population-year/)
```

```
20. [Determine Whether Matrix Can Be Obtained By Rotation](https://leetcode.com/problems/determine-whether-matrix-can-be-obtained-by-rotation/)
```

```
21. [Two Sum](https://leetcode.com/problems/two-sum/)
```

```
22. [Find N Unique Integers Sum up to Zero](https://leetcode.com/problems/find-n-unique-integers-sum-up-to-zero/)
```

```
23. [Lucky Number In a Matrix](https://leetcode.com/problems/lucky-numbers-in-a-matrix/)
```

```
24. [Maximum Subarray](https://leetcode.com/problems/maximum-subarray/)
```

```
25. [Reshape the Matrix](https://leetcode.com/problems/reshape-the-matrix/)
```

```
26. [Plus One](https://leetcode.com/problems/plus-one/)
```

```
27. [Remove Duplicates from Sorted Array](https://leetcode.com/problems/remove-duplicates-from-sorted-array/)
```

```
28. [Minimum Cost to Move Chips to The Same Position](https://leetcode.com/problems/minimum-cost-to-move-chips-to-the-same-position/)
```

```