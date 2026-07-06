## Returns
Remember, ```variables``` can only exist in the scope that they were declared in. We can use a value outside of the method it was created in if we return it from the method.

We return a value by using the keyword ```return```:
```java
public int numberOfTires() {
    int tires = 4;
    // return statement
    return tires;
}
```

This method, called ```numberOfTires()```, returns ```4```. Once the return statement is executed, the ```compiler``` exits the function. Any code that exists after the return statement in a function is ignored.

In past exercises, when creating new ```methods```, we used the keyword ```void```. Here, we are replacing ```void``` with ```int```, to signify that the return type is an ```int```.

The void keyword (which means “completely empty”) indicates that no value is returned after calling that method.

A non-void method, like ```numberOfTires()``` returns a value when it is called. We can use datatype keywords (such as ```int```, ```char```, etc.) to specify the type of value the method should return. The return value’s type must match the return type of the method. If the return expression is compatible with the return type, a copy of that value gets returned in a process known as return by value.

Unlike void methods, non-void methods can be used as either a variable value or as part of an expression like so:
```java
public static void main(String[] args){
    Car myCar = new Car("red");
    int numTires = myCar.numberOfTires();
}
```

Within ```main()```, we called the ```numberOfTires()``` method on ```myCar```. Since the method returns an ```int``` value of ```4```, we store the value in an integer variable called ```numTires```. If we printed ```numTires```, we would see ```4```.

### Keep Reading: AP Computer Science A Students

We learned how to return primitive values from a method, but what if we wanted our method to return an object? Returning an object works a little differently than returning a primitive value. When we return a primitive value, a copy of the value is returned; however, when we return an object, we return a reference to the object instead of a copy of it.

Let’s create a second class, ```carLot```, that takes in a ```Car``` as a parameter and contains a method which returns a ```Car``` object.

```java
class CarLot {
    Car carInLot;
    public CarLot(Car givenCar) {
        carInLot = givenCar;
    }

    public Car returnACar() {
        // return Car object
        return carInLot;
    }

    public static void main(String[] args) {
        Car myCar = new Car("red", 70);
        System.out.println(myCar); 
        CarLot myCarLot = new CarLot(myCar);
        System.out.println(myCarLot.returnACar());
    }
}
```

This code outputs the same memory address because myCar and carInLot have the same reference value:
```git
Car@2f333739
Car@2f333739
```

**Store.java**
```java
public class Store {

    // instance fields
    String productType;
    public double price;
        
    // constructor method
    public Store(String product, double initialPrice) {
        productType = product;
        price = initialPrice;
    }
        
    // increase price method
    public void increasePrice(double priceToAdd){
        double newPrice = price + priceToAdd;
        price = newPrice;
    }
        
}
```

**Main.java**
```java
public class Main {
    public static void main(String[] args) {
        Store lemonadeStand = new Store("Lemonade", 3.75);
        lemonadeStand.increasePrice(1.50);
        System.out.println(lemonadeStand.price);
    }
}
```

EXERCISE:
1. Add a new method called ```getPriceWithTax()``` in the ```Store``` class that will return the price of the product including the tax.

    Set the return type to ```double``` to indicate that it returns a double value, and it should take in no parameters.

    For now, leave the body of the method empty.

    SOLUTION:

    **Store.java**
    ```java
    public class Store {

        // instance fields
        String productType;
        double price;
        double tax = 0.08;
            
        // constructor method
        public Store(String product, double initialPrice) {
            productType = product;
            price = initialPrice;
        }
            
        // increase price method
        public void increasePrice(double priceToAdd){
            double newPrice = price + priceToAdd;
            price = newPrice;
        }
            
        // get price with tax method
        public double getPriceWithTax() {}

    }
    ```

2. Inside the ```Store``` class, we have an instance field called ```double tax``` with the value of ```0.08```.

    We need another variable to calculate the total price of the product including tax.

    Inside the ```getPriceWithTax()``` method, create a variable called ```totalPrice``` of type ```double``` and set it equal to the new price with tax. The formula for calculating a price with tax is the following:

    *totalPrice = price + price x tax*

    *Note: for testing purposes, please write the formula exactly as we have shown it. The tests may fail otherwise.*

    SOLUTION:

    **Store.java**
    ```java
    public class Store {

        // instance fields
        String productType;
        double price;
        double tax = 0.08;
            
        // constructor method
        public Store(String product, double initialPrice) {
            productType = product;
            price = initialPrice;
        }
            
        // increase price method
        public void increasePrice(double priceToAdd){
            double newPrice = price + priceToAdd;
            price = newPrice;
        }
            
        // get price with tax method
        public double getPriceWithTax() {
            double totalPrice = price + price * tax;
        }

    }
    ```   

3. At the end of ```getPriceWithTax()``` method, return the variable ```totalPrice```.

    SOLUTION:

    **Store.java**
    ```java
    public class Store {

        // instance fields
        String productType;
        double price;
        double tax = 0.08;
            
        // constructor method
        public Store(String product, double initialPrice) {
            productType = product;
            price = initialPrice;
        }
            
        // increase price method
        public void increasePrice(double priceToAdd){
            double newPrice = price + priceToAdd;
            price = newPrice;
        }
            
        // get price with tax method
        public double getPriceWithTax() {
            double totalPrice = price + price * tax;
            return totalPrice;
        }

    }
    ``` 

4. Inside ```main()``` in Main.java, create a ```double``` variable ```lemonadePrice``` and set it to ```lemonadeStand.getPriceWithTax()```.

    Also, print your results.

    SOLUTION:

    **Main.java**
    ```java
    public class Main {
        public static void main(String[] args) {
            Store lemonadeStand = new Store("Lemonade", 3.75);
            double lemonadePrice = lemonadeStand.getPriceWithTax();
            System.out.println(lemonadePrice);
        }
    }
    ``` 

    OUTPUT:
    ```git
    4.05
    ```
    