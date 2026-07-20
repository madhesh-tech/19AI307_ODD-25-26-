# Ex.No:2(B) METHODS

## QUESTION:

Create a method printName(String name) that gets input from the user for the string and prints "Hello, " followed by the name passed.

## AIM:

To create a method printName(String name) that prints "Hello, " followed by the given name, where the name is taken as user input.

## ALGORITHM :
1. Start the program.
2. Create a method named printName that takes a string argument.
3. Inside the method, print "Hello, " followed by the received name.
4. In the main method, read a string input from the user.
5. Call the printName method and pass the input string.
6. The method prints the greeting message.
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
public class prog{
    static void printName(String name){
        System.out.print("Hello, "+name);
    }
    public static void main(String[] args){
        Scanner input = new Scanner(System.in);
        String name = input.nextLine();
        printName(name);
    }
}
```


## OUTPUT:
<img width="1267" height="143" alt="image" src="https://github.com/user-attachments/assets/b741de50-ff29-4214-82f2-2afcc433d1bc" />



## RESULT:
The program was executed successfully.
When the user entered a name, the method printed a greeting message starting with "Hello," followed by the given name.
