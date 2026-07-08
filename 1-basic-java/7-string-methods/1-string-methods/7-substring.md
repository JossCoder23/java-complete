## substring()
There may be times when we only want a part of a string. In such cases, we may want to extract a substring from a string.

The substring() method does exactly that. For example:
```java
String line = "The Heav'ns and all the Constellations rung";

System.out.println(line.substring(24));
```

It would output Constellations rung because that’s what begins at index 24 and ends at the end of line. The substring begins with the character at the specified index and extends to the end of the string.

Suppose we want a substring from the middle of the string. We can instead include two arguments in this method. For example:
```java
String line = "The Heav'ns and all the Constellations rung";

System.out.println(line.substring(27, 33));
```

When substring() is called with two arguments, the first argument is inclusive and the second is exclusive. This means the resulting substring will begin at index 27 and extend up to, but not including, index 33. Therefore, the example above would output stella because that’s the substring that begins at index 27 and ends at index 32, one index before 33.

We can use this method to return a single-element substring at a specific index. We do this by calling substring() with the desired index value as the first argument and then the index value plus one as the second argument.

For example, we can use this method to output just C:
```java
String line = "The Heav'ns and all the Constellations rung";

System.out.println(line.substring(24, 25));
// Prints: C
```

**Poetry.java**
```java
public class Poetry {
  
	public static void main(String[] args) {
      
        String line = "The Heav'ns and all the Constellations rung";     
        // Change the arguments:
        System.out.println(line.substring(23, 38));
        
    }
  
}
```

EXERCISE:
1. Change the arguments of the ```line.substring()``` method so that it prints out ```Heav'ns``` instead.

    **SOLUTION:**
    ```java
    public class Poetry {
  
        public static void main(String[] args) {
            
            String line = "The Heav'ns and all the Constellations rung";     
            // Change the arguments:
            System.out.println(line.substring(4, 11));
            
        }
        
    }
    ```