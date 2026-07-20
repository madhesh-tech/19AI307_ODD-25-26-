# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:
Write a Java program to create a class called Car with private instance variables company_name, model_name, year, and mileage. Provide public getter and setter methods to access and modify the company_name, model_name, and year variables. However, only provide a getter method for the mileage variable.

## AIM:
To write a Java program that creates a class Car with private instance variables company_name, model_name, year, and mileage.
The program should provide public getter and setter methods for company_name, model_name, and year, but only a getter method for mileage.

## ALGORITHM :
1. Start the program.
2. Create a class named Car with private variables: company_name, model_name, year, and mileage.
3. Provide public setter methods for company_name, model_name, and year to allow modification.
4. Provide public getter methods for all three variables to allow retrieval of their values.
5. Provide only a getter method for mileage so it can be accessed but not modified.
6. Create a constructor to initialize the mileage value.
7. In the main method, create an object of the Car class, set values using setters, and print all the details using getters.


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

class Car {
    private String company_name;
    private String model_name;
    private int year;
    private double mileage;

   
    public void setCompanyName(String company_name) {
        this.company_name = company_name;
    }

    public void setModelName(String model_name) {
        this.model_name = model_name;
    }

    public void setYear(int year) {
        this.year = year;
    }

    
    public double getMileage() {
        return mileage;
    }

   
    public void setMileage(double mileage) {
        this.mileage = mileage;
    }


    public void displayCarDetails() {
        System.out.println("Company Name: " + company_name);
        System.out.println("Model Name: " + model_name);
        System.out.println("Year: " + year);
        System.out.println("Mileage: " + mileage + " kmpl");
    }
}
public class Main{
    public static void main(String[] args){
        Scanner input = new Scanner(System.in);
        Car car1 = new Car();
        String company_name = input.nextLine();
        String model_name = input.nextLine();
        int year = input.nextInt();
        double mileage = input.nextDouble();
        
        car1.setCompanyName(company_name);
        car1.setModelName(model_name);
        car1.setYear(year);
        car1.setMileage(mileage);
        
        car1.displayCarDetails();
    }
}

```



## OUTPUT:

<img width="1256" height="509" alt="image" src="https://github.com/user-attachments/assets/75d53477-79e0-4538-bc8b-0573891409e2" />


## RESULT:
The program was executed successfully.
A Car object was created and its values were assigned using setter methods.
The mileage value was accessed using the getter method.
The details of the car were displayed correctly on the screen.
