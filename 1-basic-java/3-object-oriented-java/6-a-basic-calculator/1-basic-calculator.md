## A Basic Calculator
In this project, you will use classes, methods, and objects to create a simple arithmetic calculator. The calculator will be able to:

* Add two integers
* Subtract two integers
* Multiply two integers
* Divide two integers
* Apply the modulo operator on two integers

The instructions provided are general guidelines. Upon completion of the project, feel free to explore more in the learning environment.

Important: Moving forward, all projects will require that you define the main method manually. When you click the “Save” button below, an attempt to run your Java code is made. However, Java will return an error if you attempt to run a Java program without first defining a main method. If you encounter such an error, do not worry, you can define the main method ahead of time in order to avoid seeing the error.

================================================================

SOLUTION:
1. Create a ```public``` class called ```Calculator```.

    SOLUTION

    **Calculator.java**
    ```java
    public class Calculator {
    
    }
    ```

2. Inside of the class, create a ```Calculator()``` constructor. You can leave the contents of the constructor empty.

    SOLUTION

    **Calculator.java**
    ```java
    public class Calculator {
    
        public Calculator() {}

    }
    ```

3. Next, create a ```public``` method that returns an ```int``` and call it ```add()```.

    SOLUTION

    **Calculator.java**
    ```java
    public class Calculator {
    
        public Calculator() {}

        public int add() {}

    }
    ```

4. The ```add()``` method should accept two ```int``` parameters. For example: ```int a, int b```.

    SOLUTION

    **Calculator.java**
    ```java
    public class Calculator {
    
        public Calculator() {}

        public int add(int a, int b) {}

    }
    ```

5. The ```add``` method should add the two integer parameters that a user will specify. Inside of the ```add``` method, return the sum of ```a``` and ```b```.

    SOLUTION

    **Calculator.java**
    ```java
    public class Calculator {
    
        public Calculator() {}

        public int add(int a, int b) {
            return a + b;
        }

    }
    ```

6. Next, create another similar method called ```subtract()```. The ```subtract()``` method should accept two ```int``` parameters, just like the ```add()``` method does.
    
    SOLUTION

    **Calculator.java**
    ```java
    public class Calculator {
    
        public Calculator() {}

        public int add(int a, int b) {
            return a + b;
        }

        public int substract(int a, int b) {
  
        }

    }
    ```

7. Inside of the ```subtract()``` method, ```return``` the difference of ```a``` and ```b```.
    
    SOLUTION

    **Calculator.java**
    ```java
    public class Calculator {
    
        public Calculator() {}

        public int add(int a, int b) {
            return a + b;
        }

        public int substract(int a, int b) {
            return a - b;
        }

    }
    ```

8. Create another method called ```multiply()```. The ```multiply()``` method should accept two ```int``` parameters.
    
    SOLUTION

    **Calculator.java**
    ```java
    public class Calculator {
    
        public Calculator() {}

        public int add(int a, int b) {
            return a + b;
        }

        public int substract(int a, int b) {
            return a - b;
        }

        public int multiply(int a, int b){ 

        }

    }
    ```

9. Inside of the ```multiply``` method, ```return``` the product of ```a``` and ```b```.
    
    SOLUTION

    **Calculator.java**
    ```java
    public class Calculator {
    
        public Calculator() {}

        public int add(int a, int b) {
            return a + b;
        }

        public int substract(int a, int b) {
            return a - b;
        }

        public int multiply(int a, int b){ 
            return a * b;
        }

    }
    ```

10. Create another method called ```divide()```. It should accept two ```int``` parameters.
    
    SOLUTION

    **Calculator.java**
    ```java
    public class Calculator {
    
        public Calculator() {}

        public int add(int a, int b) {
            return a + b;
        }

        public int substract(int a, int b) {
            return a - b;
        }

        public int multiply(int a, int b){ 
            return a * b;
        }

        public double divide(int a, int b){

        }

    }
    ```

11. Inside of the ```divide()``` function, return ```a``` divided by ```b```.

    SOLUTION

    **Calculator.java**
    ```java
    public class Calculator {
    
        public Calculator() {}

        public int add(int a, int b) {
            return a + b;
        }

        public int substract(int a, int b) {
            return a - b;
        }

        public int multiply(int a, int b){ 
            return a * b;
        }

        public double divide(int a, int b){
            return a / b;
        }

    }
    ```

