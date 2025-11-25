# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:

Write a program to access a static variable using both class name and object.


<img width="398" height="150" alt="image" src="https://github.com/user-attachments/assets/3e8e2dbb-d13c-4b71-a89f-ed7d16273f1e" />

## AIM:

To write a Java program that demonstrates accessing a static variable using both the class name and an object of the class.


## ALGORITHM :

1.Start the program and declare a static variable num inside the class prog.

2.In the main() method, read an integer value from the user and assign it to the static variable num.

3.Access and print the static variable using the class name (prog.num).

4.Create an object of the class (prog obj = new prog();) and access the static variable using the object (obj.num).

5.Stop the program after displaying the values.

## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by: Thanika Sree B
RegisterNumber: 212222100055
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class prog {
    
    static int num;

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        num = sc.nextInt();
        System.out.println("Accessing using class name: " + prog.num);

        prog obj = new prog();
        System.out.println("Accessing using object: " + obj.num);

        sc.close();
    }
}
```

## OUTPUT:


<img width="797" height="299" alt="image" src="https://github.com/user-attachments/assets/c08d2470-58a0-4afa-a83d-a5773f7b2b11" />


## RESULT:

The program successfully shows that a static variable can be accessed directly via the class name and also through an object, producing the same value
