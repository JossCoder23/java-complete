## Syntax Errors
When we are writing Java programs, the compiler is our first line of defense against errors. It can catch syntax errors.

Syntax errors represent grammar errors in the use of the programming language. They are the easiest to find and correct. The compiler will tell you where it got into trouble, and its best guess as to what you did wrong.

Some common syntax errors are:

* Misspelled variable and method names
* Omitting semicolons ```;```
* Omitting closing parenthesis ```)```, square bracket ```]```, or curly brace ```}```

Here’s an example of a syntax error message:
```git
Debug.java:5: error: ';' expected
  int year = 2019
                  ^
1 error
```

Usually the error is on the exact line indicated by the compiler, or the line just before it; however, if the problem is incorrectly nested braces, the actual error may be at the beginning of the nested block.

EXERCISE:

1. Inside the file **Debug.java**, there’s a syntax error.

    Compile the code using the terminal and find the syntax error in **Debug.java**.

    OUTPUT:
    ```git
    error ;
    ```

2. Well done! You found that there’s a semicolon missing at the end of the last ```System.out.println()``` statement.

    Fix the bug, recompile the code, then execute it.

    **SOLUTION:**

    **Debug.java**
    ```java
    public class Debug {

        public static void main(String[] args) {
            
            System.out.println("       1");
            System.out.println("     2 3");
            System.out.println("   4 5 6");
            System.out.println("7 8 9 10");
            
        }
    
    }
    ```