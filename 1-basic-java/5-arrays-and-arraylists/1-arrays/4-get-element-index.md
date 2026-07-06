## Get Element By Index
Now that we have an array declared and initialized, we want to be able to get values out of it.

We use square brackets, ```[``` and ```]```, to access data at a certain index:
```java
double[] prices = {13.1, 15.87, 14.22, 16.66};
System.out.println(prices[1]);
```

This command would print:
```git
15.87
```

This happens because ```15.87``` is the item at the ```1``` index of the array. Remember, the index of an array starts at ```0``` and ends at an index of one less than the number of elements in the array.

If we try to access an element outside of its appropriate index range, we will receive an ```ArrayIndexOutOfBoundsException``` error.

For example, if we were to run the command ```System.out.println(prices[5])```, we’d get the following output:
```git
java.lang.ArrayIndexOutOfBoundsException: 5
```

**Main.java**

```java
// import the Arrays package here
import java.util.Arrays;

public class Main {
    public static void main(String[] args) {
        Newsfeed sampleFeed = new Newsfeed();
        String[] topics = sampleFeed.getTopics();
        System.out.println(Arrays.toString(topics));
    }
}
```

**Newsfeed.java**
```java
public class Newsfeed {
    public Newsfeed(){
        
    }
        
    public String[] getTopics(){
        String[] topics = {"Opinion", "Tech", "Science", "Health"};
        return topics;
    }
}
```

EXERCISE:
1. Inside the ```Newsfeed``` class, create a method called ```getFirstTopic()``` that returns a ```String``` and accepts no parameters.

    Inside the ```getFirstTopic()``` method, return the first element of the ```topics``` array.

    SOLUTION:

    **Newsfeed.java**

    ```java
    public class Newsfeed {
        String[] topics = {"Opinion", "Tech", "Science", "Health"};
        public int[] views = {0, 0, 0, 0};
        
        public Newsfeed(){

        }
            
        public String[] getTopics(){
            return topics;
        }
        
        // Create getFirstTopic() below
        public String getFirstTopic() {
            return topics[0];
        }
        
        public void viewTopic(int topicIndex){
            
        }
    }
    ```

2. We have added an array called ```views``` to keep track of how many viewers visit a topic.

    Every time someone views a topic, we want to increase the value of the corresponding element in ```views``` by 1.

    For example, if someone views an “Opinion” piece (index of 0 in topics), we will increase the value of the 0th index of ```views``` by 1.

    Inside the ```viewTopic()``` method, implement this functionality. The parameter ```topicIndex``` represents the location of the element in ```topics``` that was viewed.

    *Note: switch over to the Main.java file to see the output of the program you wrote.*

    SOLUTION:

    **Newsfeed.java**

    ```java
    public class Newsfeed {
        String[] topics = {"Opinion", "Tech", "Science", "Health"};
        public int[] views = {0, 0, 0, 0};
        
        public Newsfeed(){

        }
            
        public String[] getTopics(){
            return topics;
        }
        
        // Create getFirstTopic() below
        public String getFirstTopic() {
            return topics[0];
        }
        
        public void viewTopic(int topicIndex){
            views[topicIndex] = views[topicIndex] + 1;
        }
    }
    ```