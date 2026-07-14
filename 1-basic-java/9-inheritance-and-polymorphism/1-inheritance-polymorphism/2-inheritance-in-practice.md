## Inheritance in Practice
So how do we define a child class so that it inherits from a parent class? We use the keyword ```extends``` like this:

```java
class Shape {
  // Shape class members
}

class Triangle extends Shape {
  // additional Triangle class members
}
```

Now ```Triangle``` has inherited traits from ```Shape```, meaning it copied over class members from ```Shape```. When we use ```inheritance``` to extend a subclass from a superclass, we create an “is-a” relationship from the subclass to the superclass. For example, an object of ```Triangle``` is a member of the ```Shape``` class; however, an object of ```Shape``` is not necessarily an object of ```Triangle```.

Until now, we’ve only been working with one class and one file. However, most Java programs utilize multiple ```classes```, each of which requires its own file. Only one file needs a ```main()``` method — this is the file we will run.

Note: the various classes in our Java package — even though they are in different ```files``` — will have access to each other, so we can instantiate one class inside of another.

**Noodle.java**
```java
class Noodle {

    double lengthInCentimeters;
    String shape;
    String texture = "brittle";
    
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
1. We’ve provided two files:
    
    * **Noodle.java**: This will be our parent class.
    * **Spaghetti.java**: This will be our child class.

    Notice that the parent class Noodle.java already has some instance fields and methods:

    * The ```lengthInCentimeters``` field.
    * The ```shape``` field.
    * The ```texture``` field.
    * A ```cook()``` method.

    Let’s create a child class. In the **Spaghetti.java** file, create a class called ```Spaghetti``` and make it a child class of the ```Noodle``` class.

    Run the **Noodle.java** file.

    **SOLUTION:**

    **Spaghetti.java**
    ```java
    class Spaghetti extends Noodle {

    }
    ```

2. Inside ```main()``` of **Main.java**, create a new instance of the ```Spaghetti``` class and name it ```spaghettiPomodoro```.

    Print out the ```texture``` field of the instance ```spaghettiPomodoro``` to the terminal.

    **SOLUTION:**

    **Main.java**
    ```java
    public class Main{
        public static void main(String[] args) {
            Spaghetti spaghettiPomodoro = new Spaghetti();
            System.out.println(spaghettiPomodoro.texture);
        }
    }
    ```