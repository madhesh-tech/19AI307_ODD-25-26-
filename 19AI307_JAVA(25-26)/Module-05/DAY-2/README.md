# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION 

## QUESTION:
Write a Java program to serialize a collection of objects (like ArrayList<Student>) into a file.


## AIM:
To write a Java program that serializes a collection of objects (ArrayList of Student objects) into a file and later deserializes the same file to retrieve the objects.

## ALGORITHM :
1. Start the program.
2. Create a Student class that implements Serializable.
3. Read the number of students from the user.
4. For each student, read ID, Name, and Marks.
5. Store the student objects in an ArrayList<Student>.
6. Create FileOutputStream and wrap it inside ObjectOutputStream.
7. Write the ArrayList to the file using writeObject().
8. Close the output streams.
     Deserialization
9. Create FileInputStream and wrap it inside ObjectInputStream.
10. Read back the ArrayList using readObject().
11. Display all deserialized student objects.
12. End the program.




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
import java.io.*;
import java.util.*;

// Student class must implement Serializable
class Student implements Serializable {
    private static final long serialVersionUID = 1L;

    private int id;
    private String name;
    private double marks;

    public Student(int id, String name, double marks) {
        this.id = id;
        this.name = name;
        this.marks = marks;
    }

    @Override
    public String toString() {
        return "Student{id=" + id + ", name='" + name + "', marks=" + marks + "}";
    }
}

public class StudentSerializationUserInput {

    // Serialize list of students
    public static void serializeStudents(List<Student> students, String fileName) {
        try (ObjectOutputStream oos = new ObjectOutputStream(new FileOutputStream(fileName))) {
            oos.writeObject(students);
            System.out.println("Students serialized successfully into: " + fileName);
        } catch (IOException e) {
            System.out.println("Error during serialization: " + e.getMessage());
        }
    }

    // Deserialize list of students
    @SuppressWarnings("unchecked")
    public static List<Student> deserializeStudents(String fileName) {
        List<Student> students = null;
        try (ObjectInputStream ois = new ObjectInputStream(new FileInputStream(fileName))) {
            students = (List<Student>) ois.readObject();
            System.out.println("Students deserialized successfully from: " + fileName);
        } catch (IOException | ClassNotFoundException e) {
            System.out.println("Error during deserialization: " + e.getMessage());
        }
        return students;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        List<Student> students = new ArrayList<>();

        int n = scanner.nextInt();
        scanner.nextLine(); // consume newline

        for(int i=0;i<n;i++){
            int id = scanner.nextInt();
            scanner.nextLine();
            String name = scanner.nextLine();
            double marks = scanner.nextDouble();
            scanner.nextLine();
            
            students.add(new Student(id,name,marks));
        }
        
        String filename = "students.dat";
        serializeStudents(students,filename);
        List<Student> deserializedStudents = deserializeStudents(filename);
        // Write your code here

        // Display deserialized data
        if (deserializedStudents != null) {
            System.out.println("\nDeserialized Students:");
            for (Student s : deserializedStudents) {
                System.out.println(s);
            }
        }

        scanner.close();
    }
}

```


## OUTPUT:

<img width="1211" height="726" alt="image" src="https://github.com/user-attachments/assets/c1d4defa-d26f-4549-a664-068e1c93dca7" />


## RESULT:
The program successfully:
Reads the student details from the user.
Serializes (saves) the ArrayList of Student objects into the file students.dat.
Deserializes (retrieves) the ArrayList from the file.
Displays the student details correctly after deserialization.
Thus, serialization and deserialization of a collection of objects were performed successfully.
