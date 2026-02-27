# Basic Programs

1.Area Of Circle 
```
    static void areaOfCircle(float r){
        double area=3.14*r*r;
        System.out.print(area);
    }
```

2.Area Of Triangle
```
    static void areaOfTriangle(float b,float h){
        double area=0.5*b*h;
        System.out.print(area);
    }
```

3.Area Of Rectangle
```
    static void areaOfRectangle(float l,float b){
        double area=l*b;
        System.out.print(area);
    }
```

4.Perimeter Of Circle
```
    static void periOfCircle(float r){
        double peri=2*3.14*r;
        System.out.print(peri);
    }
```

5.Perimeter Of Equilateral Triangle
```
    static void periOfEquiTriangle(float a){
        double peri=3*a;
        System.out.print(peri);
    }
```

6.Perimeter Of Parallelogram
```
    static void periOfParallelogram(float a,float b){
        double peri=2*(a+b);
        System.out.print(peri);
    }
```

7.Volume Of Cone
```
    static void volumeOfCone(float r,float h){
        double volume=0.33*3.14*r*r*h;
        System.out.print(volume);
    }
```

8.Volume Of Sphere
```
    static void volumeOfSphere(float r){
        double volume=1.33*3.14*r*r*r; //(4/3)πr³
        System.out.print(volume);
    }
```

9.Volume Of Pyramid
```
     static void volumeOfPyramid(float b,float h){
        double volume=0.33*b*h; //(1/3) xbase area × Height
        System.out.print(volume);
    }
```

10.Curved Surface Area Of Cylinder
```
    static void csaOfCylinder(float r, float h){
        double csa=2*3.14*r*h; //2πrh 
        System.out.print(csa);
    }
```

11.Total Surface Area Of Cube
```
    static void tsaOfCube(float a){
        double tsa=6*a*a;
        System.out.print(tsa);
    }
```

12.Subtract the Product and Sum of Digits of an Integer
```
    static int subtractProductAndSum(int num) {
        int sum = 0;
        int product = 1;
        while (num != 0) {
            int digit = num % 10;
            sum += digit;
            product *= digit;
            num /= 10;
        }
        return product - sum;
}
```

13.Input a number and print all the factors of that number (use loops).
```
    static void factors(int num) {
        for (int i = 1; i <= num; i++) {
            if (num % i == 0) {
                System.out.print(i + " ");
            }
        }
    }
```
