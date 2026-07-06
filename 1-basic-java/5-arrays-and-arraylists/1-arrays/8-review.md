## Review
We have now seen how to store a list of values in arrays. We can use this knowledge to make organized programs with more complex variables.

Throughout the lesson, we have learned about:

* Creating arrays explicitly, using ```{``` and ```}```.
* Accessing an index of an array using ```[``` and ```]```.
* Creating empty arrays of a certain size, and filling the indices one by one.
* Getting the length of an array using ```length```.
* Using the argument array ```args``` that is passed into the ```main()``` method of a class.

**Main.java**

```java
import java.util.Arrays;

public class Main {
    public static void main(String[] args) {

      
    }
}
```

EXERCISE:
1. Let’s practice what we’ve learned throughout this lesson.

    First, inside ```main()``` in **Main.java**, create a String array ```students``` and initialize it with these elements:

    * “Sade”
    * “Alexus”
    * “Sam”
    * “Koma”

    SOLUTION:

    ```java
    import java.util.Arrays;

    public class Main {

        public static void main(String[] args) {
            String[] students = {"Sade", "Alexus", "Sam", "Koma"};    
        }

    }
    ```

2. Now, to store the scores of the recent math test, create an array called ```mathScores``` of type ```int``` and set it to an empty array of size 
    
    Each spot in this array will represent the math test score of the student in the corresponding spot in the ```students``` array. For example: ```mathScores[2]``` will represent the score ```students[2]``` which is “Sam”.

    SOLUTION:

    ```java
    import java.util.Arrays;

    public class Main {

        public static void main(String[] args) {
            String[] students = {"Sade", "Alexus", "Sam", "Koma"};  
            int[] mathScores = new int[4]; 
        }

    }
    ```

3. The students had the following scores on their most recent math test:

    * Sade got a 64
    * Sam got a 76
    * Alexus got a 57
    * Koma got a 98

    Store these values in the appropriate spots in the ```mathScores``` array.

    SOLUTION:

    ```java
    import java.util.Arrays;

    public class Main {

        public static void main(String[] args) {

            String[] students = {"Sade", "Alexus", "Sam", "Koma"};    
            int[] mathScores = new int[4];

            mathScores[0] = 64;
            mathScores[1] = 57;
            mathScores[2] = 76;
            mathScores[3] = 98;

        }

    }
    ```

4. Print out the math scores of each student. Print each score on a new line and use the following format:

    *Scott: 88*

    SOLUTION:

    ```java
    import java.util.Arrays;

    public class Main {

        public static void main(String[] args) {

            String[] students = {"Sade", "Alexus", "Sam", "Koma"};    
            int[] mathScores = new int[4];

            mathScores[0] = 64;
            mathScores[1] = 57;
            mathScores[2] = 76;
            mathScores[3] = 98;

            System.out.println(students[0] + ": " + mathScores[0]);
            System.out.println(students[1] + ": " + mathScores[1]);
            System.out.println(students[2] + ": " + mathScores[2]);
            System.out.println(students[3] + ": " + mathScores[3]);

        }

    }
    ```