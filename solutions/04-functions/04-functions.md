1.Define two methods to print the maximum and the minimum number respectively among three numbers entered by the user.
```
    static int largestOfThree(int a,int b,int c){
        if(a>b && a>c){
            return a;
        }else if(b>a && b>c){
            return b;
        }else{
            return c;
        }
    }
```

2.Define a program to find out whether a given number is even or odd.
```
    static String oddEven(int num){
        if(num%2==0){
            return "Even";
        }else{
            return "Odd";
        }
    }
```

3.A person is eligible to vote if his/her age is greater than or equal to 18. Define a method to find out if he/she is eligible to vote.
```
    static String oddEven(int age){
        if(age>=18){
            return "Eligible to vote";
        }else{
            return "Ineligible to vote";
        }
    }
```

4.Write a program to print the sum of two numbers entered by user by defining your own method.
```
    static double add(float num1,float num2){
        double res=num1+num2;
        return res;    
    }
```


5.Define a method that returns the product of two numbers entered by user.
```
    static double add(float num1,float num2){
        double res=num1*num2;
        return res;    
    }
```

6.Write a function that returns all prime numbers between two given numbers.
```
public class Prime {
    public static void main(String[] args) {
        int low = 20, high = 50;
        while (low < high) {
            if(checkPrimeNumber(low))
                System.out.print(low + " ");
            ++low;
        }
    }

    public static boolean checkPrimeNumber(int num) {
        boolean flag = true;
        for(int i = 2; i <= num/2; ++i) {
            if(num % i == 0) {
                flag = false;
                break;
            }
        }
        return flag;
    }
}
```

7.Write a program that will ask the user to enter his/her marks (out of 100). Define a method that will display grades according to the marks entered as below:
```
    static String marksOut(float marks){
        if(marks>=91 && marks<=100){
            return "AA";
        }else if(marks>=81 && marks<=90){
            return "AB";
        }else if(marks>=71 && marks<=80){
            return "BB";
        }else if(marks>=61 && marks<=70){
            return "BC";
        }else if(marks>=51 && marks<=60){
            return "CD";
        }else if(marks>=41 && marks<=50){
            return "DD";
        }else if(marks<=40){
            return "Fail";
        }else{
            return "Extra marks for good Handwriting";
        }
    }
```

8.Write a function to find if a number is a palindrome or not. Take number as parameter.
```
    static boolean isPali(int num){
        if(num<0){
            num=num*(-1);
        }
        int rev=0;
        int temp=num;
        while(num>0){
            int d=num%10;
            rev=rev*10+d;
            num/=10;
        }
        return temp==rev;
    }
```

9.Write a function to check if a given triplet is a Pythagorean triplet or not. (A Pythagorean triplet is when the sum of the square of two numbers is equal to the square of the third number).
```
     static boolean PythagoreanTrip(int a, int b,int c){
        int absquare=(a*a)+(b*b);
        int csquare=c*c;
        return absquare==csquare;
    }
```

10.Write a function that returns the sum of first n natural numbers.
```
    static int sumOfNatural(int end){
        int sum=0;
        for(int i=0;i<=end;i++){
            sum+=i;
        }
        return sum;
    }
```
