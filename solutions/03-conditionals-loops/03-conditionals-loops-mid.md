1.Factorial Program In Java
```
    static int fact(int x){
        if(x==0 || x==1){
            return 1;
        }
        if(x>1){
            return (x*fact(x-1));
        }
        return 1;
    }
```

2.Power In Java
```
    static int power(int x, int n) {
        int res = 1;
        for (int i = n; i > 0; i--) {
            res = res * x;
        }
        return res;
    }
```

3.Calculate CGPA 
```
    static double calculateCGPA(double[] grades, double[] credits) {
        double totalGradePoints = 0;
        double totalCredits = 0;
        for (int i = 0; i < grades.length; i++) {
            totalGradePoints += grades[i] * credits[i];
            totalCredits += credits[i];
        }
        return totalGradePoints / totalCredits;
    }
```

4.Compound Interest  
```
    static double calculateCI(double p, double r, double t) {
        double amount = p * Math.pow((1 + r / 100), t);
        return amount;
    }
```

5.Calculate Average Marks
```
    static double avgMarks(float[] arr){
        int n=arr.length;
        double sum=0;
        for(int i=0;i<n;i++){
            sum+=arr[i];
        }
        return sum/n;
    }
```

6.Sum Of N Numbers
```
    static double sumOfN(float[] arr){
        int n=arr.length;
        double sum=0;
        for(int i=0;i<n;i++){
            sum+=arr[i];
        }
        return sum;
    }
```

7.Reverse A String In Java
```
    static String power(String str) {
        char[] arr=str.toCharArray();
        String rev="";
        for(int i=arr.length-1;i>=0;i--){
            rev+=arr[i];
        }
        return rev.toString();
    }
```

8.Find if a number is palindrome or not
```
    static boolean isPali(int num){
        int temp=num;
        int rev=0;
        while(num>0){
            int d=num%10;
            rev=rev*10+d;
            num=num/10;
        }
        return temp==rev;
    }
```

9.Vowel Or Consonant
```
    static void isVorC(String str){
        char[] ch=str.toCharArry();
        
    }
```

10.Perfect Number In Java
```

```

11.Kunal is allowed to go out with his friends only on the even days of a given month. Write a program to count the number of days he can go out in the month of August.
```

```

12.Write a program to print the sum of negative numbers, sum of positive even numbers and the sum of positive odd numbers from a list of numbers (N) entered by the user. The list terminates when the user enters a zero.
```

```