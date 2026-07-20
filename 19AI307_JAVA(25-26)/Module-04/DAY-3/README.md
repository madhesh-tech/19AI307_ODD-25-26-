# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:
Write a Java program to demonstrate Composition, where one class contains another class as a part of it. Create an Engine class and a Car class.
The Car class should contain an Engine object and use it to start the car.

## AIM:
To write a Java program that demonstrates composition by creating a Car class that has an Engine object. When the car starts, the engine is also started, showing strong ownership between the two objects.

## ALGORITHM :
1. Start the program.
2. Create an Engine class with a method start() that prints a message.
3. Create a Car class that contains a private Engine object.
4. Initialize the Engine object inside the Car constructor.
5. Define a startCar() method in Car to call the engine.start() method.
6. In main(), create an object of the Car class.
7. Call the startCar() method to demonstrate composition.
8. End the program.



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
// Engine class (part of Car)
class Engine {
    void start() {
        System.out.println("Engine started.");
    }
}

// Car class uses Composition
class Car {
    private Engine engine;  // Car HAS-A Engine

    Car() {
        engine = new Engine();  // Engine created inside Car
    }

    void startCar() {
        engine.start();
        System.out.println("Car is running.");
    }
}

public class CompositionDemo {
    public static void main(String[] args) {
        Car car = new Car();
        car.startCar();
    }
}

```






## OUTPUT:

<img width="440" height="81" alt="image" src="https://github.com/user-attachments/assets/075d428f-051f-46f3-922a-42e52e7e12ba" />


## RESULT:
The program was executed successfully.
It demonstrated the concept of composition, where a Car object contains an Engine object.
When the car was started, the engine started first, showing strong dependency between the two objects.
