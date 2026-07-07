## Getting an Item's Index
What if we had a really large list and wanted to know the position of a certain element in it? For instance, what if we had an ```ArrayList detectives``` with the names of fictional detectives in chronological order, and we wanted to know what position ```"Fletcher"``` was.

```java
// detectives holds ["Holmes", "Poirot", "Marple", "Spade", "Fletcher", "Conan", "Ramotswe"];
System.out.println(detectives.indexOf("Fletcher"));
```

This code would print ```4```, since ```"Fletcher"``` is at index ```4``` of the ```detectives ArrayList```.

EXERCISE:
1. After visiting the crime scene, the ever-impatient Dr. Watson wants to know how many to-dos are left until Sherlock solves the case.

    To help Dr. Watson figure this out, use ```indexOf()``` to determine where in the to-do list ```"solve the case"``` is.

    Print this information out. That’s the number of to-dos remaining before Sherlock reaches ```"solve the case"```.

    SOLUTION:

    ```java
    import java.util.ArrayList;

    class ToDos {
        
        public static void main(String[] args) {
            
            // Sherlock
            ArrayList<String> sherlocksToDos = new ArrayList<String>();
            
            sherlocksToDos.add("visit the crime scene");
            sherlocksToDos.add("play violin");
            sherlocksToDos.add("interview suspects");
            sherlocksToDos.add("listen to Dr. Watson for amusement");
            sherlocksToDos.add("solve the case");
            sherlocksToDos.add("apprehend the criminal");
            
            sherlocksToDos.remove("visit the crime scene");
            
            // Calculate to-dos until case is solved:
            System.out.println(sherlocksToDos.indexOf("solve the case"));
            
            // Change the value printed:
            System.out.println("PRINT THE ANSWER HERE");

        }
    
    }
    ```

    OUTPUT:
    ```git
    3
    PRINT THE ANSWER HERE
    ```