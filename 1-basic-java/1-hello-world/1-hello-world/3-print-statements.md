## Print Statements

Let’s take a closer look at this instruction from our previous program:
```java
System.out.println("Hello World");
```

Print statements output information to the screen (also referred to as the output terminal). Let’s break this line of code down a little more. Don’t worry if some of the terms here are new to you. We’ll dive into what all of these are in much more detail later on!

* ```System``` is a built-in Java class that contains useful tools for our programs.
* ```out``` is short for “output”.
* ```println``` is short for “print line”.

We can use ```System.out.println()``` whenever we want the program to create a new line on the screen after outputting a value:
```java
System.out.println("Hello World");
System.out.println("Today is a great day to code!");
```

After ```"Hello World"``` is printed, the output terminal creates a new line for the next statement to be outputted. This program will print each statement on a new line like so:
```git
Hello World
Today is a great day to code!
```

We also can output information using ```System.out.print()```. Notice that we’re using ```print()```, not ```println()```. Unlike ```System.out.println()```, this type of print statement outputs everything on the same line. For example:
```java
System.out.print("Hello ");
System.out.print("World");
```

The above code will have the following output:
```git
Hello World
```

In this example, if you were to use ```print()``` or ```println()``` again, the new text will print immediately after ```World``` on the same line. It’s important to remember where you left your program’s “cursor”. If you use ```println()``` the cursor is moved to the next line. If you use ```print()``` the cursor stays on the same line.

**Note**: Going forward after this exercise, all exercises will use ```System.out.println()``` to output values. You will get to practice using ```System.out.print()``` statements in the Checkpoints below, however.

EXERCISE:
1. Inside ```main()``` and underneath the print statement ```System.out.println("Let's play hide and seek.");```, output the following two statements using ```System.out.print()```:
    * ```"Three..."```
    * ```"Two..."```

2. Underneath your previous statements, output the following two text values using ```System.out.println()```:
    * ```"One..."```
    * ```"Ready or not, here I come!"```
    ```java
    public class HideAndSeek {
        public static void main(String[] args) {
            System.out.println("Let's play hide and seek.");


        }
    }
    ```

SOLUTION: ONE
```java
public class HideAndSeek {
  public static void main(String[] args) {
    System.out.println("Let's play hide and seek.");
    System.out.print("Three...");
    System.out.print("Two...");
  }
}
```

OUTPUT:
```git
Let's play hide and seek.
Three...Two...
```

SOLUTION: TWO
```java
public class HideAndSeek {
  public static void main(String[] args) {
    System.out.println("Let's play hide and seek.");
    System.out.print("Three...");
    System.out.print("Two...");
    System.out.println("One...");
    System.out.println("Ready or not, here I come!");
  }
}
```

OUTPUT:
```git
Let's play hide and seek.
Three...Two...One...
Ready or not, here I come!
```