## equals()

With objects, such as ```String```s, we can’t use the primitive equality operator ```==``` to check for equality between two strings. To test equality with strings, we use a built-in method called ```equals()```

For example:
```java
String flavor1 = "Mango";
String flavor2 = "Peach";

System.out.println(flavor1.equals("Mango"));
// prints true

System.out.println(flavor2.equals("Mango"));
// prints false
```

Side note, there’s also an ```equalsIgnoreCase()``` method that compares two strings without considering upper/lower cases.

### Keep Reading: AP Computer Science A Students
We can also compare ```String``` values lexicographically (think dictionary order) using the ```compareTo()``` method. When we call the ```.compareTo()``` method, each character in the ```String``` is converted to Unicode; then the Unicode character from each ```String``` is compared.

The method will return an ```int``` that represents the difference between the two Strings.

For example:
```java
String flavor1 = "Mango";
String flavor2 = "Peach";

System.out.println(flavor1.compareTo(flavor2)); 
```

Our program above will output ```-3```.

When we use ```.compareTo()```, we must pay attention to the return value:
* If the method returns ```0```, the two ```String```s are equal.
* If the value is less than ```0```, then the ```String``` object is lexicographically less than the ```String``` object argument.
* If the value is greater than ```0```, then the ```String``` object is lexicographically greater than the ```String``` object argument.

In the example above, ```"Mango"``` comes before ```"Peach"```, so we get a negative number (we specifically get ```-3``` because the Unicode values of ```"M"``` and ```"P"``` differ by 3). If we did ```flavor2.compareTo(flavor1)```, we would get ```3```, signifying that ```"Peach"``` is greater than ```"Mango"```.

**Note:** Make sure to pay attention to capitalization when using ```.compareTo()```. Upper case and lower case letters have different Unicode values. For example, when comparing ```"Mango"``` and ```"Peach"```, we got ```-3```, meaning that ```"Mango"``` was smaller. But if we compare ```"mango"``` and ```"Peach"``` we get ```29```. The Unicode value for lower case ```"m"``` is actually larger than upper case ```"P"```. Using ```.compareToIgnoreCase()``` will perform the same task, but will not consider upper/lower case.

**Password.java**
```java
public class Password {
  
    public static void main(String[] args) {
        
        String password = "correcthorsebatterystaple";
        
        // Write the code:
        
        
    }
  
}
```

EXERCISE:
1. In **Password.java**, there’s a ```password``` with a value of ```"correcthorsebatterystaple"```.

    Use ```equals()``` to print out whether it’s the same as another string.

    **SOLUTION:**
    ```java
    public class Password {
  
        public static void main(String[] args) {
            
            String password = "correcthorsebatterystaple";
            
            // Write the code:
            System.out.println(password.equals("HolaMundo"));
            
        }
    
    }
    ```