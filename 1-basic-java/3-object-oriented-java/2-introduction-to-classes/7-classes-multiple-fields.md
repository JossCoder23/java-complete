## Classes: Multiple Fields
Objects are not limited to a single instance field. We can declare as many fields as necessary for our program’s requirements. To illustrate this, let’s add two more instance fields to our Car instances.

We’ll add a ```boolean isRunning```, which represents whether the car engine is on or not, and an ```int velocity```, which indicates the speed at which the car is traveling.

**Car.java**
```java
public class Car { 
    String color; 

    // new fields! 
    boolean isRunning; 
    int velocity; 

    // new parameters that correspond to the new fields 
    public Car(String carColor, boolean carRunning, int milesPerHour) { 
        color = carColor; 

        // assign new parameters to the new fields 
        isRunning = carRunning; 
        velocity = milesPerHour; 
    } 
} 
```

**Main.java**
```java
Public class Main(){ 

    public static void main(String[] args) { 
        // new values passed into the method call 
        Car ferrari = new Car("red", true, 27); 
        Car renault = new Car("blue", false, 70); 

        System.out.println(renault.isRunning); // false 
        System.out.println(ferrari.velocity); // 27 
    } 

} 

```

Now, the constructor has two new parameters: ```boolean carRunning``` and ```int milesPerHour```.

Remember, it’s important to pass the arguments in the same order as they are listed in the parameters.
```java
// values match types, no error 
Car honda = new Car("green", false, 0); 

// values do not match types, error! 
Car junker = new Car(true, 42, "brown"); 
```

Let’s practice this concept!

**Store.java**
```java
public class Store {
    
    // instance fields
    public String productType;
    
    // constructor method
    public Store(String product) {
        productType = product;
    }

}
```

**Main.java**
```java
public class Main{
    public static void main(String[] args) {    

    }
}
```

EXERCISE:
1. Let’s add more to our ```Store``` class.

    Add these two fields ```int inventoryCount``` and ```double inventoryPrice``` to ```Store```.

    **Store.java**
    ```java
    public class Store {
        // instance fields
        public String productType;
        int inventoryCount;
        double inventoryPrice;
        
        // constructor method
        public Store(String product) {
            productType = product;
        }
    }
    ```

2. Add two new parameters to the ```Store``` constructor method, ```int count``` and ```double price```. The final order of the parameters should be ```product```, ```count```, ```price```.

    For example, ```product``` is of type ```String``` because that value is assigned to the instance field ```String productType```.
    
    **Store.java**
    ```java
    public class Store {
        // instance fields
        public String productType;
        int inventoryCount;
        double inventoryPrice;
        
        // constructor method
        public Store(String product, int count, double price) {
            productType = product;
        }
    }
    ```


3. Inside the ```Store``` constructor, assign the parameter values to the appropriate instance fields.
   
    **Store.java**
    ```java
    public class Store {
        // instance fields
        public String productType;
        int inventoryCount;
        double inventoryPrice;
        
        // constructor method
        public Store(String product, int count, double price) {
            productType = product;
            inventoryCount ? count;
            inventoryPrice = price;
        }
    }
    ```

4. Now create another instance of ```Store``` called ```cookieShop``` in the ```main()```method of **Main.java**.

    ```CookieShop``` has a product called “cookies”. It has 12 cookies to sell and each cookie costs 3.75.

    **Main.java**
    ```java
    public class Main{
        public static void main(String[] args) {    
            Store cookieShop = new Store("cookies", 12, 3.75);
        }
    }
    ```
    

