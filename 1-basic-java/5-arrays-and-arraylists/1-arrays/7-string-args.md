## String[] args
When we write ```main() methods``` for our programs, we use the parameter ```String[] args```. Now that we know about array syntax, we can start to parse what this means.

A ```String[]``` is an array made up of ```String```s. Examples of ```String``` arrays:
```java
String[] humans = {"Talesha", "Gareth", "Cassie", "Alex"};
String[] robots = {"R2D2", "Marvin", "Bender", "Ava"};
```

The ```args``` parameter is another example of a ```String``` array. In this case, the array ```args``` contains the arguments that we pass in from the terminal when we run the class file. (So far, ```args``` has been empty.)

So how can you pass arguments to ```main()```? Let’s say we have this class ```HelloYou```:
```java
public class HelloYou {
    public static void main(String[] args) {
        System.out.println("Hello " + args[0]);  
    }
}
```

When we run the file ```HelloYou``` in the terminal with an argument of ```"Laura"```:
```git
java HelloYou Laura
```

We get the output:
```git
Hello Laura
```

The ```String[] args```would be interpreted as an array with one element, ```"Laura"```.

When we use ```args[0]``` in the main method, we can access that element like we did in ```HelloYou```.

EXERCISE:
1. Let’s make users have the option to personalize the Newsfeed object for either robots or humans.

    The ```main()``` in Main.java will take either “Robot” or “Human” as an argument when we run the file.

    If the ```args[0]``` array holds “Human”, we will initialize the feed with human topics.

    If the ```args[0]``` array holds “Robot”, we will initialize the feed with robot topics.

    In the conditional statement on line 6, Replace the blank to check if the ```args``` has the value ```Robot``` or not.

    SOLUTION:

    **Main.java**

    ```java
    import java.util.Arrays;

    public class Main{
        public static void main(String[] args){
            
            Newsfeed feed;
            
            if(args[0].equals("Robot")){
                //topics for a Robot feed:
                String[] robotTopics = {"Oil", "Parts", "Algorithms", "Love"};
                feed = new Newsfeed(robotTopics);
            }
            else if(args[0].equals("Human")){
                //topics for a Human feed:
                String[] humanTopics = {"Politics", "Science", "Sports", "Love"};
                        feed = new Newsfeed(humanTopics);
            }
            else{
                String[] genericTopics = {"Opinion", "Tech", "Science", "Health"};
                feed = new Newsfeed(genericTopics);
            }
                
            System.out.println("The topics in this feed are:");
            System.out.println(Arrays.toString(feed.topics));
        }
    }
    ```

2. In the terminal, run the Main.java with the argument ```Robot```.

    *Note: Do not use quotation marks for the argument. Passing in “Robot” as an argument will not work.*

    SOLUTION:

    ```cmd
    java Main Robot
    The topics in this feed ars:
    [Oil, Parts, Algorithms, Love]
    ```

3. Now, run the Main.java file with the argument ```Human```.

    *Note: Do not use quotation marks for the argument. Passing in “Human” as an argument will not work.*

    SOLUTION:

    ```git
    java Main Human
    The topics in this feed ars:
    [Politics, Science, Sports, Love]
    ```