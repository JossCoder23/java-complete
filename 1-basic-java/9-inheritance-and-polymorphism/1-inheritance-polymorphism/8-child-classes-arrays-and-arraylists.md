## Child Classes in Arrays and ArrayLists
Usually, when we create an array or an ```ArrayList```, the list items all need to be the same type. But polymorphism puts a new spin on what is considered the same type…

In fact, we can put instances of different ```classes``` that share a parent class together in an array or ```ArrayList```! For example, let’s say we have a ```Monster``` parent class with a few child classes: ```Vampire```, ```Werewolf```, and ```Zombie```. We can set up an array with instances of each:

```java
Monster dracula, wolfman, zombie1;

dracula = new Vampire();
wolfman = new Werewolf();
zombie1 = new Zombie();

Monster[] monsters = {dracula, wolfman, zombie1};
```

We can even iterate through the list of items — regardless of subclass — and perform the same action with each item:
```java
for (Monster monster : monsters) {
  monster.attack();
}
```

In the code above, we were able to call ```attack()``` on each monster in ```monsters``` despite the fact that, in the for-each loop, ```monster``` is declared as the parent class type ```Monster```.

**ARCHIVES:**

**Noodle.js**
```java
class Noodle {

    protected double lengthInCentimeters;
    protected double widthInCentimeters;
    protected String shape;
    protected String ingredients;
    protected String texture = "brittle";
    
    Noodle(double lenInCent, double wthInCent, String shp, String ingr) {
        
        this.lengthInCentimeters = lenInCent;
        this.widthInCentimeters = wthInCent;
        this.shape = shp;
        this.ingredients = ingr;
        
    }
    
    public String getCookPrep() {
        return "Boil noodle for 7 minutes and add sauce.";
    }

}
```

**Spaghetti.java**
```java
class Spaghetti extends Noodle {

    Spaghetti() {
        super(30.0, 0.2, "round", "semolina flour");
    }
    
    @Override
    public String getCookPrep() {
        return "Boil spaghetti for 8 - 12 minutes and add sauce, cheese, or oil and garlic.";
    }

}
```

**Ramen.java**
```java
class Ramen extends Noodle {

    Ramen() {
        super(30.0, 0.3, "flat", "wheat flour");
    }
    
    @Override
    public String getCookPrep() {
        return "Boil ramen for 5 minutes in broth, then add meat, mushrooms, egg, and vegetables.";
    }

}
```

**Pho.java**
```java
class Pho extends Noodle {

    Pho() {
        super(30.0, 0.64, "flat", "rice flour");
    }
    
    @Override
    public String getCookPrep() {
        return "Soak pho for 1 hour, then boil for 1 minute in broth. Then garnish with cilantro and jalapeno.";
    }

}
```

**Main.java**
```java
public class Main {
    public static void main(String[] args) {
        Noodle spaghetti, ramen, pho;
        
        spaghetti = new Spaghetti();
        ramen = new Ramen();
        pho = new Pho();
            
        // Add your code below:
        
    }
}
```

**EXERCISE:**
1. Look at the code editor. We have ```Noodle``` as a parent class and it has three child classes: ```Pho```, ```Ramen```, and ```Spaghetti```.

    Inside the ```main()``` method of **Main.java**, declare an array of type ```Noodle``` called ```allTheNoodles``` and initialize it with the following items: ```spaghetti```, ```ramen```, ```pho``` in that order.

    **SOLUTION:**

    **Main.java**
    ```java
    public class Main {
        public static void main(String[] args) {
            Noodle spaghetti, ramen, pho;
            
            spaghetti = new Spaghetti();
            ramen = new Ramen();
            pho = new Pho();
                
            // Add your code below:
            Noodle[] allTheNoodles = {spaghetti, ramen, pho};   

        }
    }
    ```

2. Use the ```for-each``` loop to traverse through each noodle in ```allTheNoodles```.

    Inside the ```for-each``` loop, call the ```getCookPrep()``` method on each noodle and print the result.

    *Note: you must use a for-each loop and not a regular for loop for this exercise!*

    **SOLUTION:**

    **Main.java**
    ```java
    public class Main {
        public static void main(String[] args) {
            Noodle spaghetti, ramen, pho;
            
            spaghetti = new Spaghetti();
            ramen = new Ramen();
            pho = new Pho();
                
            // Add your code below:
            Noodle[] allTheNoodles = {spaghetti, ramen, pho};   
            for( Noodle noodle : allTheNoodles ) {
                System.out.println(noodle.getCookPrep());
            }

        }
    }
    ```

    OUTPUT:
    ```git
    Boil spaghetti for 8 - 12 minutes and add sauce, cheese, or oil and garlic.
    Boil ramen for 5 minutes in broth, then add meat, mushrooms, egg, and vegetables.
    Soak pho for 1 hour, then boil for 1 minute in broth. Then garnish with cilantro and jalapeno.
    ```