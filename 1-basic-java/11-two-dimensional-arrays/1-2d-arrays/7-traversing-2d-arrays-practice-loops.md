## Traversing 2D Arrays: Practice with Loops

We have seen how to traverse 2D arrays using standard **for** loops, but in this exercise, we will practice traversing them using some other loop types. For example, you may want to only retrieve elements without keeping track of the indices using enhanced for loops, or you could continuously update the 2D array until a condition is met using while loops.

In enhanced for loops, each element is iterated through until the end of the array. When we think about the structure of 2D arrays in Java (arrays of array objects) then we know that the outer enhanced for loop elements are going to be arrays.

Let’s take a look at an example:

Given this 2D array of character data: 
```java
char[][] charData = {{'a', 'b', 'c', 'd', 'e', 'f'},{'g', 'h', 'i', 'j', 'k', 'l'}};
```

Print out every character using enhanced for loops:
```java
for(char[] charRow : charData) {
    for(char c : charRow) {
        System.out.print(c + " ");
    }
    System.out.println();
}
```

Remember that the syntax for enhanced for loops looks like so: ```for( datatype elementName : arrayName){```. Since 2D arrays in Java are arrays of arrays, each element in the outer enhanced for loop is an entire row of the 2D array. The nested enhanced for loop is then used to iterate through each element in the extracted row. Here is the output of the above code:
```git
a b c d e f 
g h i j k l
```

Here is an example which accomplishes the same thing, but using while loops:
```java
int i = 0, j=0;
while(i<charData.length) {
    j = 0;
    while(j<charData[i].length) {
        System.out.print(charData[i][j] + " ");
        j++;
    }
    System.out.println();
    i++;
}
```

Here is the output of the above code:
```git
a b c d e f 
g h i j k l
```

Notice how we can use different loop types for traversal, but still receive the same result.

Let’s work some example problems using different loop types!

**Main.java**
```java
public class Main {
	public static void main(String[] args) {
	    int[][] binary = {
            {0, 1, 0, 1},
            {1, 1, 1, 0},
            {1, 0, 0, 1},
            {1, 0, 1, 0}
        };
		int onesCount = 0;
		System.out.println(onesCount);

        String[][] wordData = {{"study", "consider", "examine", "learn"}, {"ponder", "read", "think", "cogitate"}};	
        
        int i = 0;
        int j = 0;

		//System.out.println(wordData[i][j] + ": [" + i + "]" + "[" + j + "]");

	}
}
```

EXERCISE:
1. We’ve provided a 2D array called ```binary``` and a counter called ```onesCount```.

    Calculate the total number of ```1```s in the 2D array ```binary``` using nested enhanced ```for``` loops and print it to the console.

    *Note: you must use nested for-loops for this task.* 

    **SOLUTION:**

    ```java
    public class Main {
        public static void main(String[] args) {

            int[][] binary = {
                {0, 1, 0, 1},
                {1, 1, 1, 0},
                {1, 0, 0, 1},
                {1, 0, 1, 0}
            };

            int onesCount = 0;

            for( int[] binaryRow : binary ) {
                for( int row : binaryRow ) {
                    onesCount += row;
                } 
            }

            System.out.println(onesCount);

            String[][] wordData = {{"study", "consider", "examine", "learn"}, {"ponder", "read", "think", "cogitate"}};	
            
            int i = 0;
            int j = 0;

            //System.out.println(wordData[i][j] + ": [" + i + "]" + "[" + j + "]");

        }
    }
    ```

2. We have provided the iterators i and j and a matrix of strings called ```wordData```.

    Use nested while loops and iterate through all the elements of ```wordData``` and print them to the console in this format:

    ```git
    word [row][column] 
    ```

    The print statement is given, you need to use it in the body of the inner while loop.

    **SOLUTION:**

    ```java
    public class Main {
        public static void main(String[] args) {

            int[][] binary = {
                {0, 1, 0, 1},
                {1, 1, 1, 0},
                {1, 0, 0, 1},
                {1, 0, 1, 0}
            };

            int onesCount = 0;

            for( int[] binaryRow : binary ) {
                for( int row : binaryRow ) {
                    onesCount += row;
                } 
            }

            System.out.println(onesCount);

            String[][] wordData = {{"study", "consider", "examine", "learn"}, {"ponder", "read", "think", "cogitate"}};	
            
            int i = 0;
            int j = 0;

            while( i < wordData.length ) {
                j = 0;
                while( j < wordData[i].length ) {
                    System.out.println(wordData[i][j] + ": [" + i + "]" + "[" + j + "]");
                    j++;
                }
                System.out.println(); 
                i++;
            }

        }
    }
    ```