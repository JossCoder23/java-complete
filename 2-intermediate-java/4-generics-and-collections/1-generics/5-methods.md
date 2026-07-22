## Methods

We’ve covered generic classes and interfaces, but what can we do if we want one of our methods to be generic and not the whole class or interface? We can create generic methods to do just that. For example:

```java
public class StringBox {

    private String data;

    public <T> boolean isString(T item) {
        return item instanceof String; 
    }

}

StringBox box = new StringBox();
box.isString(5); // Returns false
```

In the example above, using the class ```StringBox```, we created the generic method ```isString()``` with a generic type ```T``` as a method parameter. It’s important to note that generic methods need to include the type parameter, ```<T>``` in our example, before the return type, even if the return type is ```void```. The generic method is called like any other method as shown.

We can also do this with ```static``` methods. Their signatures have the same requirements except for also needing the ```static``` keyword. For example:

```java
public class StringBox {

    private String data;

    public static <T> boolean isString(T item) {
        return item instanceof String; 
    }

}
StringBox.isString(5);  // Returns false
```

In the example above, we see how we made the ```isString()``` a ```static``` method by adding ```static``` to the method signature. We call it by using the class name instead of an object.

Let’s practice creating generic methods.

**Main.java**
```java
public class Main {
    public static void main(String[] args) {
        String test1 = "Double";
        double test2 = 5.8;

        // Enter code below...  
    }
}
```

**EXERCISE:**
1. Let’s define a generic method in our class so we can detect ```Double``` types.

    In **Main.java**, define a generic, ```static``` method named ```isDouble()``` with a ```T``` type parameter named ```object``` and a ```boolean``` return type.

    **SOLUTION:**
    ```java
    public class Main {

        public static <T> boolean isDouble(T object) {

        }

        public static void main(String[] args) {
            
            String test1 = "Double";
            double test2 = 5.8;

            // Enter code below...  


        }

    }
    ```

2. Let’s complete the body of ```isDouble()``` to return ```true``` if ```object``` is an instance of ```Double``` and ```false``` otherwise.

    **SOLUTION:**
    ```java
    public class Main {

        public static <T> boolean isDouble(T object) {
            return object instanceof Double;
        }

        public static void main(String[] args) {
            
            String test1 = "Double";
            double test2 = 5.8;

            // Enter code below...  


        }
        
    }
    ```

3. Let’s try calling our generic method using the variables provided.

    In ```main()``` we’ve provided two test cases variables, ```test1``` & ```test2```. Call

    * ```isDouble()``` with ```test1``` and store the result in a ```boolean``` type named ```isTest1Double```.
    * ```isDouble()``` with ```test2``` and store the result in a ```boolean``` type named ```isTest2Double```.

    Call ```System.out.println()``` twice to output ```isTest1Double``` & ```isTest2Double```.

    **SOLUTION:**
    ```java
    public class Main {

        public static <T> boolean isDouble(T object) {
            return object instanceof Double;
        }

        public static void main(String[] args) {
            
            String test1 = "Double";
            double test2 = 5.8;

            // Enter code below...  
            boolean isTest1Double = Main.isDouble(test1);
            boolean isTest2Double = Main.isDouble(test2);
            System.out.println(isTest1Double);
            System.out.println(isTest2Double);

        }
        
    }
    ```