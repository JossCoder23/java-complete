## 2D Array Review

Let’s review the concepts we have learned throughout this lesson.

Arrays are objects in Java, we can have arrays of objects, therefore we can also have arrays of arrays. This is the way 2D arrays are structured in Java.

We can declare and initialize 2D arrays in a few different ways depending on the situation:

```java
// Declaring without initializing
int[][] intTwoD;

// Initializing an empty 2D array which has already been declared
intTwoD = new int[5][5];

// Declaring and initializing an empty 2D array at once
String[][] stringData = new String[3][6];

// Declaring and initializing a 2D array using initializer lists
double[][] doubleValues = {{1.5, 2.6, 3.7}, {7.5, 6.4, 5.3}, {9.8,  8.7, 7.6}, {3.6, 5.7, 7.8}};

// Initializing a 2D array using initializer lists after it has already been declared, or already contains data;
char[][] letters = new char[100][250];
letters = new char[][]{{'a', 'b', 'c'}, {'d', 'e', 'f'}};
```

We retrieve elements in a 2D array by providing a row and column index ```char c = letters[0][1];```

* We can also think of them as the index of the outer array and the index of the subarray
* We can modify elements the same way ```letters[1][2] = 'z';```

We traverse 2D arrays using nested loops.

* We can use loops of any type, but we typically use nested for loops to keep track of the indices
* Row-major order traverses through each row moving horizontally to the right through each row
* Column-major order traverses through each column moving vertically down through each column
* Row-major order and column-major order start and end on the same elements, but the paths are different.
* In order to convert row-major to column-major, we need to make the outer loop terminating condition depend on the number of columns, make the inner loop terminating condition depend on the number of rows, and flip the variables in our accessor within the inner loop to ensure that we don’t try to access outside of the 2D array since we flipped the direction of traversal.

Here are examples of row-major and column-major order:

```java
// Row-major order
for(int o = 0; o < letters.length; o++) {
    for(int i = 0; i < letters[o].length; i++) {
        char c = letters[o][i];
    }
}

// Column-major order
for(int o = 0; o < letters[0].length; o++) {
    for(int i = 0; i < letters.length; i++) {
        char c = letters[i][o];
    }
}
```

Conditional logic in our 2D array traversal allows us to use the data in a meaningful way. We can control which rows and columns we look at, ensure that the data we are looking at is what we want, perform calculations on specific elements, avoid throwing exceptions, and more.

Here is an example of traversal with conditional logic.

Given this 2D array of Strings:

```java
String[][] words = {{"championship", "QUANTITY", "month"},{"EMPLOYEE", "queen", "understanding"},{"method", "writer", "MOVIE"}};
```

We are going to flip the capitalization of the words:
```java
System.out.println("Before...");
System.out.println(Arrays.deepToString(words).replace("],", "],\n") + "\n");

for(int i=0; i<words.length; i++) {
    for(int j = 0; j<words[i].length; j++) {
        if(words[i][j]!=null) {

            // Check the capitalization
            boolean allCaps = true;
            for(char c : words[i][j].toCharArray()) 
                if(!Character.isUpperCase(c)) 
                    allCaps = false;
                
            // Flip the capitalization
            if(allCaps)
                words[i][j] = words[i][j].toLowerCase();
            else
                words[i][j] = words[i][j].toUpperCase();
        }
    }
}

System.out.println("After...");
System.out.println(Arrays.deepToString(words).replace("],", "],\n") + "\n");
```

Here is the output of the above code:
```git
Before...
[[championship, QUANTITY, month],
 [EMPLOYEE, queen, understanding],
 [method, writer, MOVIE]]

After...
[[CHAMPIONSHIP, quantity, MONTH],
 [employee, QUEEN, UNDERSTANDING],
 [METHOD, WRITER, movie]]
```

Time to work some review problems!

After learning about 2D arrays, you have decided to become a CS professor and you are now teaching your class about 2D arrays. You are making an application which will keep track of their exam grades and show you statistics about their performance. You will be using 2D arrays to keep track of their exam grades

