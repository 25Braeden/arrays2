# Arrays 2
## If you're in my java class don't take my work. It's on you if you do. This is a reference. Anybody else you can take whatever you want.
### Problem 1
#### Answer
```java
// a. A 24-element float array
float[] floatArray = new float[24];

// b. A 500-element int array
int[] intArray = new int[500];

// c. A 50-element double array
double[] doubleArray = new double[50];

// d. A 10-element char array
char[] charArray = new char[10];
```
### Problem 2
#### Answer
```
1   3   -2
17   6   11
4   2   2
19   14   5
11   15   -4

Suma: 52
Sumb: 40
Sumdiff: 12
```
#### Runnable code
```java
import java.util.Scanner;

public class arrays {
    public static void main(String[] args) {
        int[] a, b;
        int j, m, suma = 0, sumb = 0, sumdiff = 0;
        Scanner keyboard = new Scanner(System.in);
        a = new int[100];
        b = new int[100];

        System.out.print("Enter the number of pairs: ");
        m = keyboard.nextInt();

        System.out.println("Enter pairs of integers:");

        for (j = 0; j < m; j++) {
            a[j] = keyboard.nextInt();
            b[j] = keyboard.nextInt();
            suma += a[j];
            sumb += b[j];
            sumdiff += (a[j] - b[j]);
        }

        System.out.println("\nReverse order of pairs and differences:");

        for (j = m - 1; j >= 0; j--) {
            System.out.println(a[j] + "   " + b[j] + "   " + (a[j] - b[j]));
        }

        System.out.println("\nSuma: " + suma + "\nSumb: " + sumb + "\nSumdiff: " + sumdiff);
    }
}
```
### Problem 3
#### Answer
`10 9 8 7 6 5 4 3`
#### Code
```java
public class arrays {
    public static void main(String[] args) {
      int[] sample = new int[8];

      for (int k = 0; k < 8; k++) {
          sample[k] = 10 - k;
      }
      
      System.out.print("Array contents: ");
      for (int i = 0; i < sample.length; i++) {
          System.out.print(sample[i] + " ");
      }
      
    }
}
```
### Problem 4
#### Answer
`1 1 1 1 -1 -1 -1 -1`
#### Code
```java
public class arrays {
    public static void main(String[] args) {
        int[] sample = new int[8];

        for (int i = 0; i < 8; i++) {
            if (i <= 3) {
                sample[i] = 1;
            } else {
                sample[i] = -1;
            }
        }

        System.out.print("Array contents: ");
        for (int i = 0; i < sample.length; i++) {
            System.out.print(sample[i] + " ");
        }
    }
}
```
### Problem 5
#### Answer
`0 101 2 103 4 105 6 107`
#### Code
```java
public class arrays {
    public static void main(String[] args) {
        int[] sample = new int[8];

        for (int k = 0; k < 8; k++) {
            if (k % 2 == 0)
                sample[k] = k;
            else
                sample[k] = k + 100;
        }

        System.out.print("Array contents: ");
        for (int i = 0; i < sample.length; i++) {
            System.out.print(sample[i] + " ");
        }
    }
}
```
### Problem 6
#### Answer
Array values after the operation: -4 0 2 26 10 12 14 <br />
#### Code
```java
public class arrays {
    public static void main(String[] args) {
      int h = 6, p = 2, m = 3;
      int[] values = {-4, 0, 2, 6, -2, -1, 14};
      for (; m <= 5; m++) {
         values[m] = values[h] + values[p] * values[m];
     }
      System.out.print("Array values after the operation: ");
      for (int i = 0; i < values.length; i++) {
         System.out.print(values[i] + " ");
      }
   }
}
```
### Problem 7
#### Answer 
They forgot the [] after `int`. The corrected code is:
```java
int i;
int[] count = new int[10];
System.out.println("Please enter 10 numbers: ");
for (i = 0; i < 10; i++)
    count[i] = keybd.nextInt();
```
### Problem 8
```java
for (int i = 0; i < array.length; i++) {
    int doubledValue = array[i] * 2;
    // You can use 'doubledValue' in further processing or print it, depending on your needs.
}
```
### Problem 9
```java
int sum = 0; // Initialize sum to 0
for (int i = 0; i < array.length; i += 2) {
    int num = array[i];
    sum += num;
}
```
### Problem 10
```java
int[] array = new int[25];
       int sum = 0;
       for (int i = 0; i < array.length; i++) {
           if(array[i] % 2 == 0) {
               sum += array[i];
           }
       }
```
### Problem 11
#### Output
```
50  45  40  35  30  25  20  15  10  5  
5  10  15  20  25  30  35  40  45  50  
5   5   5   5   5   5   5   5   5   5
```
### Problem 12
#### Output
```
50  45  40  35  30  25  20  15  10  5  
5  10  15  20  25  30  35  40  45  50  
5   5   10   15   20   25   30   35   40   45
```
### Problem 13
```java
public class Example {
    public static void main(String[] args) {
        int[] temps = new int[50];


        boolean num = false;

        for (int i = 0; i < temps.length; i++) {
            if (temps[i] == 100) {
                num = true;
                break;
            }
        }

        if (num) {
            System.out.println("yes");
        }
    }
}
```
### Problem 14
```java
import java.util.Arrays;
import java.util.Random;

public class ArraysExample {
    public boolean is100(int x) {
        return x == 100;
    }

    public static void main(String[] args) {
        Random random = new Random();
        int[] temps = new int[50];

        // Populate the temps array with random values
        for (int i = 0; i < temps.length; i++) {
            temps[i] = random.nextInt(100) + 1;
        }

        // Use a flag to track if 100 is found
        boolean found100 = false;

        // Check each element in the array
        for (int temp : temps) {
            if (new ArraysExample().is100(temp)) {
                found100 = true;
                break;  // Exit the loop once a match is found
            }
        }

        // Print the result
        if (found100) {
            System.out.println("Value 100 found in the array.");
        } else {
            System.out.println("Value 100 not found in the array.");
        }
    }
}
```
