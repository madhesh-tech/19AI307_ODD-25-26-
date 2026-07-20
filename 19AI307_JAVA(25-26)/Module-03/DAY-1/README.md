# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:
Create a Super class Person with fields name and age. Create a subclass Student that inherits from Person and adds a field marks (integer). Implement a method in Student called calculateGrade() which returns the grade based on the marks:

Marks ≥ 90: Grade A

Marks ≥ 75 and < 90: Grade B

Marks ≥ 50 and < 75: Grade C

Marks < 50: Grade F

## AIM:
To create a superclass Person with fields name and age, and a subclass Student that inherits from Person and adds a marks field.
The Student class should include a method calculateGrade() that returns a grade based on the marks.

## ALGORITHM :
1. Start the program.
2. Create a superclass Person with fields name and age.
3. Create a subclass Student that extends Person and adds an extra field marks.
4. Inside Student, implement the method calculateGrade() to determine the grade based on marks.
5. In the main method, create a Student object.
6. Assign values to name, age, and marks.
7. Call the calculateGrade() method and print the student's details along with the grade.

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

class Person {
    String name;
    int age;
    Person(String name, int age) {
        this.name = name;
        this.age = age;
    }
    void displayDetails() {
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
    }
}
class Student extends Person {
    int marks;
    Student(String name, int age, int marks) {
        super(name, age); 
        this.marks = marks;
    }
    String calculateGrade() {
        if (marks >= 90) {
            return "Grade: A";
        } else if (marks >= 75) {
            return "Grade: B";
        } else if (marks >= 50) {
            return "Grade: C";
        } else {
            return "Grade: F";
        }
    }

    void displayStudentDetails() {
        displayDetails(); 
        System.out.println("Marks: " + marks);
        System.out.println(calculateGrade());
    }
}
public class Main {
    public static void main(String[] args) {
        Scanner input=new Scanner(System.in);
        String name=input.nextLine();
        int age=input.nextInt();
        int mark=input.nextInt();
        Student s1 = new Student(name,age,mark);

        s1.displayStudentDetails();
        System.out.println();
    }
}

```





## OUTPUT:

<img width="1257" height="491" alt="image" src="https://github.com/user-attachments/assets/ee6f6295-c69b-4dfb-b75a-f9747f429019" />


## RESULT:

The program was executed successfully.
A Student object was created with the details: name, age, and marks.
The calculateGrade() method evaluated the marks and returned the correct grade based on the grading rules.
