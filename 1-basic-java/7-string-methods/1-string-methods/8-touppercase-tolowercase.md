## toUpperCase() / toLowerCase()
There will be times when we have a word in a case other than what we need it in. Luckily, Java has a couple String methods to help us out:
* toUpperCase(): returns the string value converted to uppercase
* toLowerCase(): returns the string value converted to lowercase

For example:
```java
String input = "Cricket!";

String upper = input.toUpperCase();
// stores "CRICKET!"

String lower = input.toLowerCase();
// stores "cricket!"
```

A good use of this functionality is to ensure consistency of the data you store in a database. Making sure all of the data you get from a user is lowercase before you store it in your database will make your database easier to search through later.

**HashTag.java**
```java
public class Hashtag {
  
    public static void main(String[] args) {
        
        String hashtag = "#100DaysOfCode";
        
        // Make the hashtag lowercase:
        
        
    }
  
}
```

EXERCISE:
1. In Hashtag.java, use ```toLowerCase()``` to print out the lower case version of ```hashtag```.

    **SOLUTION:**
    ```java
    public class Hashtag {
  
        public static void main(String[] args) {
            
            String hashtag = "#100DaysOfCode";
            
            // Make the hashtag lowercase:
            System.out.println(hashtag.toLowerCase());
            
        }
        
    }
    ```

    OUTPUT:
    ```git
    #100daysofcode
    ```