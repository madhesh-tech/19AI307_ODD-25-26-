# Ex.No:3(D)    INTERFACE 

## QUESTION:
You are programming bots that analyze weather data. Each bot must implement a common interface and give a prediction.


 Bot Types:

SunBot: Predicts "HOT" if temperature > 30, else "MODERATE".

RainBot: Predicts "COLD" if temperature < 20, else "WARM".


## AIM:

To develop a Java program that uses interfaces to implement different types of weather-predicting bots.
Each bot predicts weather conditions based on temperature using its own logic.

## ALGORITHM :

1. Start the program.
2. Define an interface WeatherBot with the abstract method:
  String predict(int temperature);
3. Create class SunBot that implements WeatherBot.
  If temperature > 30 → return "HOT"
  Else → return "MODERATE"
4. Create class RainBot that implements WeatherBot.
  If temperature < 20 → return "COLD"
  Else → return "WARM"
5. In main() method:
  Read temperature
  Read botType (1 = SunBot, 2 = RainBot)
6. Based on botType, create appropriate bot object.
7. Call predict() method using the object.
8. Display the prediction.
9. Stop the program.

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

interface WeatherBot {
    String predict(int temperature);
}

class SunBot implements WeatherBot {
    public String predict(int temperature) {
        return temperature > 30 ? "HOT" : "MODERATE";
    }
}

class RainBot implements WeatherBot {
    public String predict(int temperature) {
        return temperature < 20 ? "COLD" : "WARM";
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int temperature = sc.nextInt();
        int botType = sc.nextInt();

        WeatherBot bot;
        if (botType == 1) {
            bot = new SunBot();
        } else {
            bot = new RainBot();
        }

        System.out.println(bot.predict(temperature));
    }
}

```





## OUTPUT:

<img width="1257" height="139" alt="image" src="https://github.com/user-attachments/assets/b5b21760-ba66-4812-81ea-3c0afe6f92d5" />


## RESULT:
Thus, the program successfully creates two weather-prediction bots using an interface, accepts user input, and outputs the correct weather prediction based on the selected bot.

