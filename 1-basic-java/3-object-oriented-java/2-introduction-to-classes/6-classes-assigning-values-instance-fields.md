## Classes: Assigning Values to Instance Fields
Since the constructor now accepts a parameter, let’s see how we can use this constructor to create an instance of an object with initial values for its fields.

To use the constructor, we call it just as we would an ordinary method and pass in values for the parameters. These values, known as arguments, will be used to initialize the instance fields of the created object.

Let’s revisit our previous example of the ```Car``` class.
```java
public class Car { 
    public String color; 

    public Car(String carColor) { 
        // assign parameter value to instance field 
        color = carColor; 
    } 
} 
```

In this case, when creating a specific instance of ```Car``` called ```ferrari```, we pass the string “red” as the value for the ```carColor``` parameter.
```java
class Main{ 
    public static void main(String[] args){ 
        Car ferrari = new Car("red"); 
    } 
}  
```

When passing in values to a constructor, just like an ordinary method, the type of the value must match the type of the parameter.

In the code, we pass the ```String``` value “red” to the constructor method call: ```new Car("red")```. The parameter ```carColor``` of type ```String``` now refers to the value passed in during the method call, which is “red”.

The field ```color``` of the object ```ferrari``` now has a value of “red”.

Remember, that we can access the fields of an object by using the dot operator like so:
```java
ferrari.color; // "red" 
```

### Keep Reading: AP Computer Science A Students
An argument refers to the actual values passed during the method call while a parameter refers to the vaiables declared in the method signature.

When we pass an argument, a copy of the argument value is passed to the parameter rather than the actual variables. This process of calling a method with an argument value is called a call-by-value.

For example, we passed the ```String``` value “red” as an argument, but a copy of this value is assigned to the parameter ```carColor```.

**Main.java**

```java
public class Main{
    public static void main(String[] args) {    

    }
}
```

EXERCISE:
1. Create a new instance of ```Store``` called ```lemonadeStand``` in the ```main()``` method of Main.java and pass “lemonade” as the argument.