## Quiz

1. Which of the following is true about Row-major order?
    * Row-major order starts at the top right of the 2D array (when viewing it as a matrix) and traverses across each row until it ends at the bottom left corner.
    * Row-major order starts at the bottom left of the 2D array (when viewing it as a matrix) and traverses up each column until it ends at the top right corner.
    * ```Row-major order starts at the top left of the 2D array (when viewing it as a matrix) and traverses across each row until it ends at the bottom right corner.```
    * Row-major order starts at the top left of the 2D array (when viewing it as a matrix) and traverses down each column until it ends at the bottom right corner.

2. Using initializer lists, we need the first 2D array to have a top row of ```{1,2,3}``` and a bottom row of ```{4,5,6}```. The second 2D array needs to have a top row of ```{7,8,9}``` and a bottom row of ```{10,11,12}```. Fill in the blanks with the correct code.

    ```java
    public class Exercise1Solution {
        public static void main(String[] args) {
            
            int[][] first = ________
            
            int[][] second;
            second = ________
        }
    }
    ```
    * {7,8,9,10,11,12};
    * {{7,8,9},{10,11,12}};
    * ```{{1,2,3},{4,5,6}};```
    * {1,2,3,4,5,6};
    * ```new int[][] {{7,8,9},{10,11,12}};```

3. Which answer describes how you should set up enhanced ```for``` loops to iterate through the provided 2D array of ```Strings```?

    ```java
    public class EnhancedForLoops {
        public static void main(String[] args) {
            String[][] strTwoD = {
                {"learn", "study", "remember"},
                {"read", "memorize", "grasp"},
                {"master", "know", "retain"}
            };
        }
    }
    ```
    * The outer enhanced for loop iterates through each String value, and the inner enhanced for loop iterates through each String value.
    * The outer enhanced for loop iterates through each String value, while the inner enhanced for loop iterates through each array of Strings.
    * The outer enhanced for loop iterates through each array of Strings, and the inner enhanced for loop iterates through each array of Strings.
    * ```The outer enhanced for loop iterates through each array of Strings, while the inner enhanced for loop iterates through each String value in the subarray.```

4. Fill in the correct code to store the char 'i' from the 2D array twoDChar.

    ```java
    public class GetChar {
        public static void main(String[] args) {
            
            char[][] twoDChar = {
                {'h', 'z', 'u', 'j'},
                {'o', 'x', 'm', 'p'},
                {'q', 'i', 'n', 'g'}
            };
            
            //Store 'i' from twoDChar
            char result = twoDChar[2][1];
        }
    }
    ```
    * ```twoDChar[2][1];```

5. Which of the following is true about modifying elements in a 2D array?

    * When modifying an element in a 2D array, you access the element using the row index in brackets first, the variable name second, and the column index in brackets third. You then set it equal to a value.
    * When modifying an element in a 2D array, you access the element using the row index in brackets first, column index in brackets second, and the variable name third. You then set it equal to a value.
    * When modifying an element in a 2D array, you access the element using the variable name first, the column index in brackets second, and the row index in brackets third. You then set it equal to a value.
    * ```When modifying an element in a 2D array, you access the element using the variable name first, the row index in brackets second, and the column index in brackets third. You then set it equal to a value.```

6. Choose the correct code for declaring a 2D int array in this Java application.

    ```java
    public class MyTwoDArray {
        public static void main(String[] args) {
            //Declare a 2D int array
            _____________
        }
    }
    ```
    * ```int[][] myTwoD;```
    * int myTwoD;
    * [int] myTwoD;
    * int[] myTwoD;
    * int myTwoD[];

7. Which of the following is true about nested loop iteration?

    * The outer-most loop and and inner-most loop will always iterate at the same rate.
    * The inner-most nested loop must complete all of its iterations before the outer loop begins.
    * The outer-most loop must complete all of its iterations before the inner loop iterates.
    * ```The inner-most nested loop must complete all of its iterations before the outer loop continues.```

8. Fill in the code for nested loops which traverse the 2D array using column-major order.

    ```java
    public class ColumnMajor {
        public static void main(String[] args) {
            
            double[][] data = {
                {1.4, 7.5, 3.5, 8.7, 9.2},
                {0.8, 2.6, 6.3, 3.4, 7.5}
            };
            
            for(int i = 0; i < ________; i++) {
                for( int j = 0; j < ________; j++) {
                    System.out.println(data[j][i]);
                }
            }
        }
    }
    ```
    * data[j].length
    * data.size
    * data[i].length
    * ```data.length```
    * data
    * ```data[0].length```