## Quiz

1. The following class definition requires a parameter to be passed in to the constructor in order to make an instance.
    ```java
    public class Dinosaur {
        boolean isExtinct;
        
        public Dinosaur(boolean extinct) {
            isExtinct = extinct;
        }
        
        public static void main(String[] args) {
            // program tasks
        }
    }
    ```
    * ```True```
    * False

2. Complete the following class definition for a ```Bank``` class.
    ```java
    public ________ Bank {
        public static void main(String[] args) {
            // program tasks
        }
    }
    ```
    * ```class```
    * void
    * function
    * static

3. Instances of a Java class represent the real world with what two qualities?
    * ```State and behavior.```
    * State and history.
    * History and consequences.
    * Behavior and history.

4. Every Java program contains at least one class.
    * False.
    * ```True.```

5. What is the signature of the following constructor?
    ```java
    public class Bug {

        String name;
        boolean ableToFly;
        int numberOfLegs;

        public Bug(String bugName, boolean canFly, int numLegs) {
            name = bugName;
            ableToFly = canFly;
            numberOfLegs = numLegs;
        }

        public static void main(String[] args) {
            Bug ladybug = new Bug("Lady Bug", true, 6);
        }

    }
    ```
    * Bug(name, ableToFly, numberOfLegs)
    * Bug(bugName String, canFly boolean, numLegs int)
    * Bug(double, String, boolean)
    * ```Bug(String bugName, boolean canFly, int numLegs)```

6. Why will the following program produce an error?
    ```java
    public class Shelf {

        String material;
        
        public Shelf() {
        
        }
        
        public static void main(String[] args) {
            Shelf bureau = new Shelf("pine");
        }

    }
    ```
    * ```The constructor does not have a parameter listed.```
    * No constructor method has been declared.
    * The instance field has an incorrect declaration.
    * bureau has the incorrect type.

7. What is the data type of the variable ```hedwig```?
    ```java
    public class Owl {

        String speak;
        boolean nocturnal;

        public Owl() {
            speak = "Hoot";
            nocturnal = true;
        }  

        public static void main(String[] args) {
            Owl hedwig = new Owl();
        }

    }
    ```
    * hedwig
    * ```Owl```
    * nocturnal
    * speak

8. The ```Bank``` class has one instance field: ```branchLocationCount```.

    Complete the constructor method for this class. 
    ```java
    public class Bank {
        int branchLocationCount;
        
        public Bank( _______ ) {
            branchLocationCount = numLocations;
        }
        public static void main(String[] args) {
            // program tasks
        }
    }
    ```
    * double numLocations
    * String numLocations
    * boolean numLocations
    * ```int numLocations```

9. An instance is declared in the ```main()``` function. Complete the method call.
    ```java
    public class Window {

        boolean isOpen;
        int height;
        int width;
        
        public Window(boolean open, int windowHeight, int windowWidth) {
            isOpen = open;
            height = windowHeight;
            width = windowWidth;
        }
        
        public static void main(String[] args) {
            Window bedroomWindow = _____________________
        }

    }
    ```
    * new Window(72, false, 34);
    * ```new Window(true, 72, 34);```
    * new Window(true, 72);

10. The main() method is automatically run when the .class file is executed.
    * ```True.```
    * False.

