# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:
Write a Java program to calculate the factorial of a number using a for loop. The factorial of n is the product of all positive integers less than or equal to n.

<img width="273" height="132" alt="image" src="https://github.com/user-attachments/assets/ef6f3d44-9bba-4a9e-90a0-757a79fa9c3b" />


## AIM:
To write a Java program that calculates the factorial of a given number using a for loop.



## ALGORITHM :
```
Start the program and read an integer n from the user.

Initialize a variable factorial to 1 to store the result.

Use a for loop from 1 to n, multiplying factorial by the loop counter in each iteration.

After the loop ends, print the value of factorial as the factorial of n.

Stop the program.
```

## PROGRAM:
 ```
/*
Program to implement a Looping Statement using Java
Developed by: Thanika Sree B
RegisterNumber: 212222100055
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class FactorialCalculator {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();  
        long factorial = 1;

        for (int i = 1; i <= n; i++) {
            factorial *= i;
        }

        System.out.println("Factorial of " + n + " is: " + factorial);
    }
}
```
## OUTPUT:

<img width="749" height="256" alt="image" src="https://github.com/user-attachments/assets/2f16e1e4-638c-4d8a-82e2-24aa4768437c" />


## RESULT:
The program successfully computes and displays the factorial value of the entered number.


