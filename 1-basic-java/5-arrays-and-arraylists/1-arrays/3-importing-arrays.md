## Importing Arrays
When we printed out the array we created in the last exercise, we saw a memory address that did not help us understand what was contained in the array.

If we want to have a more descriptive printout of the array itself, we need a ```toString()``` method that is provided by the ```Arrays``` package in Java.
```java
import java.util.Arrays;
```

We put this at the top of the file, before we even define the class!

When we import a package in Java, we are making all of the methods of that package available in our code.

The ```Arrays``` package has many useful methods, including ```Arrays.toString()```. When we pass an array into ```Arrays.toString()```, we can see the contents of the array printed out:
```java
import java.util.Arrays;

public class Lottery(){
  
    public static void main(String[] args){
        int[] lotteryNumbers = {4, 8, 15, 16, 23, 42};
        String betterPrintout = Arrays.toString(lotteryNumbers);
        System.out.println(betterPrintout);
    }

}
```

This code will print:
```git
[4, 8, 15, 16, 23, 42]
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

**Main.java**
```java
// import the Arrays package here

public class Main {
    public static void main(String[] args) {
        Newsfeed sampleFeed = new Newsfeed();
        String[] topics = sampleFeed.getTopics();
        System.out.println(topics);
    }
}
```

EXERCISE:
1. If you run the code now, You’ll see something like this: ```[Ljava.lang.String;@2aae9190```.

    This is the memory address of the array and not the actual ```String``` array.

    To make the code print the actual elements, use the ```toString()``` method from the ```Arrays``` package.

    Import the ```Arrays``` package from ```java.util``` at the top of the **Main.java** file.

    SOLUTION:

    **Main.java**

    ```java
    // import the Arrays package here
    import java.util.Arrays;

    public class Main {
        public static void main(String[] args) {
            Newsfeed sampleFeed = new Newsfeed();
            String[] topics = sampleFeed.getTopics();
            System.out.println(topics);
        }
    }
    ```

2. Now, use the ```toString()``` method from the ```Arrays``` package to print array ```topics``` in the ```main()``` method of Main.java.

    SOLUTION:

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

    OUTPUT:
    ```git
    [Opinion, Tech, Science, Health]
    ```