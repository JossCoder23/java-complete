## String Concatenation
We have covered a lot of built-in functionality in Java throughout this lesson. We’ve seen ```+```, ```-```, ```<```, ```==```, and many other operators. Most of these only work on primitives, but some work on ```String```s too!

Let’s say we want to print out a variable, and we want to describe it as we print it out. For our bank account example, imagine we want to tell the user:
```git
Your username is: <username>
```

With the value of the variable ```username``` displayed.

The ```+``` operator, which we used for adding numbers together, can be used to concatenate ```String```s. In other words, we can use it to join two ```String```s together!
```java
String username = "PrinceNelson";
System.out.println("Your username is: " + username);
```

This code will print:
```git
Your username is: PrinceNelson
```

We can even use a primitive datatype as the second variable to concatenate, and Java will intelligently make it a ```String``` first:
```java
int balance = 10000;
String message = "Your balance is: " + balance;
System.out.println(message);
```

This code will print:
```git
Your balance is: 10000
```

EXERCISE:
1. In our zoo, we have a certain number of animals, stored in ```animals```, of a certain species, stored in ```species```.

    Use ```+``` to make a new ```String``` variable called ```zooDescription```. It should hold a String that looks like:

    ```git
    Our zoo has <animals> <species>s!
    ```
    For example, if we had ```5``` animals that were all of the species ```Masai Giraffe```, the String would say:
    ```git
    Our zoo has 5 Masai Giraffes!
    ```
2. Print out the variable ```zooDescription```!

    **Zoo.java**
    ```java
    public class Zoo {
        public static void main(String[] args){
            int animals = 12;
            String species = "zebra";
        }       
    }
    ```

SOLUTION - ONE:
```java
public class Zoo {
  	public static void main(String[] args){
      int animals = 12;
      String species = "zebra";
      String zooDescription = "Our zoo has " + animals + " " + species + "s!";
    }       
}
```

SOLUTION - TWO:
```java
public class Zoo {
  	public static void main(String[] args){
      int animals = 12;
      String species = "zebra";
      String zooDescription = "Our zoo has " + animals + " " + species + "s!";
      System.out.println(zooDescription);
    }       
}
```

OUTPUT:
```git
Our zoo has 12 zebras!
```