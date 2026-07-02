## booleans
Often our programs face questions that can only be answered with yes or no.

Is the oven on? Is the light green? Did I eat breakfast?

These questions are answered with a boolean, a type that references one of two values: ```true``` or ```false```.

We declare boolean variables by using the keyword ```boolean``` before the variable name.
```java
boolean javaIsACompiledLanguage = true;
boolean javaIsACupOfCoffee = false;
```

In future lessons, we’ll see how ```boolean``` values help navigate decisions in our programs.

EXERCISE:
1. Create a variable called ```intsCanHoldDecimals```. Set it to ```true``` if the ```int``` type can hold a decimal number. Set it to ```false``` if the ```int``` type cannot do this.
2. Print out your ```intsCanHoldDecimals``` variable.

    **Booleans.java**
    ```java
    public class Booleans {
        public static void main(String[] args) {    
        
        }
    }
    ```

SOLUTION - ONE:
```java
public class Booleans {
	public static void main(String[] args) {    
        boolean intsCanHoldDecimals = false;
	}
}
```

SOLUTION - TWO:
```java
public class Booleans {
	public static void main(String[] args) {    
        boolean intsCanHoldDecimals = false;
        System.out.println(intsCanHoldDecimals);
	}
}
```

OUTPUT:
```git
false
```