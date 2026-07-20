# Ex.No:3(F) WRAPPER CLASS

## QUESTION:
Write a Java program to check if a number is an Armstrong number using Math.pow() and the Integer wrapper class. Take input from the user.

## AIM:
To write a Java program that checks whether a given number is an Armstrong number using Math.pow() and the Integer wrapper class to count digits.

## ALGORITHM :
1. Start the program.
2. Read an integer value from the user.
3. Convert the number to a string using Integer.toString() to count the number of digits.
4. Extract each digit of the number using modulus and division.
5. For each digit, calculate its power using Math.pow(digit, number_of_digits) and add to the sum.
6.  After processing all digits, compare the sum with the original number.
7. If both are equal, it is an Armstrong number; otherwise, it is not.
8. Stop the program.


## PROGRAM:
```
/*
Program to implement variables and Operators using Java
Developed by: Madhesh I
RegisterNumber:  212224220055
*/
```

## SOURCE CODE:
```java
import java.util.Scanner;

public class ArmstrongCheck {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // Taking input from user
        int num = sc.nextInt();

        // Convert to string to count digits using Integer wrapper class
        int digits = Integer.toString(num).length();

        int temp = num;
        int sum = 0;

        // Calculate sum of digits raised to power of digits
        while (temp > 0) {
            int digit = temp % 10;
            sum += Math.pow(digit, digits);
            temp /= 10;
        }

        // Check Armstrong condition
        if (sum == num) {
            System.out.println(num + " is an Armstrong number.");
        } else {
            System.out.println(num + " is not an Armstrong number.");
        }

        sc.close();
    }
}

```






## OUTPUT:
<img width="1263" height="219" alt="image" src="https://github.com/user-attachments/assets/bc064f4b-bfbe-4e6f-8971-66d28f2c1706" />



## RESULT:
The program successfully checks whether a given number is an Armstrong number by calculating the sum of each digit raised to the total number of digits.
The output correctly displays whether the input number is an Armstrong number.
