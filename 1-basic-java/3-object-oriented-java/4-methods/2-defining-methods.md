## Defining Methods
If we were to define a ```checkBalance()``` method for the Savings Account example we talked about earlier, it would look like the following:
```java
public void checkBalance(){
  System.out.println("Hello!");
  System.out.println("Your balance is " + balance);
}
```

The first line, ```public void checkBalance()```, is the method declaration. It gives the program some information about the method:
* ```public``` means that other ```classes``` can access this method. We will learn more about that later in the course.
* The ```void``` keyword means that there is no specific ```output``` from the method. We will see ```methods``` that are not ```void``` later in this lesson, but for now, all of our methods will be ```void```.
* ```checkBalance()``` is the name of the method.

Every method has its own unique method signature which is composed of the method’s name and its parameter type. In this example, the method signature is ```checkBalance()```.

The two print statements are inside the body of the method, which is defined by the curly braces: ```{``` and ```}```.

Anything we can do in our ```main()``` method, we can do in other methods! All of the Java tools you know, like the math and comparison operators, can be used to make interesting and useful methods.

### Keep Reading: AP Computer Science A Students

```checkBalance()``` is considered a non-static method because its signature does not include the keyword ```static``` like the ```main()``` method does. We’ll learn more about non-static methods later in this course.

**Store.java**
```java
public class Store {
  // instance fields
  String productType;
    
  // constructor method
  public Store(String product) {
    productType = product;
  }
    
  // Add advertise method below
    

}
```

**Main.java**
```java
public class Main {
  public static void main(String[] args) {
      
  }
}
```

EXERCISE:
1. In the ```Store``` class, add a new method called ```advertise()``` that is accessible by other classes and does not return anything. Don’t add anything to the body of the method.

    SOLUTION:

    **Store.java**
    ```java
    public class Store {

        // instance fields
        String productType;
            
        // constructor method
        public Store(String product) {
            productType = product;
        }
            
        // Add advertise method below
        public void advertise(){
        }

    }
    ```

2. Well done! Let’s add some print statements inside our ```advertise()``` method. Print these two statements:

    ```git
    "Come spend some money!" 

    "Selling <productType>!" 
    ```

    The value stored in the variable ```<productType>``` should be printed instead of “productType” string.

    Don’t worry if you are not able to see the output. We’ll learn how to use the ```advertise()``` method in later exercises.

    SOLUTION:

    **Store.java**
    ```java
    public class Store {

        // instance fields
        String productType;
            
        // constructor method
        public Store(String product) {
            productType = product;
        }
            
        // Add advertise method below
        public void advertise(){
            System.out.println("Come spend some money!");
            System.out.println("Selling " + productType + "!");
        }

    }
    ```
