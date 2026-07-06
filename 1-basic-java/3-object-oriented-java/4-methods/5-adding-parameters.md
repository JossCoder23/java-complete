## Adding Parameters
We saw how a method’s scope prevents us from using ```variables``` declared in one method in another method. What if we had some information in one method that we needed to pass into another method?

Similar to how we added parameters to ```constructors```, we can customize all other ```methods``` to accept parameters. For example, in the following code, we create a ```startRadio()``` method that accepts a ```double``` parameter, ```stationNum```, and a ```String``` parameter called ```stationName```:
```java
class Car {

  String color;

  public Car(String carColor) {
    color = carColor;        
  }

  public void startRadio(double stationNum, String stationName) {
    System.out.println("Turning on the radio to " + stationNum + ", " + stationName + "!");
    System.out.println("Enjoy!");
  }

  public static void main(String[] args){
    Car myCar = new Car("red");
    myCar.startRadio(103.7, "Meditation Station");
  }
}
```

Adding parameter values impacts our method’s signature. Like constructor signatures, the method signature includes the method name as well as the parameter types of the method. The signature of the above method is ```startRadio(double, String)```.

In the ```main()``` method, we call the ```startRadio()``` method on the ```myCar``` object and provide a ```double``` argument of ```103.7``` and ```String``` argument of ```"Meditation Station"```, resulting in the following output:
```git
Turning on the radio to 103.7, Meditation Station!
Enjoy!
```

Note that when we call on a method with multiple parameters, the arguments given in the call must be placed in the same order as the parameters appear in the signature. If the argument types do not match the parameter types, we’ll receive an error.

### Keep Reading: AP Computer Science A Students

Through method overloading, our Java programs can contain multiple methods with the same name as long as each method’s parameter list is unique. For example, we can recreate our above program to contain two startRadio() methods:
```java
// Method 1
public void startRadio(double stationNum, String stationName) {
  System.out.println("Turning on the radio to " + stationNum + ", " + stationName + "!");
  System.out.println("Enjoy!");
}
  
// Method 2
public void startRadio(double stationNum) {
  System.out.println("Turning on the radio to " + stationNum + "!");
}

public static void main(String[] args){
  Car myCar = new Car("red");
  // Calls the first startRadio() method
  myCar.startRadio(103.7, "Meditation Station");

  // Calls the second startRadio() method
  myCar.startRadio(98.2);
}
```

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
        
    // greetCustomer() method
    
}
```

**Main.java**
```java
public class Main{
    public static void main(String[] args) {
        Store lemonadeStand = new Store("Lemonade");
        
    }
}
```

EXERCISE:
1. Let’s create a method to greet the customers.

    In Store.java, add a ```greetCustomer()``` method to the ```Store``` class that is accessible by other classes and does not return anything.

    *Note: it is okay to get an error regarding a missing main() method. The main() method is defined in Main.java.*

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
            
        // greetCustomer() method
        public void greetCustomer() {
            
        }  

    }
    ```

2. Now, add a ```String``` parameter to the ```greetCustomer()``` method called ```customerName```.

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
            
        // greetCustomer() method
        public void greetCustomer(String customerName) {
            
        }  

    }
    ```

3. Inside ```greetCustomer()```, print a string that has the following format:
    ```git
    "Welcome to the store, " + customerName + "!"
    ```

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
            
        // greetCustomer() method
        public void greetCustomer(String customerName) {
            System.out.println("Welcome to the store, " + customerName + "!");
        }  

    }
    ```

4. Inside the ```main()``` method of Main.java, call the greetCustomer() method on the ```lemonadeStand``` object. Pass in a name of your choice!

    SOLUTION:

    **Main.java**
    ```java
    public class Main{
        public static void main(String[] args) {
            Store lemonadeStand = new Store("Lemonade");
            lemonadeStand.greetCustomer("Jose Pardo");
        }
    }
    ```

    OUTPUT:
    ```git
    Welcome to the store, Jose Pardo!
    ```