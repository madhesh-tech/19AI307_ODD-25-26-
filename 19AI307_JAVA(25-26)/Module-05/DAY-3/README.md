# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:
Write a program to overwrite the content of a file.


## AIM:
To write a Java program that overwrites the existing content of a file using FileWriter.

## ALGORITHM :
1. Start the program.
2. Create a Scanner object to read user input.
3. Read a line of text from the user.
4. Create a FileWriter object in non-append mode (default), which overwrites the file.
5. Write the input text to the file.
6. Close the writer.
7. Display a success message.
9. End the program.

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
import java.io.*;
public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        String message = sc.nextLine();
        try(FileWriter fw = new FileWriter("example.txt")){
            fw.write(message);
            System.out.println("File content overwritten successfully.");
        }
        catch(IOException e){
            System.out.println(e.getMessage());
        }
    }
}
```






## OUTPUT:
<img width="1263" height="183" alt="image" src="https://github.com/user-attachments/assets/85079d0d-17f4-4b27-8908-41b9407ee5ec" />



## RESULT:
When the user enters "Saveetha Engineering College",
the program overwrites the existing content of the file output.txt with this new text and displays:
"File content overwritten successfully.
Thus, the file content is replaced successfully.
