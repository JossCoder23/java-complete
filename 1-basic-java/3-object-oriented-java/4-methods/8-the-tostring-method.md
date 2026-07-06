## The toString() Method
When we print out Objects, we often see a String that is not very helpful in determining what the Object represents. In the last lesson, we saw that when we printed our ```Store``` objects, we would see ```output``` like:
```git
Store@6bc7c054
```

where ```Store``` is the name of the object and ```6bc7c054``` is its position in memory.

This doesn’t tell us anything about what the ```Store``` sells, the price, or the other instance fields we’ve defined. We can add a method to our ```classes``` that makes this printout more descriptive.

When we define a toString() method for a class, we can return a ```String``` that will print when we print the object:
```java
class Car {

    String color;

    public Car(String carColor) {
        color = carColor;
    }

    public static void main(String[] args){
        Car myCar = new Car("red");
        System.out.println(myCar);
    }

    public String toString(){
        return "This is a " + color + " car!";
    }

}
```

When this runs, the command ```System.out.println(myCar)``` will print ```This is a red car!```, which tells us about the Object ```myCar```.

**Store.java**
```java
public class Store {

    // instance fields
    public String productType;
    public double price;
        
    // constructor method
    public Store(String product, double initialPrice) {
        productType = product;
        price = initialPrice;
    }
  
}
```

**Main.java**
```java
public class Main {
    public static void main(String[] args) {
        Store lemonadeStand = new Store("Lemonade", 3.75);
        Store cookieShop = new Store("Cookies", 5);
    }
}
```

EXERCISE:
1. The ```Store``` class currently does not contain a custom definition of ```toString()```. Let’s see what happens when we call ```System.out.println()``` on two instances of ```Store```.

    Call ```System.out.println()``` on ```lemonadeStand``` and ```cookieShop``` inside the ```main()``` method of **Main.java**.

    SOLUTION:

    **Main.java**
    ```java
    public class Main {
        public static void main(String[] args) {
            Store lemonadeStand = new Store("Lemonade", 3.75);
            Store cookieShop = new Store("Cookies", 5);
            System.out.println(lemonadeStand);
            System.out.println(cookieShop);
        }
    }
    ```

    OUTPUT:
    ```git
    Store@7ad041f3
    Store@251a69d7
    ```

2. When we print our objects, we want them to return a meaningful and informative string.

    Create a ```toString()``` method inside the ```Store``` class. Leave it empty for now.

    *Note: It is okay to get an error in the output claiming that toString() should return a String. You will fill out the toString() method in the next step.*

    SOLUTION:

    **Store.java**
    ```java
    public class Store {

        // instance fields
        public String productType;
        public double price;
            
        // constructor method
        public Store(String product, double initialPrice) {
            productType = product;
            price = initialPrice;
        }

        public String toString() {

        }
        
    }
    ```

3. Fill in the ```toString()``` method of the ```Store``` class such that it returns this string:

    “This store sells ```<productType>``` at a price of ```<price>```.”

    Where ```<productType>``` and ```<price>``` are the values in the instance fields of the same name.

    For example, if we had a hat store implementation of ```Store``` where hats cost 8, the string would be:
    ```git
    This store sells hats at a price of 8. 
    ```

    *Note: If you click “Run” while you still have the Store.java file open, you will get an error in the output regarding a missing main() method. This is an okay error to get because the method is located in the Main.java file.*

    SOLUTION:

    **Store.java**
    ```java
    public class Store {

        // instance fields
        public String productType;
        public double price;
            
        // constructor method
        public Store(String product, double initialPrice) {
            productType = product;
            price = initialPrice;
        }

        public String toString() {
            return "This store sells " + productType + " at a price of " + price + ".";
        }
        
    }
    ```

4. Open **Main.java** and click “Run”.

    Do our objects give us information about them?

    SOLUTION:

    ```git
    This store sells Lemonade at a price of 3.75.
    This store sells Cookies at a price of 5.0.
    ```