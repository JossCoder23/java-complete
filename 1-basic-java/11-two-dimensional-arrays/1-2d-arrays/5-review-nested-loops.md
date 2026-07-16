## Review of Nested Loops

We’re about to look at how we can use loops to make our lives easier when working with 2D arrays. But before we do that, let’s take a moment to refresh ourselves on how nested loops work.

Nested loops consist of two or more loops placed within each other. We will be looking at one loop nested within another for 2D traversal.

The way it works is that, for every iteration of the outer loop, the inner loop finishes all of its iterations.

Here is an example using for loops:

```java
for(int outer = 0; outer < 3; outer++){
    System.out.println("The outer index is: " + outer);
    for(int inner = 0; inner < 4; inner++){
        System.out.println("\tThe inner index is: " + inner);
    }
}
```

The output of the above nested loops looks like so:
```git
The outer index is: 0
    The inner index is: 0
    The inner index is: 1
    The inner index is: 2
    The inner index is: 3
The outer index is: 1
    The inner index is: 0
    The inner index is: 1
    The inner index is: 2
    The inner index is: 3
The outer index is: 2
    The inner index is: 0
    The inner index is: 1
    The inner index is: 2
    The inner index is: 3
```

From this example we can see how every time the outer loop iterates one time, the inner loop iterates fully.

This is an important concept for 2D array traversal, because for every row in a two dimensional matrix, we want to iterate through every column. We will look more at this in the next exercise.

Nested loops can consist of any type of loop and with any combination of loops. Let’s take a look at a few more interesting examples.

Here is an example of nested while loops:

```java
int outerCounter = 0;
int innerCounter = 0; 
while(outerCounter<5){
    outerCounter++;
    innerCounter = 0;
    while(innerCounter<7){
        innerCounter++;
    }
}
```

We can even have some interesting combinations. Here is an enhanced for loop inside of a while loop:
```java
int outerCounter = 0;
int[] innerArray = {1,2,3,4,5};

while(outerCounter<7){
    System.out.println();
    for(int number : innerArray){
        System.out.print(number * outerCounter + " ");
    }
    outerCounter++;
}
```

The output of the above example creates a multiplication table:

```git
0 0 0 0 0 
1 2 3 4 5 
2 4 6 8 10 
3 6 9 12 15 
4 8 12 16 20 
5 10 15 20 25 
6 12 18 24 30 
```

This is an interesting example, because for every iteration of the while loop, we iterate through every element of an array using an enhanced for loop. This is similar to the iteration pattern we use for 2D array traversal. We will be going over that in the next exercise.

Let’s practice using nested loops!

You are in charge of controlling the amount of people who reserve seats for the world famous programming contest. You have two long arrays of integers which represent the contestant’s IDs for two days of the competition. The index of the array represents their seat number. You need to use nested for loops to find if a contestant tried to register for both days. Print out the ID of the contestants who tried to register twice as well as their seat numbers for both days.

**Main.java**

```java
public class Main {
	public static void main(String[] args) {
		int tableSize = 10;
        for(int i = 0; i < 10; i++){
            for(int j = 10; j > 1; j--){
                System.out.print(i * j);
                System.out.print(" ");
            }
            System.out.println();
        }
	}
}
```

EXERCISE:
1. We provided a nested for loop to print out a 10x10 multiplication table. However, the outer ```for``` loop contains an error (if you run the code, you will not see a 10x10 table). Fix this error.

    **SOLUTION:**

    ```java
    public class Main {
	    public static void main(String[] args) {
            int tableSize = 10;
            for(int i = 1; i <= 10; i++){
                for(int j = 1; j <= 10; j++){
                    System.out.print(i * j);
                    System.out.print(" ");
                }
                System.out.println();
            }
        }
    }
    ```

2. The inner for-loop has two errors. Find and fix them.

    **SOLUTION:**

    ```java
    public class Main {
	    public static void main(String[] args) {
            int tableSize = 10;
            for(int i = 1; i <= 10; i++){
                for(int j = 1; j <= 10; j++){
                    System.out.print(i * j);
                    System.out.print(" ");
                }
                System.out.println();
            }
        }
    }
    ```