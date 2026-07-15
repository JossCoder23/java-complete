## Logic Errors
Once we have removed the syntax errors and run-time errors, the program runs successfully. But sometimes, the program still doesn’t do what we want it to do or no output is produced. Hmmm…

These types of errors, which provide incorrect output, but appear to be error-free, are called logic errors. Logic errors occur when there is a design flaw in your program. These are some of the most common errors that happen to beginners and also usually the most difficult to find and eliminate.

Because logical errors solely depend on the logical thinking of the programmer, your job now is to figure out why the program didn’t do what you wanted it to do.

Some common logic errors:

* Program logic is flawed
* Some “silly” mistake in an ```if``` statement or a ```for/while``` loop

Note: Logic errors don’t have error messages. Sometimes, programmers use a process called test-driven development (TDD), a way to give logic errors error messages and save yourself a lot of headaches! 

EXERCISE:

1. In the code editor, we have provided a program that should print the steps from 1 to 10.

    Run the ```Main.java``` file and see if that’s happening.

    ```java
    public class Main{
        public static void main(String[] args) {
            int steps = 10;
            
            for (int i = 0; i <= steps; i++) {
                System.out.println("Step #" + i);
            }
        }
    }
    ```

2. The program prints the steps from 0 to 10 instead of 1 to 10.

    There’s a logical error in this code.

    Fix it and run the code.

    ```java
    public class Main{
        public static void main(String[] args) {
            int steps = 10;
            
            for (int i = 1; i <= steps; i++) {
                System.out.println("Step #" + i);
            }
        }
    }
    ```