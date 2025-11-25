# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:

Write a program that reads two integers and divides the first by the second. Handle the case when division by zero occurs.


## AIM:
## ALGORITHM :
1.Start the program.

2.Create a Scanner object to take user input.

3.Read two integers a and b from the user.

4.Enter a try block and attempt to divide a by b.

5.If division succeeds, display the result.

6.If an ArithmeticException occurs (such as division by zero), move to the catch block.

7.In the catch block, print "Error: Division by zero".

8.End the program.

## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by: Thanika Sree B
RegisterNumber: 212222100055 
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
public class Main{
    public static void main(String args[]){
        Scanner sc = new Scanner(System.in);
        try{
            int a = sc.nextInt();
            int b = sc.nextInt();
            System.out.println("Result: "+a/b);
        }
        catch (ArithmeticException e){
            System.out.println("Error: Division by zero");
        }
    }
}
```

## OUTPUT:


<img width="719" height="319" alt="image" src="https://github.com/user-attachments/assets/aec30775-8be9-43a1-9965-f341157defc7" />


## RESULT:
The program successfully Completed.


