# Planting a Tree
Write your first Java program from scratch by introducing yourself to users and planting a tree for them. You’ll practice creating a class, defining the main method, and organizing print statements.

TASK 1:

We’re starting with a blank Java file named Tree.java.

Define a class that follows the Java naming conventions.
```java
// Define your tree class in this file!
public class Tree {

}
```

TASK 2:

This code produces an error because our program needs a ```main()``` method.

Define this method inside the curly braces of the ```Tree``` class.
```java
// Define your tree class in this file!
public class Tree {
  public static void main(String[] args) {
    
  }
}
```

TASK 3:

Write a comment in ```main()``` that describes the task it will perform.

We’re going to introduce ourselves and print a tree to the screen.

You can use the single-line or multi-line syntax for your comment.
```java
// Define your tree class in this file!
public class Tree {
  public static void main(String[] args) {
    // In this project we build a tree
  }
}
```

TASK 4:

Below your comment, print a message introducing yourself to the user.

Try something like “Hey there, I’m Ariel and I’m learning to code in Java!”

When you run the code, you should see this message printed to the screen.
```java
// Define your tree class in this file!
public class Tree {
  public static void main(String[] args) {
    // In this project we build a tree
    System.out.println("Hey there, I’m Ariel and I’m learning to code in Java!");
  }
}
```

## Planting Trees
TASK 5:

After introducing yourself, use another print statement to output the project goal!

Something like “I’m going to plant a tree today!” or “Ready to get my hands dirty!”
```java
// Define your tree class in this file!
public class Tree {
  public static void main(String[] args) {
    // In this project we build a tree
    System.out.println("Hey there, I’m Ariel and I’m learning to code in Java!");
    System.out.println("I’m going to plant a tree today!” or “Ready to get my hands dirty!");
  }
}
```

TASK 6:

See how the second statement begins on a new line? We’ll use multiple print statements to plant our tree.

For example:
```java
System.out.println("  *  ");
System.out.println(" *** ");
System.out.println(" *** ");
System.out.println("  *  ");
System.out.println("  *  ");   
```

will print a tree like this:
```git
  *  
 *** 
 *** 
  *  
  *  
```

Try it out!
```java
// Define your tree class in this file!
public class Tree {
  public static void main(String[] args) {
    // In this project we build a tree
    System.out.println("Hey there, I’m Jose Pardo and I’m learning to code in Java!");
    System.out.println("I’m going to plant a tree today!” or “Ready to get my hands dirty!");
    
    System.out.println("=====================");

    System.out.println("  *  ");
    System.out.println(" *** ");
    System.out.println(" *** ");
    System.out.println("  *  ");
    System.out.println("  *  "); 
    System.out.println("  *  ");
    System.out.println("* ** *");
    System.out.println("******");
    System.out.println(" **** ");
    System.out.println("  **  "); 
    System.out.println("  **  ");
    System.out.println("~~~~~~"); 
  }
}
```

OUTPUT:
```git
Hey there, I’m Jose Pardo and I’m learning to code in Java!
I’m going to plant a tree today!” or “Ready to get my hands dirty!
=====================
  *  
 *** 
 *** 
  *  
  *  
  *  
* ** *
******
 **** 
  **  
  **  
~~~~~~
```