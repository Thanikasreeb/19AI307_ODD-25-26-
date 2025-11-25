# Ex.No:4(D) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:
Build a simple Air Traffic Control System where multiple Airplane objects request landing through a central mediator.


<img width="498" height="323" alt="image" src="https://github.com/user-attachments/assets/656065b4-dcf5-42a5-913b-a832c35f94d4" />


## AIM:

To implement a Mediator design pattern where an Air Traffic Control (ATC) system coordinates landing requests from multiple airplanes.


## ALGORITHM :

1.Read the number of airplanes and whether the runway should be released after landing.

2.Create an AirTrafficControl mediator.

3.For each airplane:
```

  =>Create an Airplane object linked to the ATC.

  =>Request landing through the mediator.
```
4.If landing is allowed and release flag is true, release the runway.

5.Display landing status messages for each airplane.

6.End the program.

## PROGRAM:
 ```
/*
Program to implement a Behaviour Pattern using Java
Developed by: Thanika Sree B
RegisterNumber: 212222100055 
*/
```

## SOURCE CODE:
```
import java.util.*;

class AirTrafficControl {
    private boolean runwayFree = true;

    public boolean requestLanding(Airplane airplane) {
        if (runwayFree) {
            runwayFree = false;
            System.out.println(airplane.getName() + " granted landing.");
            return true;
        } else {
            System.out.println(airplane.getName() + " denied landing. Runway busy.");
            return false;
        }
    }

    public void releaseRunway() {
        runwayFree = true;
    }
}

class Airplane {
    private String name;
    private AirTrafficControl control;

    public Airplane(String name, AirTrafficControl control) {
        this.name = name;
        this.control = control;
    }

    public String getName() {
        return name;
    }

    public void requestLanding(boolean releaseAfterLanding) {
        boolean allowed = control.requestLanding(this);
        if (allowed) {
            System.out.println(name + " landed successfully.");
            if (releaseAfterLanding) {
                control.releaseRunway();
            }
        }
    }
}

public class AirTrafficSystem {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        AirTrafficControl control = new AirTrafficControl();

        int n = Integer.parseInt(sc.nextLine()); // number of airplanes
        boolean release = sc.nextLine().equalsIgnoreCase("true"); // release after landing?

        List<Airplane> airplanes = new ArrayList<>();
        for (int i = 0; i < n; i++) {
            String name = sc.nextLine();
            airplanes.add(new Airplane(name, control));
        }

        for (Airplane plane : airplanes) {
            plane.requestLanding(release);
        }

        sc.close();
    }
}
```

## OUTPUT:


<img width="855" height="429" alt="image" src="https://github.com/user-attachments/assets/bedbe1cc-2323-42de-a4dc-ccd4b4e3d22c" />

## RESULT:
Airplanes communicate through the ATC mediator, which manages landing permissions, demonstrating centralized control without direct airplane-to-airplane communication.