**Main.java**
```java
import java.util.Arrays;
public class Main {
	public static void main(String[] args) {  

		//Declare and initialize a 4x3 2D array of doubles called `scores` below


        System.out.println(Arrays.deepToString(scores));

            //Manually enter the scores for the second exam below


        System.out.println(Arrays.deepToString(scores));
            
        //Declare and initialize an empty 4x2 2D array of double values called `newScores` below


        //Use `for` loops to copy the scores below
        

        System.out.println(Arrays.deepToString(newScores));

        //Iterate through the `newScores` 2D array and use `if` statement to add 2 additional points below
        
        System.out.println(Arrays.deepToString(newScores));
	}
}
```

**EXERCISE:**
1. Let’s declare and initialize a 4x3 2D array of doubles called ```scores``` which will contain the exam data for four students.

    The rows in ```scores``` represent the student and the columns represent the exam number.

    Use initializer lists to store these first exam scores in the 0th column of ```scores```:

    (80.4, 96.2, 100.0, 78.9)

    Store the value ```–1``` for the rest of the exams.

    Use the provided print statement to print the result in the console.

    **SOLUTION**

    ```java
    import java.util.Arrays;
    public class Main {
        public static void main(String[] args) {  

            //Declare and initialize a 4x3 2D array of doubles called `scores` below
            double[][] scores = {{80.4, -1, -1}, {96.2, -1, -1}, {100.0, -1, -1}, {78.9, -1, -1}};

            System.out.println(Arrays.deepToString(scores));

                //Manually enter the scores for the second exam below


            System.out.println(Arrays.deepToString(scores));
                
            //Declare and initialize an empty 4x2 2D array of double values called `newScores` below


            //Use `for` loops to copy the scores below
            

            // System.out.println(Arrays.deepToString(newScores));

            //Iterate through the `newScores` 2D array and use `if` statement to add 2 additional points below
            
            // System.out.println(Arrays.deepToString(newScores));
        }
    }
    ```

2. Now that we have the scores for the next exams, enter these scores for the second exam (column 1) one by one using 4 lines.

    * 89.7
    * 90.5
    * 93.6
    * 88.1

    Use the provided print statement to print the updated 2D array.

    ```java
    import java.util.Arrays;
    public class Main {
        public static void main(String[] args) {  

            //Declare and initialize a 4x3 2D array of doubles called `scores` below
            double[][] scores = {{80.4, -1, -1}, {96.2, -1, -1}, {100.0, -1, -1}, {78.9, -1, -1}};

            System.out.println(Arrays.deepToString(scores));

            //Manually enter the scores for the second exam below
            scores[0][1] = 89.7;
            scores[1][1] = 90.5;
            scores[2][1] = 93.6;
            scores[3][1] = 88.1;

            System.out.println(Arrays.deepToString(scores));
                
            //Declare and initialize an empty 4x2 2D array of double values called `newScores` below


            //Use `for` loops to copy the scores below
            

            // System.out.println(Arrays.deepToString(newScores));

            //Iterate through the `newScores` 2D array and use `if` statement to add 2 additional points below
            
            // System.out.println(Arrays.deepToString(newScores));
        }
    }
    ```

3. We just remembered that we need to keep track of only 2 exams.

    Declare and initialize an empty 4x2 2D array of double values called ```newScores```.

    ```java
    import java.util.Arrays;
    public class Main {
        public static void main(String[] args) {  

            //Declare and initialize a 4x3 2D array of doubles called `scores` below
            double[][] scores = {{80.4, -1, -1}, {96.2, -1, -1}, {100.0, -1, -1}, {78.9, -1, -1}};

            System.out.println(Arrays.deepToString(scores));

            //Manually enter the scores for the second exam below
            scores[0][1] = 89.7;
            scores[1][1] = 90.5;
            scores[2][1] = 93.6;
            scores[3][1] = 88.1;

            System.out.println(Arrays.deepToString(scores));
                
            //Declare and initialize an empty 4x2 2D array of double values called `newScores` below
            double[][] newScores = new double[4][2];

            //Use `for` loops to copy the scores below
            

            // System.out.println(Arrays.deepToString(newScores));

            //Iterate through the `newScores` 2D array and use `if` statement to add 2 additional points below
            
            // System.out.println(Arrays.deepToString(newScores));
        }
    }
    ```

