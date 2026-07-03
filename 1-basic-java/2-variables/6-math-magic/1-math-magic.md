## Math Magic

In this project, you will become a mathemagician and write a small program that performs a mathematical magic trick! It will involve performing arithmetic operations on an integer that you choose.

The instructions provided are general guidelines. Upon completion of the project, feel free to explore the code on your own.

If you get stuck during this project or would like to see an experienced developer work through it, click “Get Unstuck“ to see a project walkthrough video.

```java
public class Magic {
	public static void main(String[] args) {

		
	}
}
```

1. Create an  ```int``` variable called  ```myNumber```.

    Set it equal to any integer other than 0.
    
    SOLUTION:
    
    ```java
    public class Magic {
        public static void main(String[] args) {
            int myNumber = 0;
            

        }
    }
    ```

2. We will refer to ```myNumber``` as the original number from now on - it might be helpful to document this.

    Write a comment in the program that documents this.

    SOLUTION:
    ```java
    public class Magic {
        public static void main(String[] args) {
            // This is mi program call it Math Magic
            int myNumber = 0;
            
        }
    }
    ```

3. Create an ```int``` variable called ```stepOne```.

    Set it equal to the original number (```myNumber```) multiplied by itself.

    SOLUTION:
    ```java
    public class Magic {
        public static void main(String[] args) {
            // This is mi program call it Math Magic
            int myNumber = 0;
            int stepOne = myNumber * myNumber;

        }
    }
    ```

4. Create an ```int``` variable called ```stepTwo```.

    Set it equal to the previous result (```stepOne```) plus the original number (```myNumber```).

    SOLUTION:
    ```java
    public class Magic {
        public static void main(String[] args) {
            // This is mi program call it Math Magic
            int myNumber = 0;
            int stepOne = myNumber * myNumber;
            int stepTwo = stepOne + myNumber;
            
        }
    }
    ```

5. Create an ```int``` variable called ```stepThree```.

    Set it equal to the previous result (```stepTwo```) divided by the original number.

    SOLUTION:
    ```java
    public class Magic {
        public static void main(String[] args) {
            // This is mi program call it Math Magic
            int myNumber = 0;
            int stepOne = myNumber * myNumber;
            int stepTwo = stepOne + myNumber;
            int stepThree = stepTwo / myNumber;
        }
    }
    ```

6. Create an ```int``` variable called ```stepFour```.

    Set it equal to the previous result (```stepThree```) plus ```17```.

    SOLUTION:
    ```java
    public class Magic {
        public static void main(String[] args) {
            // This is mi program call it Math Magic
            int myNumber = 0;
            int stepOne = myNumber * myNumber;
            int stepTwo = stepOne + myNumber;
            int stepThree = stepTwo / myNumber;
            int stepFour = stepThree + 17;
        }
    }
    ```

7. Create an ```int``` variable called ```stepFive```.
    
    Set it equal to the previous result (```stepFour```) minus the original number.

    SOLUTION:
    ```java
    public class Magic {
        public static void main(String[] args) {
            // This is mi program call it Math Magic
            int myNumber = 0;
            int stepOne = myNumber * myNumber;
            int stepTwo = stepOne + myNumber;
            int stepThree = stepTwo / myNumber;
            int stepFour = stepThree + 17;
            int stepFive = stepFour - myNumber;
        }
    }
    ```

8. Create an ```int``` variable called ```stepSix```.

    Set it equal to the previous result (```stepFive```) divided by 6.

    SOLUTION:
    ```java
    public class Magic {
        public static void main(String[] args) {
            // This is mi program call it Math Magic
            int myNumber = 0;
            int stepOne = myNumber * myNumber;
            int stepTwo = stepOne + myNumber;
            int stepThree = stepTwo / myNumber;
            int stepFour = stepThree + 17;
            int stepFive = stepFour - myNumber;
            int stepSix = stepFive / 6;
        }
    }
    ```

9. Print out the value of the last step.

    Then, save and run your code!

    What number is printed to the console?

    SOLUTION: console error
    ```java
    public class Magic {
        public static void main(String[] args) {
            // This is mi program call it Math Magic
            int myNumber = 0;
            int stepOne = myNumber * myNumber;
            int stepTwo = stepOne + myNumber;
            int stepThree = stepTwo / myNumber;
            int stepFour = stepThree + 17;
            int stepFive = stepFour - myNumber;
            int stepSix = stepFive / 6;
            System.out.println(stepSix);
        }
    }
    ```

    OUTPUT:
    ```git
    Exception in thread "main" java.lang.ArithmeticException: / by zero
	at Magic.main(Magic.java:7)
    ```

10. Now, go back to your code and change ```myNumber``` to any other integer. Run your program again.

    Is the output the same?

    It’s math magic!

    Note: Due to the range of the ```int``` primitive data type, only set ```myNumber``` to integer values between -46,341 and 46,340 (both inclusive). Values outside of this range for ```myNumber``` will cause the value of ```stepOne``` to exceed the maximum possible value of ```int``` when we multiply ```myNumber``` by itself, which can cause the program to produce unexpected results!
    
    SOLUTION:
    ```java
    public class Magic {
        public static void main(String[] args) {
            // This is mi program call it Math Magic
            int myNumber = 3;
            int stepOne = myNumber * myNumber;
            int stepTwo = stepOne + myNumber;
            int stepThree = stepTwo / myNumber;
            int stepFour = stepThree + 17;
            int stepFive = stepFour - myNumber;
            int stepSix = stepFive / 6;
            System.out.println(stepSix);
        }
    }
    ```

    OUTPUT:
    ```git
    3
    ```

11. Great job completing this project! Want to keep challenging yourself?

    Recreate this project using only two variables: ```myNumber``` and ```magicNumber```. Use your understanding of compound assignment operators to recreate the above program by only manipulating ```magicNumber```.

    See the Hint for more help.

    SOLUTION:
    ```java
    public class Magic {
        public static void main(String[] args) {
            // This is mi program call it Math Magic
            int myNumber = 323;
            int magicNumber = myNumber * myNumber;
            magicNumber += myNumber;
            magicNumber /= myNumber;
            magicNumber += 17;
            magicNumber -= myNumber;
            magicNumber /= 6;
            System.out.println(magicNumber);
        }
    }
    ```

    OUTPUT:
    ```git
    3
    ```