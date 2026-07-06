## Scope

A method is a task that an object of a class performs.

We mark the domain of this task using curly braces: ```{```, and ```}```. Everything inside the curly braces is part of the task. This domain is called the scope of a method.

We can’t access variables that are declared inside a method in code that is outside the scope of that method.

Looking at the ```Car``` class again:
```java
class Car {
    String color;
    int milesDriven;

    public Car(String carColor) {
        color = carColor;
        milesDriven = 0;         
    }

    public void drive() {
        String message = "Miles driven: " + milesDriven;
        System.out.println(message);
    }

    public static void main(String[] args){
        Car myFastCar = new Car("red");
        myFastCar.drive();
    }
}
```

The variable ```message```, which is declared and initialized inside of ```drive```, cannot be used inside of ```main()```! It only exists within the scope of the ```drive()``` method.

However, milesDriven, which is declared at the top of the class, can be used inside all ```methods``` in the class, since it is in the scope of the whole class.

EXERCISE:
1. Let’s see how the scope works!

    Inside the Store.java file, check out the ```advertise()``` method. Notice how we are using ```productType```.

    Now, replace the ```productType``` variable with the ```product``` variable inside the ```advertise()``` method.

    When you run the code, you will notice an error has occurred. This is due to the ```product``` variable not being in the ```advertise()``` method’s scope. The variable ```product``` was declared in the constructor, so we are not able to access it.

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
            
        // advertise method
        public void advertise() {
            String message = "Selling " + product + "!";
            System.out.println(message);
        }
        
    }
    ```

    OUTPUT:
    ```git
    Store.java:12: error: cannot find symbol
        String message = "Selling " + product + "!";
                                  ^
        symbol:   variable product
        location: class Store
    1 error
    ```

2. To correct the error from the previous checkpoint, in the ```advertise()``` method, change the ```product``` variable back to ```productType```.

    Switch over to Main.java and run your code.

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
            
        // advertise method
        public void advertise() {
            String message = "Selling " + productType + "!";
            System.out.println(message);
        }
        
    }
    ```

    **Main.java**
    ```java
    public class Main {
        public static void main(String[] args) {
            String cookie = "Cookies";
            Store cookieShop = new Store(cookie);
            
            cookieShop.advertise();
        }
    }
    ```

    OUTPUT:
    ```git
    Selling Cookies!
    ```