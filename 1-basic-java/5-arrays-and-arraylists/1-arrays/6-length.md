## Length
What if we have an array storing all the usernames for our program, and we want to quickly see how many users we have? To get the length of an array, we can access the ```length``` field of the array object:
```java
String[] menuItems = new String[5];
System.out.println(menuItems.length);
```

This command would print ```5```, since the ```menuItems``` array has 5 slots, even though they are all empty.

If we print out the length of the ```prices``` array:
```java
double[] prices = {13.1, 15.87, 14.22, 16.66};
System.out.println(prices.length);
```

We would see ```4```, since there are four items in the ```prices``` array!

**Newsfeed.java**
```java
public class Newsfeed {

    String[] topics = {"Opinion", "Tech", "Science", "Health"};
    int[] views = {0, 0, 0, 0};
    
    public Newsfeed(){

    }
        
    public String[] getTopics(){
        return topics;
    }
    
    public int getNumTopics(){
        
    }
  
}
```

**Main.java**
```java
import java.util.Arrays;

public class Main {
    public static void main(String[] args){
        Newsfeed sampleFeed = new Newsfeed();
        System.out.println("The number of topics is "+ sampleFeed.getNumTopics());
    }
}
```

EXERCISE:
1. We have created a method ```getNumTopics()``` to fetch how many topics exist in the array.

    Inside ```getNumTopics()```, return the length of the ```topics``` array.

    SOLUTION:

    **Newsfeed.java**
    ```java
    public class Newsfeed {
        String[] topics = {"Opinion", "Tech", "Science", "Health"};
        int[] views = {0, 0, 0, 0};
        
        public Newsfeed(){

        }
            
        public String[] getTopics(){
            return topics;
        }
        
        public int getNumTopics(){
            return topics.length;
        }
        
    }
    ```

    OUTPUT:
    ```git
    The number of topics is 4
    ```