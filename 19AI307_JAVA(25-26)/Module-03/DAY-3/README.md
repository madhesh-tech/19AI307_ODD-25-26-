# Ex.No:3(C) ABSTRACTION

## QUESTION:
Create abstract class BankAccount with method calculateInterest(). Extend it in SavingsAccount and FixedDepositAccount.

Input Format:

First line: 1 for SavingsAccount, 2 for FixedDepositAccount
- If 1: next line → balance (double)
- If 2: next line → amount (double) and years (int)

Output Format:

- A single line showing interest earned rounded to 2 decimal places.


## AIM:
To write a Java program that demonstrates abstraction using an abstract class BankAccount with an abstract method calculateInterest(), and two subclasses SavingsAccount and FixedDepositAccount that calculate interest based on different rules.

## ALGORITHM :

1. Start the program.
2. Create an abstract class BankAccount with an abstract method calculateInterest().
3. Create a subclass SavingsAccount that extends BankAccount and calculates interest at 4% of the balance.
4. Create another subclass FixedDepositAccount that calculates interest at 7% per year on the deposited amount.
5. Read user input:
  If input is 1, read balance and create a SavingsAccount object.
  If input is 2, read deposit amount and number of years and create a FixedDepositAccount object.
6. Call the calculateInterest() method using the created object.
7. Display the interest earned rounded to two decimal places.


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
abstract class BankAccount{
    double interest;
    abstract void calculateInterest();
}
class SavingsAccount extends BankAccount{
    double balance;
    void calculateInterest(){
        double interest = balance * 0.04;
        System.out.printf("%.2f",interest);
    }
}
class FixedDepositAccount extends BankAccount{
    double amount;
    int years;
    void calculateInterest(){
        double interest = amount * years * 0.07;
        System.out.printf("%.2f",interest);
    }
}
public class Main{
    public static void main(String[] args){
        Scanner input = new Scanner(System.in);
        int val = input.nextInt();
        if(val == 1){
            SavingsAccount obj = new SavingsAccount();
            obj.balance = input.nextDouble();
            obj.calculateInterest();
        }
        else if(val == 2){
            FixedDepositAccount obj = new FixedDepositAccount();
            obj.amount = input.nextDouble();
            obj.years = input.nextInt();
            obj.calculateInterest();
        }
    }
}
```




## OUTPUT:

<img width="1262" height="317" alt="image" src="https://github.com/user-attachments/assets/43f1ed14-6464-470d-996d-a0116d0d0607" />


## RESULT:
The program was executed successfully.
Depending on the user’s choice, either a SavingsAccount or a FixedDepositAccount object was created.
The calculateInterest() method was called through runtime polymorphism, and the correct interest amount was displayed, rounded to two decimal places.