4. Use ```for``` loops to copy the scores of exam 1 and exam 2 from ```scores``` to ```newScores``` 2D array. (Do not include the -1 values).

    *Note: For internal testing purposes, please use i and j as the counters for the outer and inner loops respectively.*

    ```java
    import java.util.Arrays;
    public class Main {
        public static void main(String[] args) {  

            //Declare and initialize a 4x3 2D array of doubles called `scores` below
            double[][] scores = {{80.4, -1, -1}, {96.2, -1, -1}, {100.0, -1, -1}, {78.9, -1, -1}};

            System.out.println(Arrays.deepToString(scores));

            //Manually enter the scores for the second exam below
            scores[0][1] = 89.7;
            scores[1][1] = 90.5;
            scores[2][1] = 93.6;
            scores[3][1] = 88.1;

            System.out.println(Arrays.deepToString(scores));
                
            //Declare and initialize an empty 4x2 2D array of double values called `newScores` below
            double[][] newScores = new double[4][2];

            //Use `for` loops to copy the scores below
            for( int i = 0; i < newScores.length; i++ ) {
                for( int j = 0; j < newScores[i].length; j++ ) {
                    newScores[i][j] = scores[i][j];
                }
            }

            System.out.println(Arrays.deepToString(newScores));

            //Iterate through the `newScores` 2D array and use `if` statement to add 2 additional points below
            
            System.out.println(Arrays.deepToString(newScores));
        }
    }
    ```

5. We allowed the students to complete an extra credit activity to contribute towards their scores.

    Iterate through the ```newScores``` 2D array and use an if statement to add 2 additional points to the grade if the exam grade is less than 90.

    ```java
    import java.util.Arrays;
    public class Main {
        public static void main(String[] args) {  

            //Declare and initialize a 4x3 2D array of doubles called `scores` below
            double[][] scores = {{80.4, -1, -1}, {96.2, -1, -1}, {100.0, -1, -1}, {78.9, -1, -1}};

            System.out.println(Arrays.deepToString(scores));

            //Manually enter the scores for the second exam below
            scores[0][1] = 89.7;
            scores[1][1] = 90.5;
            scores[2][1] = 93.6;
            scores[3][1] = 88.1;

            System.out.println(Arrays.deepToString(scores));
                
            //Declare and initialize an empty 4x2 2D array of double values called `newScores` below
            double[][] newScores = new double[4][2];

            //Use `for` loops to copy the scores below
            for( int i = 0; i < newScores.length; i++ ) {
                for( int j = 0; j < newScores[i].length; j++ ) {
                    newScores[i][j] = scores[i][j];
                }
            }

            System.out.println(Arrays.deepToString(newScores));

            //Iterate through the `newScores` 2D array and use `if` statement to add 2 additional points below
            for( int i = 0; i < newScores.length; i++ ) {
                for( int j = 0; j < newScores[i].length; j++ ) {
                    if( newScores[i][j] < 90 ) {
                        newScores[i][j] += 2;
                    }
                }
            }
            
            System.out.println(Arrays.deepToString(newScores));
        }
    }
    ```

    OUTPUT:
    ```git
    [[80.4, -1.0, -1.0], [96.2, -1.0, -1.0], [100.0, -1.0, -1.0], [78.9, -1.0, -1.0]]
    [[80.4, 89.7, -1.0], [96.2, 90.5, -1.0], [100.0, 93.6, -1.0], [78.9, 88.1, -1.0]]
    [[80.4, 89.7], [96.2, 90.5], [100.0, 93.6], [78.9, 88.1]]
    [[82.4, 91.7], [96.2, 90.5], [100.0, 93.6], [80.9, 90.1]]
    ```