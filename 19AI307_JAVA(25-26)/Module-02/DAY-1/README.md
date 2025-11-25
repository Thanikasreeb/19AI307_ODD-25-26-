# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
Create a class Car with attributes brand, model, year. Create 2 objects and print their details.

<img width="292" height="173" alt="image" src="https://github.com/user-attachments/assets/0dc72141-5683-40a5-8866-7aae860b8a00" />

## AIM:

To create a Java class Car with attributes brand, model, and year, and display the details of two car objects.


## ALGORITHM :
1.Start the program and define a class Car with attributes brand, model, and year.

2.Create a constructor in the Car class to initialize the attributes.

3.Define a display method in the Car class to print the car details with a label.

4.In the main method, create two Car objects with different attribute values.

5.Call the display method for each object to print their details and stop the program.

## PROGRAM:
 ```
/*
Program to implement a Class and Objects using Java
Developed by: Thanika Sree B
RegisterNumber: 212222100055
*/
```

## SOURCE CODE:
```
class Car {
    String brand;
    String model;
    int year;

    Car(String brand, String model, int year) {
        this.brand = brand;
        this.model = model;
        this.year = year;
    }

    public void display(String label) {
        System.out.println(label + ": " + brand + " " + model + " " + year);
    }
}

public class CarDemo {
    public static void main(String[] args) {

        Car car1 = new Car("Toyota", "Innova", 2022);
        Car car2 = new Car("Hyundai", "i20", 2021);

        car1.display("Car 1");
        car2.display("Car 2");
    }
}
```

## OUTPUT:
<img width="695" height="186" alt="image" src="https://github.com/user-attachments/assets/95ccdae1-ac3d-4965-a2b1-d99d371f36d0" />



## RESULT:
The program successfully creates two Car objects and prints their brand, model, and year information.


