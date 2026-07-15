## Quiz

1. **Find the bug**: What’s the error in the code example?

    ```java
    public class Debug {

        public static void main(String[] args) {
            
            System.out.println("hello")
            System.out.println("hi");
            
            System.out.println("good morning");
            System.out.println("guten tag");
            
        }
    
    }
    ```
    * The class has the wrong name.
    * main() is defined incorrectly.
    * ```There’s a semicolon missing.```

2. What type of error is caught by the compiler?
    * Logic errors.
    * ```Syntax errors.```
    * Run-time errors.

3. **True/False**: Errors which happen during program execution after successful compilation are called run-time errors.
    * False.
    * ```True.```

4. Fill in the blank so that the code is handling the ```FileNotFoundException``` using ```try/catch```

    ```java
    __________ {

    //  Block of code to try

    }
    __________ (__________ e) {

    //  Block of code to handle exceptions

    }
    ```
    * ```FileNotFoundException```
    * ArithmeticException
    * ```catch```
    * ```try```