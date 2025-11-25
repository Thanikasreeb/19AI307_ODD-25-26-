# Ex.No:3(F) WRAPPER CLASS

## QUESTION:
Write a Java program that uses the Boolean wrapper class in conditional logic to determine a pass/fail result.


<img width="248" height="126" alt="image" src="https://github.com/user-attachments/assets/5da0fec6-acdd-41ee-9f50-1a2deeae222e" />


## AIM:
To demonstrate using the Boolean wrapper class in conditional logic to determine pass/fail in Java.



## ALGORITHM :
1.Start the program.

2.Create a Scanner object to take input from the user.

3.Read the integer value marks from the user.

4.Use the Boolean wrapper class to store the condition marks >= 50 in isPass.

5.If isPass is true, print "Result: Pass".

6.Otherwise, print "Result: Fail".

7.Close the scanner.

8.End the program.

## PROGRAM:
 ```
/*
Program to implement a Wrapper Class using Java
Developed by: Thanika Sree B
RegisterNumber: 212222100055
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int marks = sc.nextInt();

        Boolean isPass = marks >= 50;  

        if (isPass) {
            System.out.println("Result: Pass");
        } else {
            System.out.println("Result: Fail");
        }

        sc.close();
    }
}
```
## OUTPUT:


<img width="455" height="261" alt="image" src="https://github.com/user-attachments/assets/e09d1066-8436-4628-a0a8-639a5c2ce214" />


## RESULT:
The program evaluates a Boolean condition using Boolean and displays whether the student passed or failed.


