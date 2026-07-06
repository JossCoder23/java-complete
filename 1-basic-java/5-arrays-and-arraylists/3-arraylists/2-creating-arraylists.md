## Creating ArrayLists
To create an ```ArrayList```, we need to declare the type of objects it will hold, just as we do with arrays:
```java
ArrayList<String> babyNames;
```

We use angle brackets ```<``` and ```>``` to declare the type of the ```ArrayList```. These symbols are used for generics. Generics are a Java construct that allows us to define classes and objects as parameters of an ```ArrayList```. For this reason, we can’t use primitive types in an ```ArrayList```:
```java
// This code won't compile:
ArrayList<int> ages;

// This code will compile:
ArrayList<Integer> ages;
```

The ```<Integer>``` generic has to be used in an ```ArrayList``` instead. You can also use ```<Double>``` and ```<Character>``` for types you would normally declare as ```double```s or ```char```s.

We can initialize to an empty ```ArrayList``` using the ```new``` keyword:
```java
// Declaring:
ArrayList<Integer> ages;
// Initializing:
ages = new ArrayList<Integer>();

// Declaring and initializing in one line:
ArrayList<String> babyNames = new ArrayList<String>();
```

**ToDos.java**
```java
// Declaring:
ArrayList<Integer> ages;
// Initializing:
ages = new ArrayList<Integer>();

// Declaring and initializing in one line:
ArrayList<String> babyNames = new ArrayList<String>();
```

EXERCISE:
1. Import the ```ArrayList``` package from ```java.util```.

    SOLUTION:

    ```java
    // import the ArrayList package here:
    import java.util.ArrayList;

    class ToDos {
    
        public static void main(String[] args) {
            
            // Create toDoList below:
            
            
        }
    
    }
    ```

2. Create a new ```ArrayList``` that will contain ```String``` elements and call it ```toDoList```.

    SOLUTION:

    ```java
    // import the ArrayList package here:
    import java.util.ArrayList;

    class ToDos {
    
        public static void main(String[] args) {
            
            // Create toDoList below:
            ArrayList<String> toDoList = new ArrayList<String>();

        }
    
    }
    ```