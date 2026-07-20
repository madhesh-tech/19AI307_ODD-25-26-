# Ex.No:3(E) INNER CLASS

## QUESTION:
Write a Java program to demonstrate the concept of an inner class. The program should contain an outer class with a method and an inner class with another method. Create objects of both classes and display their outputs.

## AIM:
To write a Java program that shows how to declare and use an inner class in Java, and to understand how objects of inner classes are created using an outer class object.

## ALGORITHM :
Start the program.
Create an Outer class with a method outerMethod() that prints a message.
Inside the Outer class, create an Inner class with a method innerMethod() that prints a message.
In the main() method:
Create an object of the Outer class.
Call the outerMethod().
Create an object of the Inner class using:
Outer.Inner inner = outer.new Inner();
Call the innerMethod().
Display the output.
End the program.





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
class Outer {
    
    void outerMethod() {
        System.out.println("This is the Outer class method.");
    }

    // Inner class
    class Inner {
        void innerMethod() {
            System.out.println("This is the Inner class method.");
        }
    }
}

public class InnerClassDemo {
    public static void main(String[] args) {

        Outer outer = new Outer();
        outer.outerMethod();

        Outer.Inner inner = outer.new Inner();
        inner.innerMethod();
    }
}
```


## OUTPUT:

<img width="336" height="66" alt="image" src="https://github.com/user-attachments/assets/a28a2ffc-2274-48ab-9238-864b25cc09fe" />


## RESULT:
The program successfully demonstrates the use of inner classes.
