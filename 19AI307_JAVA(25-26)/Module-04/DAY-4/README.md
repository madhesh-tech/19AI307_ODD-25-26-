# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:

You’re creating a cross-platform UI tool using the Abstract Factory pattern. Implement factories to create Button and Checkbox for "dark" and "light" themes. Let the user choose the theme, then generate UI components and display their types

## AIM:

To implement the Abstract Factory Pattern to generate UI components (Button and Checkbox) for two themes—Dark and Light—based on the user’s choice. The program should create appropriate objects and display their types.

## ALGORITHM :

1. Start the program.
2. Create abstract product interfaces: Button and Checkbox.
3. Create concrete classes for both themes:
  DarkButton, LightButton
  DarkCheckbox, LightCheckbox
4. Create an abstract factory interface UIFactory with methods to create Button and Checkbox.
5. Implement two factories: DarkFactory and LightFactory.
6. In main(), read the user's theme choice (“dark” or “light”).
7. Based on the choice, instantiate the appropriate factory, create components, and display messages.
8. End the program.



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

// === Abstract Products ===
interface Button {
    void render();
}

interface Checkbox {
    void render();
}

// === Concrete Products for Dark Theme ===
class DarkButton implements Button {
    public void render() {
        System.out.println("Dark Button created");
    }
}

class DarkCheckbox implements Checkbox {
    public void render() {
        System.out.println("Dark Checkbox created");
    }
}

// === Concrete Products for Light Theme ===
class LightButton implements Button {
    public void render() {
        System.out.println("Light Button created");
    }
}

class LightCheckbox implements Checkbox {
    public void render() {
        System.out.println("Light Checkbox created");
    }
}

// === Abstract Factory ===
interface UIFactory {
    Button createButton();
    Checkbox createCheckbox();
}

// === Concrete Factories ===
class DarkThemeFactory implements UIFactory {
    public Button createButton() {
        return new DarkButton();
    }

    public Checkbox createCheckbox() {
        return new DarkCheckbox();
    }
}

class LightThemeFactory implements UIFactory {
    public Button createButton() {
        return new LightButton();
    }

    public Checkbox createCheckbox() {
        return new LightCheckbox();
    }
}

// === Client ===
public class AbstractFactoryDemo {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        while (sc.hasNextLine()) {
            String theme = sc.nextLine().trim().toLowerCase();
            if (theme.isEmpty()) continue;

            UIFactory factory = null;

            if (theme.equals("dark")) {
                factory = new DarkThemeFactory();
            } else if (theme.equals("light")) {
                factory = new LightThemeFactory();
            } else {
                System.out.println("Invalid theme");
                continue; // Skip component creation
            }

            Button button = factory.createButton();
            Checkbox checkbox = factory.createCheckbox();

            button.render();
            checkbox.render();
            System.out.println(); // spacing between runs
        }

        sc.close();
    }
}

```



## OUTPUT:

<img width="1255" height="257" alt="image" src="https://github.com/user-attachments/assets/8890975e-6547-4c80-a8c7-6a6d9d556b10" />


## RESULT:

The program executed successfully using the Abstract Factory design pattern.
Based on the user’s theme selection, the appropriate UI factory (Dark or Light) was created.
The factory then generated the corresponding Button and Checkbox objects.
The program printed the type of UI components created (for example, “Dark Button created” and “Dark Checkbox created”).
