## Bug Detective
Your friend built a program to mimic a fortune cookie by randomly printing a random fortune on each run. A fortune cookie is a crisp cookie with a piece of paper inside, on which is a “fortune.”

However, your friend didn’t use incremental development and debug along the way, so she ended up with a super buggy program. Can you be a bug detective and help her debug her program Fortune.java?

The output should look something like:

```git
Flattery will go far tonight.
```

Or:
```git
Don't behave with cold manners.
```

**Final tip**: If the compiler reports 100 error messages, that doesn’t mean there are 100 errors in the program. Sometimes when a compiler encounters an error, it often gets thrown off track. Only the first error message is truly reliable. Always scroll to the top and try to debug the very first error first.

Code review available when you’re done

==============================================

1. First, run the program to see the list of error messages.

    **SOLUTION:**

    ```java
    import java.lang.Math;

    class Fortune {

    public int generateRandom() {
        
        return (int)(Math.random() * 10);
        
    }

    public static void main(String[] args) {

        Fortune fortuneCookie = new Fortune();
        int fortune = fortuneCookie.generateRandom();
        
        if (fortune == 0) {

        System.out.println("Flattery will go far tonight.");
        
        } else if (fortune == 1) {
            
        System.out.println("Don't behave with cold manners.");
        
        } else if (fortune == 2) {
            
        System.out.println("May you someday be carbon neutral");
            
        } else if (fortune == 3) {
            
        System.out.println("You have rice in your teeth.");
            
        } else if (fortune == 4) {
            
        System.out.println("A conclusion is simply the place where you got tired of thinking.");
            
        } else if (fortune == 5) {
            
        System.out.println("No snowflake feels responsible in an avalanche.");
            
        } else if (fortune == 6) {
            
        System.out.println("He who laughs last is laughing at you.");
            
        } else if (fortune == 7) {
            
        System.out.println("If you look back, you'll soon be going that way.");
            
        } else if (fortune == 8) {
            
        System.out.println("You will live long enough to open many fortune cookies.");
            
        } else if (fortune == 9) {
            
        System.out.println("The fortune you seek is in another cookie.");
            
        }
        
    }
    
    }
    ```

2. Start from debugging from the first error (at the very top) until the program is bug-free.

    Make sure to use the line number in the error message to locate the bugs.

    **SOLUTION:**

    ```java
    /*Bug free*/

    import java.lang.Math;

    class Fortune {

    public int generateRandom() {
        
        return (int)(Math.random() * 10);
        
    }

    public static void main(String[] args) {

        Fortune fortuneCookie = new Fortune();
        int fortune = fortuneCookie.generateRandom();
        
        if (fortune == 0) {

        System.out.println("Flattery will go far tonight.");
        
        } else if (fortune == 1) {
            
        System.out.println("Don't behave with cold manners.");
        
        } else if (fortune == 2) {
            
        System.out.println("May you someday be carbon neutral");
            
        } else if (fortune == 3) {
            
        System.out.println("You have rice in your teeth.");
            
        } else if (fortune == 4) {
            
        System.out.println("A conclusion is simply the place where you got tired of thinking.");
            
        } else if (fortune == 5) {
            
        System.out.println("No snowflake feels responsible in an avalanche.");
            
        } else if (fortune == 6) {
            
        System.out.println("He who laughs last is laughing at you.");
            
        } else if (fortune == 7) {
            
        System.out.println("If you look back, you'll soon be going that way.");
            
        } else if (fortune == 8) {
            
        System.out.println("You will live long enough to open many fortune cookies.");
            
        } else if (fortune == 9) {
            
        System.out.println("The fortune you seek is in another cookie.");
            
        }
        
    }
    
    }
    ```