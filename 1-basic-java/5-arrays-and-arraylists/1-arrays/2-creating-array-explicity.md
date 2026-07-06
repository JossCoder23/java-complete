## Creating an Array Explicitly
Imagine that we’re using a program to keep track of the prices of different clothing items we want to buy. We would want a list of the prices and a list of the items they correspond to. To create an array, we provide a name and declare the type of data it holds:
```java
double[] prices;
```

Just like with variables, we can declare and initialize in the same line. This allows us to explicitly initialize the array to contain the data we want to store:
```java
double[] prices = {13.15, 15.87, 14.22, 16.66};
```

We can use arrays to hold ```String```s and other objects as well as primitives:
```java
String[] clothingItems = {"Tank Top", "Beanie", "Funny Socks", "Corduroys"};
```

**Newfeed.java**
```java
public class Newsfeed {
    public Newsfeed(){
        
    }
    // Create getTopics() below:
    
}
```

**Main.java**
```java
public class Main {
    public static void main(String[] args) {
        Newsfeed sampleFeed = new Newsfeed();
        String[] topics = sampleFeed.getTopics();
        System.out.println(topics);
    }
}
```

EXERCISE:
1. For now, our ```Newsfeed``` class doesn’t have any methods.

    Create a method ```getTopics()``` that accepts no parameters, returns a ```String``` array, and is accessible by other classes.

    Leave the body empty.

    *Note: it is okay for there to be an error claiming there is no main() method. This method is defined in Main.java.*

    SOLUTION:

    **Newsfeed.java**

    ```java
    public class Newsfeed {
        public Newsfeed(){
            
        }
        // Create getTopics() below:
        public String[] getTopics() {
            
        }
        
    }
    ```


2. Inside the ```getTopics()``` method, create a ```String``` array called topics that contains these elements:

    ```git
    "Opinion", "Tech", "Science", "Health" 
    ```

    Remember to keep the order the same.

    Then, return the ```topics``` array at the end of the method!

    To see the output of the program, switch over to the Main.java file and click “Run”.

    SOLUTION:

    **Newsfeed.java**

    ```java
   public class Newsfeed {
        public Newsfeed(){
            
        }
        // Create getTopics() below:
        public String[] getTopics() {
            String[] topics = {"Opinion", "Tech", "Science", "Health"};
            return topics;
        }
        
    }
    ```

    OUTPUT:
    ```git
    [Ljava.lang.String;@7ad041f3
    ```