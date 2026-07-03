## Classes: Constructor Parameters
In Java, parameters are placeholders that we can use to pass information to a method.

Since the constructor is a method, we can include parameters to assign values to instance fields.

Here the ```Car``` constructor has a parameter: ```String carColor```:
```java
public class Car { 
    
    public String color; 

    // constructor method with a parameter 
    public Car(String carColor) { 
        // parameter value assigned to the field 
        color = carColor; 
    }

} 
```

Now, when we create a new instance of the ```Car``` class and pass in a string value to the constructor, it will be stored in the parameter ```carColor```. Inside the constructor, we can use this passed value however we want. In our example, we assign the value stored in ```carColor``` to the instance field ```color```.

A method can be characterized by its signature, which is the name, number of, and parameters of the method. In the above example, the signature is ```Car(String carColor)```.

Later, we’ll learn how to pass values into a method!

There are two types of parameters: formal and actual. The parameter we defined in the above example, ```String carColor```, is a formal parameter. We can think of them as ```variables``` that will store the data that is passed into a method. It specifies the type and name of the data.

We’ll learn about actual parameters in the next exercise.

For now, let’s practice working with constructor parameters.

### Keep Reading: AP Computer Science A Students
A class can have multiple constructors. We can differentiate them based on their parameters. The signature helps the compiler to differentiate between different methods.

For example, here we have defined two constructors:
```java
public class Car { 
    public String color; 
    public int mpg; 
    public boolean isElectric; 

    // constructor 1 
    public Car(String carColor, int milesPerGallon) { 
        color = carColor; 
        mpg = milesPerGallon; 
    } 

    // constructor 2 
    public Car(boolean electricCar, int milesPerGallon) { 
        isElectric = electricCar; 
        mpg = milesPerGallon; 
    } 
} 
```

The first constructor has two parameters: ```String carColor``` and ```int milesPerGallon```.

While the second one has these: ```boolean electricCar``` and ```int milesPerGallon```.

The values will help the compiler to decide which constructor to use. For example, ```Car myCar = new Car(true, 40)``` will be created by the second constructor because the arguments match the type and order of the second constructor’s signature.

When we don’t define the constructor, the Java compiler creates a default constructor that assigns default values to an instance. Default values can be created by assigning values to the instance fields during their declaration:
```java
public class Car { 
    public String color = "red"; 
    public boolean isElectric = false; 
    public int cupHolders = 4; 

    public static void main(String[] args) { 
        Car myCar = new Car(); 
        System.out.println(myCar.color); // Prints: red 
    } 
} 
```

Notice that the color instance field of the ```myCar``` object will have a red value because we’ve already defined the default value during the declaration.

**Store.java**

EXERCISE:
1. Add a formal parameter to the ```Store()``` constructor called ```String product```.
    ```java
    public class Store{

        public String productType;

        public Store(String product){
            
        }

    }
    ```

2. Inside the constructor, assign ```product``` parameter to the instance field ```productType```.
    ```java
    public class Store{

        public String productType;

        public Store(String product){
            productType = product;
        }

    }
    ```