## Quizz

1. Fill in the code to print the array so that its actual values display, instead of the memory address.

    ```java
    import java.util.Arrays;

    class Restaurant{
    
        public void printSpecials(){
            String[] specials = {"Chicken Mountain", "Lake of Broth", "Wishbone Tower"};
            System.out.println(________);
        }
        
        public static void main(String[] args){
            Restaurant chickenKitchen = new Restaurant();
            chickenKitchen.printSpecials();
        }
    }
    ```
    * specials.toString()
    * specials.length
    * ```Arrays.toString(specials)```
    * specials[0]
    * specials

2. Fill in the code to set ```taxRates``` to be an empty array of size 10, holding doubles.

    ```java
    class Tax {

        public static void main(String[] args){
            double[] taxRates = _____________;
        }

    }
    ```
    * ```new double[10]```
    * Arrays.toString[10]
    * taxRates

3. What property holds the number of elements in an array?
    * .numElements
    * .toString
    * .size
    * ```.length```

4. What type is the following object?
    ```java
    {4, 5, 2, 1, 7}
    ```
    * ```int[]```
    * java.util.Arrays
    * int
    * String[]

5. How would you access the element "Gorgeous" of the following array?

    ```java
    String[] tsSongs = {"Delicate", "Gorgeous", "All Too Well", "Hey Stephen"};
    ```

    * toSongs[2]
    * ```toSongs[1]```
    * String[1]
    * toSongs["Gorgeous"]

6. What would be printed out by the following code if a user ran the command:

    **CMD**
    ```git
    java Restaurant 6 vegetarians
    ```

    **Restaurant.java**
    ```java
    class Restaurant{
    
        public static void main(String[] args){
            System.out.println("Table for a party of " + args[0]);
            if(args[1].equals("vegetarians")){
            // Do something for vegetarian eaters
            }
            else {
            // Do something for meat eaters
            }
        }

    }
    ```

    * Table for a party of Restaurant
    * ```Table for a party of 6```
    * Error – args is not defined
    * Table for a party of vegetarians