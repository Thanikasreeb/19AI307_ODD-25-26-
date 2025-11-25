# Ex.No:3(E) INNER CLASS

## QUESTION:
Write a Java program where the inner class is declared private and accessed through a method in the outer class.


<img width="461" height="155" alt="image" src="https://github.com/user-attachments/assets/ec641342-43c4-4ac1-8205-35f13d4f0915" />


## AIM:
To demonstrate accessing a private inner class in Java through a public method of the outer class.



## ALGORITHM :
1.Start the program.

2.Create a Scanner object to take integer input from the user.

3.Read an integer value from the user.

4.Create an object of the OuterClass.

5.Call the accessInner() method of OuterClass, passing the input value.

6.Inside accessInner(), create an object of the private inner class InnerClass.

7.Call the setData() method of InnerClass to store and print the value.

8.Close the scanner.

9.End the program.

## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by: Thanika Sree B
RegisterNumber: 212222100055 
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class OuterClass {
    
    private class InnerClass {
        private int data;

        void setData(int value) {
            data = value;
            System.out.println("Data set inside private inner class: " + data);
        }
    }

    void accessInner(int value) {
        InnerClass inner = new InnerClass();
        inner.setData(value);
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int value = sc.nextInt();
        
        OuterClass outer = new OuterClass();
        outer.accessInner(value);
        
        sc.close();
    }
}
```
## OUTPUT:


<img width="806" height="324" alt="image" src="https://github.com/user-attachments/assets/0aa25f30-4e76-44b0-8376-a9626d6a2557" />


## RESULT:
The private inner class is successfully invoked using an outer-class method.


