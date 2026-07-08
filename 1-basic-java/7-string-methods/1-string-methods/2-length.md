## length()
In Java, the ```length()``` string method returns the length ⁠— total number of characters ⁠— of a ```String```.

Suppose we have a ```String``` called ```str```, ```str.length()``` would return its length.

Take a look at this code for example:
```java
String str = "Hello World!";  
System.out.println(str.length());
```

```12``` would be printed because ```str``` has 12 characters:

```H e l l o _ W o r l d !```

In theory, the length of a ```String``` is the same as the ```Unicode``` units of the ```String```. For example, escape sequences such as ```\n``` count as only one character.

**TweetCounter.java**
```java
public class TweetCounter {
  
	public static void main(String[] args) {
    
        String tweet = "Liz Lemon, ninjas are kind of cool... I just dont know any personally. Get on that.";  

        // What's the character count?
        
    }
    
}
```

EXERCISE:
1. Twitter allows users to post tweets with a character limit. They capture the message the user enters as a ```String```, count the length of the message, and use its length to decide whether or not to let the user post the message. The limit is 280 characters.

    Let’s check if ```tweet``` follows Twitter’s policy. Print out the number of characters in ```tweet``` using the ```length()``` method.

    **SOLUTION:**
    ```java
    public class TweetCounter {
    
        public static void main(String[] args) {
            
            String tweet = "Liz Lemon, ninjas are kind of cool... I just dont know any personally. Get on that.";  

            // What's the character count?
            System.out.println(tweet.length());
            
        }
        
    }
    ```