# Ex.No:1(D) ARRAYS

## QUESTION:
Write a Java program to reverse an array.

## AIM:
To write a Java program that reads an array of integers and prints the array in reverse order.

## ALGORITHM :
1. Start the program.
2. Read the size of the array from the user.
3. Create an integer array of that size.
4. Read all elements of the array.
5. Use a loop to traverse the array from the last element to the first.
6. Print each element while traversing backward.
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
import java.util.Scanner;
public class Main{
    public static void main(String[] args){
        Scanner input=new Scanner(System.in);
        int n=input.nextInt();
        int arr[]=new int[n];
        for(int i=0;i<n;i++){
            arr[i]=input.nextInt();
        }
        for(int i=n-1;i>=0;i--){
            System.out.print(arr[i]+" ");
        }
    }
}
```





## OUTPUT:
<img width="1257" height="475" alt="image" src="https://github.com/user-attachments/assets/10e0a2c5-206e-4ece-bd65-dff8e210b362" />



## RESULT:
The program was executed successfully.
When the input array 10, 20, 30, 40 was entered, the program reversed the order of the elements.
