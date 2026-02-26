1.Write a program to print whether a number is even or odd, also take input from the user.
```
    static String evenOrOdd(int num){
        if(num%2==0){
            return "Even";
        }else{
            return "Odd";
        }
    }
```

2.Take name as input and print a greeting message for that particular name.
```
    static void greetMe(){
        Scanner sc=new Scanner(System.in);
        String name=sc.nextLine();
        System.out.println("Hello, "+name+" Have a nice day!!");
    }
```

3.Write a program to input principal, time, and rate (P, T, R) from the user and find Simple Interest.
```
    static void simpleInterest(float P, float R, float t){
        int SI=(P*R*T)/100;
        System.out.println(SI);
    }
```

4.Take in two numbers and an operator (+, -, *, /) and calculate the value. (Use if conditions)
```
    static void conditionalOperations(int a,int b, char op){
        double ans;
        if(op=='+'){
            ans=a+b;
        }else if(op=='-'){
            ans=a-b;
        }else if(op=='*'){
            ans=a*b;
        }else{
            ans=a/b;
        }
        System.out.print(ans);
    }
```

5.Take 2 numbers as input and print the largest number.
```
    static int largest(int a,int b){
        if(a>b){
            return a;
        }
        return b;
    }
```

6.Input currency in rupees and output in USD.
```
    static void rupeesToUSD(double rupees){
        double USD= rupees/90;
        System.out.print(USD);
    }
```

7.To calculate Fibonacci Series up to n numbers.
```
       public int fib(int n) {
        if(n<=1) return n;
        return fib(n-1) + fib(n-2);
    }
```

8.To find out whether the given String is Palindrome or not.
```
    static boolean isPali(String str){
        s=str.toLowerCase();
        String rev="";
        for(int i=s.length();i>=0;i--){
            rev=rev+s.charAt(i);
        }
        return s.equals(rev);
    }
```

9.To find Armstrong Number between two given number.
```
     static int countDigits(int num) {
        int count = 0;
        while (num != 0) {
            count++;
            num /= 10;
        }
        return count;
    }

    // Method to check Armstrong
    static boolean isArmstrong(int num) {
        int original = num;
        int digits = countDigits(num); 
        int sum = 0;

        while (num != 0) {
            int digit = num % 10;
            sum += (int) Math.pow(digit, digits);
            num /= 10;
        }
        return sum == original;
    }

    // Method to print Armstrong numbers in range
    static void printArmstrongInRange(int low, int high) {
        for (int i = low; i <= high; i++) {
            if (isArmstrong(i)) {
                System.out.print(i + " ");
            }
        }
    }
```
