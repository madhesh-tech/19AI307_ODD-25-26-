# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:

Write a program to access a static variable using both class name and object.

## AIM:
To write a Java program that demonstrates accessing a static variable using both the class name and an object of the class.

## ALGORITHM :
1. Start the program.
2. Create a class containing a static integer variable.
3. Read a value from the user and assign it to the static variable.
4. Access the static variable using the class name.
5. Create an object of the class.
6.  Access the same static variable using the object reference.
7.  Print both results and end the program.


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
    static int num;
    public static void main(String[] args){
        Scanner input = new Scanner(System.in);
        num = input.nextInt();
        Main obj = new Main();
        System.out.println("Accessing using class name: "+Main.num);
        System.out.println("Accessing using object: "+obj.num);
    }
}
```





## OUTPUT:

<img width="1258" height="272" alt="image" src="https://github.com/user-attachments/assets/7e818851-880c-4543-baac-838ea41031d4" />


## RESULT:

The program was executed successfully.
The static variable was assigned the input value 48.
When accessed using the class name and using an object, the program correctly displayed the same value in both cases.
