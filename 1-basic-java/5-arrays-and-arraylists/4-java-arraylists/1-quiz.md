## Quizz 
1. What will the following code print?
    ```java
    import java.util.ArrayList;

    public class Temperatures {

        public static void main(String[] args) {
            
            ArrayList<Integer> temperatures = new ArrayList<Integer>();
            
            temperatures.add(78);
            temperatures.add(67);
            temperatures.add(89);
            temperatures.add(94);
            
            System.out.println(temperatures.get(2));
            
        }
    }
    ```
    * 94
    * ```89```
    * 2
    * 67

2. What does the following code print?
    ```java
    import java.util.ArrayList;

    public class RatingMachine {
    
        public static void main(String[] args) {
            
            ArrayList<Double> ratings = new ArrayList<Double>();
            
            ratings.add(1.7);
            ratings.add(2.5);
            ratings.add(3.5);
            ratings.remove(1);
            
            System.out.println(ratings.get(1));
            
        }
    }
    ```
    * Error
    * 1.7
    * ```3.5```
    * 2.5

3. Fill in the blank to declare the ```ArrayList``` to hold the correct type.

    ```java
    import java.util.ArrayList;

    public class Gradebook{
    
        public static void main(String[] args){
            
            ArrayList __________ quizGrades;
            // we will add the values 96, 87, and 46 later in the method
            
        }
    }
    ```
    * ```<Integer>``` (this)
    * ```[int]```
    * ```<Char>```
    * ```[Integer]```
    * ```char>```
    * ```<int>```

4. What method can you use to find the position of a specific element in an ```ArrayList```?
    * size()
    * get()
    * remove()
    * ```indexOf()```

5. Fill in the code to print out how many elements are stored in the grades ArrayList.
    ```java
    import java.util.ArrayList;

    public class TemperaturesC {
    
        public static void main(String[] args) {
            
            ArrayList<Char> grades = new ArrayList<Char>();
            grades.add('B');
            grades.add('B');
            grades.add('D');
            
            System.out.println(_____________);

        }

    }
    ```
    * grades.size
    * grades.length()
    * ```grades.size()```
    * grades.length

6. What will the ```ArrayList usernames``` hold after this code runs?
    ```java
    import java.util.ArrayList;

    public class LogIn {
    
        public static void main(String[] args) {
            
            ArrayList<String> usernames = new ArrayList<String>();
            
            usernames.add("teraCoder");
            usernames.add("javaKnight");
            
        }

    }
    ```
    * This code has an error.
    * It will be empty.
    * ["javaKnight", "teraCoder"]
    * ```["teraCoder", "javaKnight"]```

7. What will the ```ArrayList kidsMovies``` hold after the code is run?
    ```java
    import java.util.ArrayList;

    public class Rankings {
    
        public static void main(String[] args) {
            
            ArrayList<String> kidsMovies = new ArrayList<String>();
            
            kidsMovies.add("Moana");
            kidsMovies.add("Up");
            kidsMovies.add("WALL-E");
            
            kidsMovies.set(0, "Babe");
            
        }

    }
    ```
    * ```["Babe", "Up", "WALL-E"]```
    * ["Babe", "Moana", "Up", "WALL-E"]
    * ["Moana", "Up", "WALL-E", "Babe"]
    * ["Babe", "Moana", "Up"]