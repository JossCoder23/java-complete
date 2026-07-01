## Compilation: Creating Executables

Compilation helped us catch an error. Now that we’ve corrected the file, let’s walk through a successful compilation.

As a reminder, we can compile a **.java** file from the terminal with the command:
```git
javac Whales.java
```

If the file compiles successfully, this command produces an *executable* class: **FileName.class**. Executable means we can run this program from the terminal.

We run the executable with the command:
```git
java Whales
```

Note that we leave off the **.class** part of the filename.

Here’s a full compilation cycle as an example:
```java
// within the file: Welcome.java
public class Welcome {
  public static void main(String[] args) {
    System.out.println("Welcome to Codecademy's Java course!");
  }
}
```

We have one file: **Welcome.java**. We compile with the command:
```git
javac Welcome.java
```

The terminal shows no errors, which indicates a successful compilation.

We now have two files:

1. **Welcome.java**, our original file with Java syntax.
2. **Welcome.class**, our compiled file with Java bytecode, ready to be executed by the Java Virtual Machine.

We can execute the compiled class with the command:
```git
java Welcome
```

The following is printed to the screen:
```git
Welcome to Codecademy's Java course!
```

EXERCISE:
1. Let’s compile and execute our program!

    Run the ```ls``` command in the terminal to see the uncompiled .java file.

    Press the ```Check Work``` button after you finish each checkpoint.

2. Compile the file from the terminal and then press the ```Check Work``` button.

3. Enter ```ls``` again to see the new .class file.

    Run the executable file from the terminal and then press the ```Check Work``` button.

    ```java
    public class Compiling {
        public static void main(String[] args) {
            
            System.out.println("Java is a class-based language.");
            System.out.println("Java classes have a 'main' method.");
            System.out.println("Java statements end with a semicolon.");

            System.out.println("Programming is... fun!");
            
        }
    }
    ```

SOLUTION: ONE - CMD
```git
ls
```

OUTPUT:
```git
Compiling.java
```

SOLUTION: TWO - CMD
```git
javac Compiling.java
```

SOLUTION: THREE - CMD
```
java Compiling
```

OUTPUT:
```git
Java is a class-based language.
Java classes have a 'main' method.
Java statements end with a semicolon.
Programming is... fun!
```
