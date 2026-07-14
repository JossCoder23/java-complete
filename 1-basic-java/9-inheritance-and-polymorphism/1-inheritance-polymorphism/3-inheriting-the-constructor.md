## Inheriting the Constructor
Hang on, you might be thinking, if the child class inherits its parent’s fields and ```methods```, does it also inherit the constructor? Let’s take a look at how the ```super()``` constructor works!

Let’s say ```Shape``` has a ```numSides``` field that is set by passing an integer into the constructor. If we’re instantiating a ```Triangle```, we would want that number to always be ```3```, so we’d want to modify the constructor to automatically assign ```numSides``` with a value of ```3```.

Can we do that?

As it happens, Java has a trick up its sleeve for just this occasion: using the ```super()``` method which acts like the parent constructor inside the child class constructor: 

```java
class Triangle extends Shape {

  Triangle() {
    super(3);
  }

  // additional Triangle class members

}
```

By passing ```3``` to ```super()```, we are making it possible to instantiate a ```Triangle``` without passing in a value for ```numSides```.

Meanwhile, ```super(3)``` (behaving as ```Shape(3)```) will shoulder the responsibility of setting ```numSides``` to ```3``` for our ```Triangle``` object. It’s like we called ```Shape(3)```.

It is also possible to write a constructor without making a call to any ```super()``` constructor:

```java
class Triangle extends Shape {

  Triangle() {
    this.numSides = 3;
  }

  // additional Triangle class methods

}
```

In this situation, Java secretly calls the parent class’ no-argument constructor (```super()```). So in this specific example, the ```Triangle()``` constructor first calls the ```Shape()``` constructor. That ```Shape()``` takes care of whatever business it needs to take care of. And then after that is complete, we go in and set ```this.numSides``` to ```3```.

If you’re writing a constructor of a child class, and don’t explicitly make a call to a constructor from a parent class using ```super```, it’s important to remember that Java will automatically (and secretly) call ```super()``` as the first line of your child class constructor.

**Pho.java**
```java
class Pho extends Noodle {
    public Pho(){
        
    }
}
```

**Noodle.java**
```java
class Noodle {

    double lengthInCentimeters;
    double widthInCentimeters;
    String shape;
    String ingredients;
    String texture = "brittle";
        
    Noodle(double lenInCent, double wthInCent, String shp, String ingr) {
        
        this.lengthInCentimeters = lenInCent;
        this.widthInCentimeters = wthInCent;
        this.shape = shp;
        this.ingredients = ingr;
        
    }
        
    public void cook() {
        this.texture = "cooked";
    }
    
}
```

**Main.java**
```java
public class Main{
    public static void main(String[] args) {
        
    }
}
```

EXERCISE:
1. Let’s use the constructor of the parent class of the ```Pho``` class.

    Inside the constructor ```Pho()```, use ```super()``` to access the constructor of the ```Noodle``` class and pass in these arguments in the following order:

    * ```30.0``` as the value of ```lengthInCentimeters```
    * ```0.64``` as ```widthInCentimeters```
    * “flat” as the ```shape```
    * “rice flour” as the ```ingredients```

    **SOLUTION:**

    **Pho.java**
    ```java
    class Pho extends Noodle {
        public Pho(){
            super(30.0, 0.64, "flat", "rice flour");
        }
    }
    ```

2. Inside ```main()``` of Main.java, create a new object of the ```Pho``` class called ```phoChay```.

    **SOLUTION:**

    **Main.java**
    ```java
    public class Main{
        public static void main(String[] args) {
            Pho phoChay = new Pho();
        }
    }
    ```

3. Now print out the ```phoChay``` instance’s ```shape``` field.

    **SOLUTION:**

    **Main.java**
    ```java
    public class Main{
        public static void main(String[] args) {
            Pho phoChay = new Pho();
            System.out.println(phoChay.shape);
        }
    }
    ```

    OUTPUT:
    ```java
    flat
    ```