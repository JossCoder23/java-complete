## Classes: Constructors
In Java, the constructor is a special type of method defined within the class, used to initialize fields when an instance of the class is created. The name of the constructor method must be the same as the class itself. Generally, the constructor is defined as ```public```. Again, don’t worry about the meaning of the ```public``` keyword for now. We will discuss this in a later exercise.

Let’s look at an updated ```Car``` class, which includes a constructor.
```java
public class Car { 

    // Constructor
    public Car() { 

    // instructions for creating a Car instance 

    }   
} 
```

In the following example, the Car instance is assigned to the variable ferrari:
```java
Car ferrari = new Car(); 
```

In this example, we have created an instance of a ```Car``` class called ```ferrari```.

After the assignment operator, (=), we call the constructor method, ```Car()```, using the keyword new to indicate that we’re creating a ```new``` instance of the ```Car``` class. Omitting the new keyword causes an error.

### Keep Reading: AP Computer Science A Students
If we print the value of the variable ```ferrari``` we would see its memory address: ```Car@76ed5528``` In the above example, our variable ```ferrari``` is declared as a reference data type rather than with a primitive data type like ```int``` or ```boolean```. This means that the variable holds a reference to the memory address of an instance. During its declaration, we specify the class name as the variable’s type, which in this case is ```Car```.

If we use a special value, ```null```, we can initialize a reference-type variable without giving it a reference. If we were to assign ```null``` to an object, it would have a void reference because ```null``` has no value.

For example, consider the following code snippet where we create an instance of a ```Car```, assign it a reference, and then set its value to null:
```java
Car thunderBird = new Car(); 

System.out.println(thunderBird); // Prints: Car@76ed5528 

thunderBird = null; // change value to null 

System.out.println(thunderBird); // Prints: null 
```

It’s important to understand that using a null reference to call a method or access an instance variable will result in a ```NullPointerException``` error.

EXERCISE:
1. Create a constructor for the Store class that prints out the message “I am inside the Store constructor”.

    *Note: do not worry about the error requiring a main() method to be defined. The main() method is inside the Main.java file.*

    SOLUTION:

    **Store.java**

    ```java
    public class Store{
        public Store() {
            System.out.println("I am inside the Store constructor");
        }
    }
    ```

2. Inside the ```main()``` method of a separate class called Main.java (separate file), create an instance of the ```Store``` class and call it ```newStore```.

    SOLUTION:

    **Main.java**
    ```java
    public class Main{
        public static void main(String[] args){
            Store newStore = new Store();
        }
    }
    ```

    OUTPUT
    ```cmd
    I am inside the Store constructor
    ```