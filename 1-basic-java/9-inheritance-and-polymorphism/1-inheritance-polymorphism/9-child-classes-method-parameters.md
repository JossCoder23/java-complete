## Child Classes in Method Parameters
When we call a method that contains parameters, the arguments we place in our method call must match the parameter type. Similar to the previous exercise, polymorphism gives us a little more flexibility with the arguments we can use.

If we use a superclass reference as a method parameter, we can call the method using subclass reference arguments!

For example, imagine the class ```ScaryStory```, whose constructor takes in a reference to the ```Monster``` class:

```java
class ScaryStory {
    Monster monster;
    String setting;

    public ScaryStory(Monster antagonist, String place) {
        monster = antagonist;
        setting = place;
    }

    public void tellStory(){
        System.out.println("Once upon a time, " + monster.name + " was at " + setting + " looking to scare some mortals.");
    }

    public static void main(String[] args) {
        Monster dracula;
        dracula = new Vampire("Dracula");
        ScaryStory countDracula = new ScaryStory(dracula, "Dracula Castle");
        countDracula.tellStory();
    }
}
```

In the ```main()``` method, we used a reference of the class ```Vampire``` as our argument even though the constructor requested an object of class ```Monster```. This is allowed because ```Vampire``` is a subclass of the ```Monster``` class.

**ARCHIVES:**

**Main.ja**
```java
public class Main{
    public static void main(String[] args) {
        Noodle ramen, pho;
        ramen = new Ramen();
        pho = new Pho();
        
        NoodleRestaurant customer1 = new NoodleRestaurant("Sagirah");
    
        // Add your code here
    
    }
}
```

**EXERCISE:**

1. Look at the new file called Main.java. There is an instance of ```NoodleRestaurant``` called ```customer1```. The class ```NoodleRestaurant``` has a method called ```order()``` that takes in an object of type ```Noodle``` as a parameter.

    We instantiated ```Ramen``` and ```Pho``` as ```Noodle``` in the ```main()``` method.

    Inside the ```main()``` method, call the ```order()``` method of the ```customer1``` instance and pass in the ```pho``` instance as an argument.

    **SOLUTION:**

    **Main.java**
    ```java
    public class Main{
        public static void main(String[] args) {
            Noodle ramen, pho;
            ramen = new Ramen();
            pho = new Pho();
            
            NoodleRestaurant customer1 = new NoodleRestaurant("Sagirah");
        
            // Add your code here
            customer1.order(pho);
        }
    }
    ```

    OUTPUT:
    ```git
    Soak pho for 1 hour, then boil for 1 minute in broth. Then garnish with cilantro and jalapeno.
    Order for Sagirah is ready.
    ```