12. Create another method called ```modulo```. It should accept two ```int``` parameters.

    SOLUTION

    **Calculator.java**
    ```java
    public class Calculator {
    
        public Calculator() {}

        public int add(int a, int b) {
            return a + b;
        }

        public int substract(int a, int b) {
            return a - b;
        }

        public int multiply(int a, int b){ 
            return a * b;
        }

        public double divide(int a, int b){
            return a / b;
        }

        public int modulo(int a, int b){ 

        }

    }
    ```

13. Inside of the ```modulo()``` function, return ```a``` modulo ```b```.

    SOLUTION

    **Calculator.java**
    ```java
    public class Calculator {
    
        public Calculator() {}

        public int add(int a, int b) {
            return a + b;
        }

        public int substract(int a, int b) {
            return a - b;
        }

        public int multiply(int a, int b){ 
            return a * b;
        }

        public double divide(int a, int b){
            return a / b;
        }

        public int modulo(int a, int b){ 
            return a % b;
        }

    }

14. Next, create a ```main()``` method. Can you remember all the keywords necessary for a ```main()``` method?

    SOLUTION

    **Calculator.java**
    ```java
    public class Calculator {
    
        public Calculator() {}

        public int add(int a, int b) {
            return a + b;
        }

        public int substract(int a, int b) {
            return a - b;
        }

        public int multiply(int a, int b){ 
            return a * b;
        }

        public double divide(int a, int b){
            return a / b;
        }

        public int modulo(int a, int b){ 
            return a % b;
        }

        public static void main(String[] args){
    
        }

    }

15. Inside of ```main()```, create a ```Calculator``` object called ```myCalculator```.

    SOLUTION

    **Calculator.java**
    ```java
    public class Calculator {
    
        public Calculator() {}

        public int add(int a, int b) {
            return a + b;
        }

        public int substract(int a, int b) {
            return a - b;
        }

        public int multiply(int a, int b){ 
            return a * b;
        }

        public double divide(int a, int b){
            return a / b;
        }

        public int modulo(int a, int b){ 
            return a % b;
        }

        public static void main(String[] args){
            Calculator myCalculator = new Calculator();
        }

    }

16. Print out the value of calling the ```add()``` method on ```myCalculator```. Pass in ```5``` and ```7``` as parameters.

    SOLUTION

    **Calculator.java**
    ```java
    public class Calculator {
    
        public Calculator() {}

        public int add(int a, int b) {
            return a + b;
        }

        public int substract(int a, int b) {
            return a - b;
        }

        public int multiply(int a, int b){ 
            return a * b;
        }

        public double divide(int a, int b){
            return a / b;
        }

        public int modulo(int a, int b){ 
            return a % b;
        }

        public static void main(String[] args){
            Calculator myCalculator = new Calculator();
            System.out.println(myCalculator.add(5, 7));
        }

    }

17. On the next line, print out the value of calling the ```subtract()``` method on ```myCalculator```. Pass in ```45``` and ```11``` as parameters.
    
    SOLUTION

    **Calculator.java**
    ```java
    public class Calculator {
    
        public Calculator() {}

        public int add(int a, int b) {
            return a + b;
        }

        public int substract(int a, int b) {
            return a - b;
        }

        public int multiply(int a, int b){ 
            return a * b;
        }

        public double divide(int a, int b){
            return a / b;
        }

        public int modulo(int a, int b){ 
            return a % b;
        }

        public static void main(String[] args){
            Calculator myCalculator = new Calculator();
            System.out.println(myCalculator.add(5, 7));
            System.out.println(myCalculator.substract(45, 11));
        }

    }

18. If you completed this project correctly, the output should be ```12``` and ```34```. Feel free to explore more with the program. What are some ways in which the program could be improved?

    SOLUTION

    OUTPUT
    ```git
    12
    34
    ```

19. Add comments near the top of the program that describe what the program does.

    ```java
    public class Calculator {

        /*
        author: Jose Pardo
        project: Basic Calculator
        */
        
        public Calculator() {}

        public int add(int a, int b) {
            return a + b;
        }

        public int substract(int a, int b) {
            return a - b;
        }

        public int multiply(int a, int b){ 
            return a * b;
        }

        public double divide(int a, int b){
            return a / b;
        }

        public int modulo(int a, int b){ 
            return a % b;
        }

        public static void main(String[] args){
            Calculator myCalculator = new Calculator();
            System.out.println(myCalculator.add(5, 7));
            System.out.println(myCalculator.substract(45, 11));
        }

    }
    ```