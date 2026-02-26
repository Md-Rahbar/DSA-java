1.Input a year and find whether it is a leap year or not.
```
    static boolean leapYear(int year){
        if((year%4==0 && year%100!=0 ) || year%400==0  ){
            return true;
        }
        return false;
    }
```

2.Take two numbers and print the sum of both.
```
    static int sum(int a,int b){
        int temp=a+b;
        return temp;
    }
```
3.Take a number as input and print the multiplication table for it.
```
    static void table(int num){
        for(int i=1;i<=10;i++){
            System.out.println(num+"*"+i+"="+(num*i));
        }
    }
```
4.Take 2 numbers as inputs and find their HCF and LCM.
```
    public static int findHCF(int a, int b) {
        int hcf = 1;

        for (int i = 1; i <= a && i <= b; i++) {
            if (a % i == 0 && b % i == 0) {
                hcf = i;
            }
        }

        return hcf;
    }
        // Method to find LCM
    public static int findLCM(int a, int b) {
        int hcf = findHCF(a, b);
        int lcm = (a * b) / hcf;
        return lcm;
    }
```

5.Keep taking numbers as inputs till the user enters ‘x’, after that print sum of all.
```
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int sum = 0;
        while (true) {
            System.out.print("Enter number (or x to stop): ");
            String input = sc.next();
            if (input.equals("x") || input.equals("X")) {
                break;
            }

            int num = 0;
            // Convert string to integer manually
            for (int i = 0; i < input.length(); i++) {
                num = num * 10 + (input.charAt(i) - '0');
            }
            sum = sum + num;
        }
        System.out.println("Total Sum: " + sum);
    }
```