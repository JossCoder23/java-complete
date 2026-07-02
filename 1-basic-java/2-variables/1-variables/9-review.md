## Review
Creating and filling variables is a powerful concept that allows us to keep track of all kinds of data in our program.

In this lesson, we learned how to create and print several different data types in Java, which you’ll use as you create bigger and more complex programs.

We covered:
* ```int```, which stores whole numbers.
* ```double```, which stores bigger whole numbers and decimal numbers.
* ```boolean```, which stores ```true``` and ```false```.
* ```char```, which stores single characters using single quotes.
* ```String```, which stores multiple characters using double quotes.
* Static typing, which is one of the safety features of Java.
* Variable naming conventions.

Practice declaring variables and assigning values to make sure you have a solid foundation for learning more complicated and exciting Java concepts!

EXERCISE:
1. The file **MyProfile.java** contains a class that represents your hiring profile as presented to potential employers.

    In the ```main()``` method, create a variable called ```name``` that holds your name, as a sequence of characters.
2. Create a variable called ```age``` that holds your age as a whole number.
3. Create a variable called ```desiredSalary``` that holds your desired salary per year to a precision of two decimal points.
4. Create a variable called ```gender``` that holds a single character, ```m``` (male), ```f``` (female), ```n``` (for none), or ```o``` (for other).
5. Create a variable called ```lookingForJob``` that holds whether or not you are currently open to job offers.

    ```java
    public class MyProfile {
        public static void main(String[] args) {   

        }
    }
    ```

SOLUTION - ONE:
```java
public class MyProfile {
	public static void main(String[] args) {   
        String name = "Jose Pardo"; 
	}
}
```

SOLUTION - TWO:
```java
public class MyProfile {
	public static void main(String[] args) {   
        String name = "Jose Pardo"; 
        int age = 30;
	}
}
```

SOLUTION - THREE:
```java
public class MyProfile {
	public static void main(String[] args) {   
        String name = "Jose Pardo"; 
        int age = 30;
        double desiredSalary = 4500.23;
	}
}
```

SOLUTION - FOUR:
```java
public class MyProfile {
	public static void main(String[] args) {   
        String name = "Jose Pardo"; 
        int age = 30;
        double desiredSalary = 4500.23;
        char gender = 'm';
	}
}
```

SOLUTION - FIVE:
```java
public class MyProfile {
	public static void main(String[] args) {   
        String name = "Jose Pardo"; 
        int age = 30;
        double desiredSalary = 4500.23;
        char gender = 'm';
        boolean lookingForJob = true;
	}
}
```