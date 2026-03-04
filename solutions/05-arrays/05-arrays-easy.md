# Easy Ones

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
    public int numIdenticalPairs(int[] nums) {
        int res=0;
        int[] count=new int[101];
        for(int i:nums){
            res=res+count[i]++;
        }
        return res;
    }
```
8. [How Many Numbers Are Smaller Than the Current Number](https://leetcode.com/problems/how-many-numbers-are-smaller-than-the-current-number/)
```
    public int[] smallerNumbersThanCurrent(int[] nums) {
        int[] res=new int[nums.length];
        for(int i=0;i<nums.length;i++){
            int count=0;
            for(int j=0;j<nums.length;j++){
                if(nums[j]<nums[i]){
                    count++;
                }
            }
            res[i]=count;
        }
        return res;
    }
```

10. [Check if the Sentence Is Pangram](https://leetcode.com/problems/check-if-the-sentence-is-pangram/)
```
        //Pangram--> All the alphabets should be present in the sentence
        public boolean checkIfPangram(String sentence) {
        if(sentence.length()<26) return false;
        for(char ch='a';ch<='z';ch++){
            if(sentence.indexOf(ch)<0){
                return false;
            }
        }
        return true;
    }
```
11. [Count Items Matching a Rule](https://leetcode.com/problems/count-items-matching-a-rule/)
```
    public int countMatches(List<List<String>> items, String ruleKey, String ruleValue) {
        int result=0;
        for(int i=0;i<items.size();i++){
            if(ruleKey.equals("type") && items.get(i).get(0).equals(ruleValue)) result++;
            if(ruleKey.equals("color") && items.get(i).get(1).equals(ruleValue)) result++;
            if(ruleKey.equals("name") && items.get(i).get(2).equals(ruleValue)) result++;
        }
        return result;
    }
```
12. [Find the Highest Altitude](https://leetcode.com/problems/find-the-highest-altitude/)
```
    public int largestAltitude(int[] gain) {
        int currentAlti=0;
        int highestPoint=currentAlti;

        for(int i:gain){
            currentAlti+=i;
            highestPoint=Math.max(currentAlti,highestPoint);
        }
    return highestPoint;
    }
```
13. [Flipping an Image](https://leetcode.com/problems/flipping-an-image/)
```
    public int[][] flipAndInvertImage(int[][] image) {
        for(int i=0;i<image.length;i++){
        int start=0;
        int end=image[i].length-1;
        while(start<=end){
            int temp=image[i][start]^1;
            image[i][start]=image[i][end]^1;
            image[i][end]=temp;
            start++;
            end--;
        }
    }
    return image;
    }
```
14. [Cells with Odd Values in a Matrix](https://leetcode.com/problems/cells-with-odd-values-in-a-matrix/)
```
    public int oddCells(int m, int n, int[][] indices) {
        int row[] = new int[m];
        int col[] =new int[n];
        int count=0;

        for(int x[]: indices){
            row[x[0]]++;
            col[x[1]]++;
        }

        for(int i=0;i<m;i++)
            for(int j=0;j<n;j++)
                count+=(row[i]+col[j])%2;
        return count;
    }
```
15. [Matrix Diagonal Sum](https://leetcode.com/problems/matrix-diagonal-sum/)
```

```
16. [Find Numbers with Even Number of Digits](https://leetcode.com/problems/find-numbers-with-even-number-of-digits/)
```
    public int findNumbers(int[] nums) {
       int count=0;
        for(int num:nums){
            if(even(num)){
                count++;
            }
        }
       return count; 
    }
    static boolean even(int num){
        int count=0;
        while(num>0){
            count++;
            num=num/10;
        }
        return (count%2==0);
    }
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
    public int[] twoSum(int[] nums, int target) {  
        Map<Integer,Integer> map=new HashMap<>();
        for(int i =0;i<nums.length;i++){
            int needed=target-nums[i];
            if(map.containsKey(needed)){
                return new int[]{map.get(needed),i};
            }
            map.put(nums[i],i);
        }
        return new int[]{-1,-1};
    }
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
27. [Minimum Cost to Move Chips to The Same Position](https://leetcode.com/problems/minimum-cost-to-move-chips-to-the-same-position/)
```

```
