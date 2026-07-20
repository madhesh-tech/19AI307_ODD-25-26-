# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:
Aliens scan DNA numbers:
If the DNA number is divisible by 2 and ends in 4, they accept it.
If the DNA number is divisible by 2 but ends in anything else, it’s a suspect.
If the DNA is odd, they reject it.
The program will print one of the following statements based on the input:
Accepted
Suspect
Rejected



## AIM:
To write a Java program that reads a DNA number and determines whether it is Accepted, Suspect, or Rejected based on given conditions.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3. Read the DNA number from the user.
4. Check if the number is divisible by 2 (i.e., even).
5. If it is even, check whether it ends with digit 4.
6. If the number is even and ends with 4 → print "Accepted".
7. If the number is even but does not end with 4 → print "Suspect".
8. If the number is odd → print "Rejected".


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
        if(n%2==0){
            if(n%10==4){
                System.out.print("Accepted");
            }
            else{
                System.out.print("Suspect");
            }
        }
        else{
            System.out.print("Rejected");
        }
    }
}
```





## OUTPUT:

<img width="1221" height="222" alt="image" src="https://github.com/user-attachments/assets/9ca710a4-70c7-4567-8933-a4246c69f2f6" />


## RESULT:

The program was executed successfully.
When the input DNA number 64 was entered, the program checked the conditions and correctly displayed the output “Accepted”.
Thus, the program works as expected and produces the correct result based on the given rules.

