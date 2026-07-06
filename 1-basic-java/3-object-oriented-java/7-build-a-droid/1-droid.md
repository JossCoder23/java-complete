## Build A Droid
We’ve set up a robot workshop to build some droids. All that’s missing are the instructions on how to create the robots and what they’ll do.

Can we write a Java class to help?

We’ll need to define the state and behavior of the droids using instance fields and methods. Let’s get to work!

Code review available when you’re done

================================================================

1. The Droid.java file is empty.

    Start by defining the class ```Droid```.

    Don’t forget to include a ```main()``` method! You can leave it empty for now.

    We want a ```Droid``` object that has the following state:

    * name
    * battery level
    
    and the following behavior:

    * performing a task
    * stating its battery level

    SOLUTION

    **Droid.java**
    ```java
    public class Droid {
  
        public Droid() {
        }

        public static void main(String[] args) {
        }

    }
    ```

2. Declare an instance field called ```batteryLevel```. We want to store whole number values in this field.

    SOLUTION

    **Droid.java**
    ```java
    public class Droid {

        int batteryLevel;
  
        public Droid() {
        }

        public static void main(String[] args) {
        }

    }
    ```

3. Declare another instance field called ```name``` which will store our droid’s name.

    What type should this be?

    SOLUTION

    **Droid.java**
    ```java
    public class Droid {

        int batteryLevel;
        String name;
  
        public Droid() {
        }

        public static void main(String[] args) {
        }

    }
    ```

4. Create a constructor method for the ```Droid``` class.

    The method should have one parameter of ```String droidName```.

    SOLUTION

    **Droid.java**
    ```java
    public class Droid {

        int batteryLevel;
        String name;
  
        public Droid(String droidName) {
        }

        public static void main(String[] args) {
        }

    }
    ```

5. Inside the constructor, assign the parameter value of ```droidName``` to the appropriate instance field.

    Set the value of ```batteryLevel``` to ```100```. Every new instance of ```Droid``` will have a ```batteryLevel``` of ```100```.

    SOLUTION

    **Droid.java**
    ```java
    public class Droid {

        int batteryLevel = 100;
        String name;
  
        public Droid(String droidName) {
            name = droidName;
        }

        public static void main(String[] args) {
        }

    }
    ```

6. Inside ```main()```, create a ```new``` instance of ```Droid``` named ```"Codey"```.

    SOLUTION

    **Droid.java**
    ```java
    public class Droid {

        int batteryLevel = 100;
        String name;
        
        public Droid(String droidName) {
            name = droidName;
        }

        public static void main(String[] args) {
            Droid droid = new Droid("Codey");
        }

    }
    ```

7. Print out the variable using ```System.out.println()```.
    
    SOLUTION

    **Droid.java**
    ```java
    public class Droid {

        int batteryLevel = 100;
        String name;
        
        public Droid(String droidName) {
            name = droidName;
        }

        public static void main(String[] args) {
            Droid droid = new Droid("Codey");
            System.out.println(droid.name);
            System.out.println(droid.batteryLevel);
        }

    }
    ```

    OUTPUT:
    ```git
    Codey
    100
    ```

8. That output isn’t very informative!

    Define a ```toString()``` method within ```Droid```.

    The return type is ```String```.

    Inside ```toString()```, ```return``` a string that introduces the ```Droid``` using their name.

    Something like “Hello, I’m the droid: droidNameHere”

    SOLUTION

    **Droid.java**
    ```java
    public class Droid {

        int batteryLevel = 100;
        String name;
        
        public Droid(String droidName) {
            name = droidName;
        }

        public static void main(String[] args) {
            Droid droid = new Droid("Codey");
            System.out.println(droid.name);
            System.out.println(droid.batteryLevel);
        }

        public String toString(){
            return "Hello, I'm the droid: " + name;
        }

    }
    ```

9. Define a new method: ```performTask()```. This method should have a single parameter: ```String task```.

    This method does not return any value.

    SOLUTION

    **Droid.java**
    ```java
    public class Droid {

        int batteryLevel = 100;
        String name;
        
        public Droid(String droidName) {
            name = droidName;
        }

        public static void main(String[] args) {
            Droid droid = new Droid("Codey");
            System.out.println(droid.name);
            System.out.println(droid.batteryLevel);
        }

        public String toString(){
            return "Hello, I'm the droid: " + name;
        }

        public void performTask(String task) {
        }

    }
    ```

10. Inside ```performTask()```, print a statement like “```name``` is performing task: ```task```“.

    For example, ```codey.performTask("dancing");``` will print:
    ```git
    Codey is performing task: dancing
    ```

    SOLUTION

    **Droid.java**
    ```java
    public class Droid {

        int batteryLevel = 100;
        String name;
        
        public Droid(String droidName) {
            name = droidName;
        }

        public static void main(String[] args) {
            Droid droid = new Droid("Codey");
            System.out.println(droid.name);
            System.out.println(droid.batteryLevel);
        }

        public String toString(){
            return "Hello, I'm the droid: " + name;
        }

        public void performTask(String task) {
            System.out.println(name + " is performing task: " + task + ".");
        }

    }
    ```

11. Performing tasks is hard work. After the print statement, set ```batteryLevel``` to be ```10``` less than it was before.

    We’ll need to reassign the instance field to be the current value minus 10.

    SOLUTION

    **Droid.java**
    ```java
    public class Droid {

        int batteryLevel = 100;
        String name;
        
        public Droid(String droidName) {
            name = droidName;
        }

        public static void main(String[] args) {
            Droid droid = new Droid("Codey");
            System.out.println(droid.name);
            System.out.println(droid.batteryLevel);
        }

        public String toString(){
            return "Hello, I'm the droid: " + name;
        }

        public void performTask(String task) {
            System.out.println(name + " is performing task: " + task + ".");
            batteryLevel = batteryLevel - 10;
        }

    }
    ```
    

12. Have your ```Droid``` instance perform some tasks inside of ```main()```.

13. Create new instances and play around with methods. Here are some ideas to get you started:

    * Create a ```energyReport()``` method that prints the instance’s ```batteryLevel```.
    * Create another instance.
    * Create a method ```energyTransfer()``` that exchanges ```batteryLevel``` between instances.

    SOLUTION

    **Droid.java**
    ```java
    public class Droid {

        int batteryLevel = 100;
        String name;
        
        public Droid(String droidName) {
            name = droidName;
        }

        public static void main(String[] args) {
            Droid droid = new Droid("Codey");
            System.out.println(droid.name);
            System.out.println(droid.batteryLevel);
            droid.performTask("dance");
        }

        public String toString(){
            return "Hello, I'm the droid: " + name;
        }

        public void performTask(String task) {
            System.out.println(name + " is performing task: " + task + ".");
            batteryLevel = batteryLevel - 10;
            System.out.println("Your battery now is " + batteryLevel);
        }

        public void energyReport() {
            System.out.println("Your energy now is " + batteryLevel);
        }

        public void energyTransfer(int energy) {
            batteryLevel = batteryLevel + energy;
        }

    }
    ```