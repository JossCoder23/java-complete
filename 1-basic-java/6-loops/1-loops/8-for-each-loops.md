## For-Each Loops
Sometimes we need access to the elements’ indices or we only want to iterate through a portion of a list. If that’s the case, a regular ```for``` loop or ```while``` loop is a great choice.

For example, we can use a ```for``` loop to print out each element in an array called ```inventoryItems```:
```java
for (int inventoryItem = 0; inventoryItem < inventoryItems.length; inventoryItem++) {
    // Print element at current index
    System.out.println(inventoryItems[inventoryItem]);
}
```

But sometimes we couldn’t care less about the indices; we only care about the element itself.

At times like this, for-each ```loops``` come in handy.

*For-each loops*, which are also referred to as enhanced loops, allow us to directly loop through each item in a list of items (like an array or ```ArrayList```) and perform some action with each item.

If we want to use a for-each loop to rewrite our program above, the syntax looks like this:
```java
for (String inventoryItem : inventoryItems) {
    // Print element value
    System.out.println(inventoryItem);
}
```

Our enhanced loop contains two items: an enhanced ```for``` loop variable (```inventoryItem```) and a list to traverse through (```inventoryItems```).

We can read the : as “in” like this: for each ```inventoryItem``` (which should be a ```String```) in ```inventoryItems```, print ```inventoryItem```.

If we try to assign a new value to the enhanced ```for``` loop variable, the value stored in the array or ```ArrayList``` will not change. This is because, for every iteration in the enhanced loop, the loop variable is assigned a copy of the list element.

Note: We can name the enhanced ```for``` loop variable whatever we want; using the singular of a plural is just a convention. We may also encounter conventions like ```String word : sentence```.

**MostExpensive.java**
```java
import java.util.ArrayList;

class MostExpensive {
  
    public static void main(String[] args) {
        
        ArrayList<Double> expenses = new ArrayList<Double>();
        expenses.add(74.46);
        expenses.add(63.99);
        expenses.add(10.57);
        expenses.add(81.37);
        
        double mostExpensive = 0;
        
        // Iterate over expenses
        
        
        System.out.println(mostExpensive);
        
    }
  
}
```

EXERCISE:
1. Let’s use a for-each loop to find the priciest item in ```expenses```.

    Build a for-each loop that iterates through each ```expense``` in ```expenses```. For now, leave the body of the loop empty.

    **SOLUTION:**
    ```java
    import java.util.ArrayList;

    class MostExpensive {
        
        public static void main(String[] args) {
            
            ArrayList<Double> expenses = new ArrayList<Double>();
            expenses.add(74.46);
            expenses.add(63.99);
            expenses.add(10.57);
            expenses.add(81.37);
            
            double mostExpensive = 0;
            
            // Iterate over expenses
            for( double expense : expenses ) {}
            
            System.out.println(mostExpensive);
            
        }
    
    }
    ```

2. Inside the for-each loop, check if ```expense``` is greater than ```mostExpensive```.

    If it is, set ```mostExpensive``` equal to ```expense```.

    **SOLUTION:**
    ```java
    import java.util.ArrayList;

    class MostExpensive {
        
        public static void main(String[] args) {
            
            ArrayList<Double> expenses = new ArrayList<Double>();
            expenses.add(74.46);
            expenses.add(63.99);
            expenses.add(10.57);
            expenses.add(81.37);
            
            double mostExpensive = 0;
            
            // Iterate over expenses
            for( double expense : expenses ) {

                if( expense > mostExpensive ) {
                    mostExpensive = expense;
                }

            }
            
            System.out.println(mostExpensive);
            
        }
    
    }
    ```