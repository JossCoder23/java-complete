## Java and the Command Line

### A brief overview of running Java through the command line.

While there are many IDEs with built-in execution capabilities (Eclipse and IntelliJ for example), Java can also be run directly from the command line.

In this article, we’ll cover how to download and run Java on your personal computer, as well as how to utilize the ```String[] args``` parameter of the main method.

### Downloading Java

You more than likely have already interacted with a version of Java on your computer as many programs use it to operate. This version of Java, the version that is used simply to run programs, is called the Java Runtime Environment, and essentially takes the compiled Java byte code and allows those generic files to be run specifically on your type of computer. This is one of the core principles that has allowed Java to become as popular as it has.

As a developer though, you need the Java Development Kit, or JDK, which allows you access to the classes and interfaces of the core Java language that you use here on Codecademy such as ```System.out.println()```. The current version of Java we have here at Codecademy can be found by typing the command ```java --version``` into a terminal when you are doing a lesson.

Java’s JDK is available (for free) through Oracle’s website. There are several types, each with a specific purpose and you can explore these use cases on Oracle’s website, the vast majority of Java development though, occurs in the SE or Standard Edition of the JDK. You can find the most recent version of the JDK here,and older versions of Java, such as Java 9 like we are using here.

### Compiling Java

Before you can run the program from the command line, you must compile it. Open your terminal or command prompt (depending on OS), and navigate to the directory where the file you want to run is located. Once there, use ```javac``` and the filename to compile:
```git
javac MyClass.java
```

*If you’re new to the command line or need a refresher on navigation, take a look at our command line cheatsheet for more guidance.*

This creates the ```.class``` file that can be executed. However, if there are any bugs found in your program, they will be flagged at this point, and the executable ```.class``` file will not be created. You won’t be able to run the file until it compiles with no issues.

### Running Java

Once you have your executable file, use ```java``` and the name of the class to run it:
```git
java MyClass
```

**Note**: Do not include the ```.java``` or ```.class``` suffixes, only use the name of the class.

Let’s say we had the following Java class:
```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello world!");
    }
}
```

We would compile this using:
```git
javac HelloWorld.java
```

Then run it using:
```git
java HelloWorld
```

It would output the following:
```git
Hello world!
```

### main Method Parameters

Each Java program must have a main method, and every main method contains the parameters ```String[] args```, but what does that mean?

```args``` is an array of ```String```s that is passed to the program when it’s run. (Click here for a refresher on arrays in Java.) We don’t need to pass anything in, but we can if we want to. For example, we can edit our ```HelloWorld``` class to use elements from ```args```:
```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello world, my name is " + args[0] + "!");
    }
}
```

Note that we access the elements of the ```args``` array the same way we would access the elements of any other array.

Let’s use the new ```HelloWorld``` class to introduce ourselves! First, we’ll compile our class the same way we did before:
```git
javac HelloWorld.java
```

Next we’ll run it. However, this time, we’ll add in a ```String``` argument:
```git
java HelloWorld Batman
```

The program will output the following:
```git
Hello world, my name is Batman!
```

Two extra takes aways from the ```main``` method:

* All arguments passed via the command line, like ```Batman``` is above, are passed in as Strings. So if we have a program that asks the user to input their name and age via the command line, we have to treat the age as a String until we parse (convert it from a String) the age into an integer.
* A Java program, in fact, most Java programs, is made up of many, many files. Some of these files will have ```main``` methods and others will not, when we use the ```java``` command, we are specifying which Java class inside the program that we should look for the ```main``` method in.