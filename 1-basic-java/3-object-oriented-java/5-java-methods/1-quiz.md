## Quiz

1. Which method signature would make a method that returns an ```int``` and takes in a ```String```?
    * ```public int countLetters(String message)```
    * public intReturn()
    * public String countLetters(int numLetters)
    * public void countLetters(String message, int numLetters)

2. Is there an error that will prevent this code from running?
    ```java
    class Coffee{

        public Coffee(){
        }

        public void stir(){
            String stirring = "Stirring the coffee!";
        }
        
        public static void main(String[] args){
            Coffee myCup = new Coffee();
            myCup.stir();
            System.out.println(stirring);
        }


    }
    ```
    * ```Yes! The variable stirring cannot be accessed in the main() method.```
    * Yes! The stir() method should be returning a value.
    * Yes! The constructor cannot be empty.
    * No.

3. When defining a method, the ```void``` keyword specifies which of the following?
    * The method returns default Java errors
    * ```The method does not return a value```
    * The method does not take any parameters
    * The method can run without being called

4. In this method definition, what does ```miles``` represent?
    ```java
    public void run(int miles) {
    }
    ```
    * A constructor
    * A Java specific keyword
    * An object belonging to the Miles class
    * ```A parameter of type int```

5. Fill in the code that will call the ```addSugar()``` method with 7 as an input.
    ```java
    public class Coffee {

        public Coffee(){
            
        }

        public void addSugar(int sugarCubes){
            System.out.println("Added " + sugarCubes + " sugar cubes!");
        }
        
        public static void main(String[] args){
            Coffee myCup = new Coffee()
            ________________
        }

    }
    ```
    * myCup.addSugar;
    * addSuggar(7);
    * int sugar = myCup.addSuggar();
    * ```myCup.addSuggar(7);```


6. Which line of code is NOT an example of calling a method?
    * "hello".equals("goodbye");
    * ```int sugarCubes = 7;```
    * System.out.println("More sugar please!");
    * myCoffeeCup.emptyCup();

7. An object named ```dalmatian``` belongs to the Spot class. Which of the following correctly calls the ```run``` method on ```dalmatian```?
    * Spot.dalmatian();
    * Spot.run();
    * ```dalmatian.run();```
    * Spot[run];








