# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:

Write a program that reads two integers and divides the first by the second. Handle the case when division by zero occurs.

## AIM:
To write a Java program that reads two integers, performs division, and handles the ArithmeticException when division by zero occurs.

## ALGORITHM :
1. Start the program.
2. Read two integers from the user: dividend and divisor.
3. Use a try block to perform the division.
4. If the divisor is zero, an ArithmeticException will occur.
5. Catch the exception and display an appropriate message.
6. If no exception occurs, print the division result.
7. End the program.

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
import java.util.*;
public class Main{
    public static void main(String args[]){
        Scanner input=new Scanner(System.in);
        try{
            int a=input.nextInt();
            int b=input.nextInt();
            System.out.print("Result: "+(a/b));
        }
        catch(ArithmeticException e){
            System.out.print("Error: Division by zero");
        }
    }
}
```






## OUTPUT:

<img width="1262" height="276" alt="image" src="https://github.com/user-attachments/assets/e26d359c-6cd8-44b0-b5af-fa483c9834a7" />


## RESULT:
The program successfully performs division of two integers and handles division-by-zero errors using exception handling.
