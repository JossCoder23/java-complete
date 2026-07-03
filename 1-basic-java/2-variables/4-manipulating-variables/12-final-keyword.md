## final Keyword
Throughout this lesson, we’ve discussed the different ways we can manipulate a variable; however, what do we do with a variable that should never change its value?

For example, the year we were born will always stay the same. There’s no way we can change that information. A value like this in our code should be unchangeable.

To declare a variable with a value that cannot be manipulated, we need to use the ```final``` keyword. To use the ```final``` keyword, prepend ```final``` to a variable declaration like so:
```java
final int yearBorn = 1968;
```

When we declare a variable using ```final```, the value cannot be changed; any attempts at doing so will cause an error to occur:
```git
error: cannot assign a value to final variable yearBorn
```

EXERCISE:
1. Create an unchangeable ```double``` variable called ```pi``` and set its value to ```3.14```.

    Print the value of ```pi```.

2. On a new line, try to change the value of ```pi```.

    What happens when the program is run?

    **Final.java**
    ```java
    public class Final {
        public static void main(String[] args) { 
        
            
        }
    }
    ```

SOLUTION - ONE:
```java
public class Final {
	public static void main(String[] args) { 
      final double pi = 3.14;
      System.out.println(pi);
	}
}
```

OUTPUT:
```git
3.14
```

SOLUTION - TWO: (witing error)
```java
public class Final {
	public static void main(String[] args) { 
      final double pi = 3.14;
      System.out.println(pi);

      pi = 4.14;
	}
}
```

OUTPUT:
```git
Final.java:6: error: cannot assign a value to final variable pi
      pi = 4.14;
      ^
1 error
```