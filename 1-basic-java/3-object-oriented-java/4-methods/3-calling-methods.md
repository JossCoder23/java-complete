## Calling Methods

When we add a non-static method to a class, it becomes available to use on an object of that class. In order to have our methods get executed, we must call the method on the object we created.

Let’s add a non-static ```startEngine()``` method to our ```Car``` class from the previous lesson. Inside the ```main()``` method, we’ll call ```startEngine()``` on the ```myFastCar``` object:

```java
class Car {

  String color;

  public Car(String carColor) {
    color = carColor;
  }

  public void startEngine() {
    System.out.println("Starting the car!");
    System.out.println("Vroom!");
  }

  public static void main(String[] args){
    Car myFastCar = new Car("red");
    // Call a method on an object 
    myFastCar.startEngine();
    System.out.println("That was one fast car!");
  }
}
```

Let’s take a closer look at the method call:
```java
myFastCar.startEngine();
```

First, we reference our object ```myFastCar```. Then, we use the dot operator (.) to call the method ```startEngine()```. Note that we must include parentheses ```()``` after our method name in order to call it.

If we run the above program, we will get the following output.
```git
Starting the car!
Vroom!
That was one fast car!
```
Code generally runs in a top-down order where code execution starts at the top of a program and ends at the bottom of a program; however, methods are ignored by the ```compiler``` unless they are being called.

When a method is called, the compiler executes every statement contained within the method. Once all method instructions are executed, the top-down order of execution continues. This is why ```Starting the car!``` and ```Vroom!``` are outputted before That was ```one fast car!```.

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
    System.out.println("Selling " + productType + "!");
    System.out.println("Come spend some money!");
  }  
}
```

**Main.java**
```java
public class Main {
  public static void main(String[] args) {
    Store lemonadeStand = new Store("Lemonade");
  }
}
```

EXERCISE:
1. Now our ```Store``` class has a new method called ```advertise()```, but we didn’t see its output.

    In the ```main()``` method of Main.java, call the ```advertise()``` method of the ```lemonadeStand``` instance and observe the displayed output.

    SOLUTION:

    **Main.java**
    ```java
    public class Main {
        public static void main(String[] args) {
            Store lemonadeStand = new Store("Lemonade");
            lemonadeStand.advertise();
        }
    }
    ```

2. Now, replace the argument “Lemonade” with “Coffee” in the instance definition and run the code.

    SOLUTION:

    **Main.java**
    ```java
    public class Main {
        public static void main(String[] args) {
            Store lemonadeStand = new Store("Coffee");
            lemonadeStand.advertise();
        }
    }
    ```