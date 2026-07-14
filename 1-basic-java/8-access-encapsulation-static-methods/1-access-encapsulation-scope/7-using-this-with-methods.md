## Using this With Methods
We’ve seen how the this works with variables, but we can also use the this with methods.

Recall how we’ve been calling methods up to this point:

```java
public static void main(String[] args){
    Dog myDog = new Dog("Odie");
    myDog.speak();
}
```

Here we’re creating an instance of a ```Dog``` and using that ```Dog``` to call the ```speak()``` method. However, when defining methods, we can also use the ```this``` keyword to call other methods. Consider the code block below:

```java
public class Computer{
    public int brightness;
    public int volume;
    
    public void setBrightness(int inputBrightness){
        this.brightness = inputBrightness;
    }

    public void setVolume(int inputVolume){
        this.volume = inputVolume;
    }

    public void resetSettings(){
        this.setBrightness(0);
        this.setVolume(0);
    }
}
```

Take a look at the ```resetSettings()``` method in particular. This method calls other methods from the class. But it needs an object to call those methods! Rather than create a new object (like we did with the ```Dog``` named ```myDog``` earlier), we use ```this``` as the object. What this means is that the object that calls ```resetSettings()``` will be used to call ```setBrightness(0)``` and ```setVolume(0)```.

```java
public static void main(String[] args){
    Computer myComputer = new Computer();
    myComputer.resetSettings();
}
```

In this example, calling ```myComputer.resetSettings()``` is as if we called ```myComputer.setBrightness(0)``` and ```myComputer.setVolume(0)```. this serves as a placeholder for whatever object was used to call the original method.

### Keep Reading: AP Computer Science A Students
Finally, ```this``` can be used as a value for a parameter. Let’s say a method exists that takes a ```Computer``` as a parameter (that method’s signature might be something like ```public void pairWithOtherComputer(Computer other)```). If you’re writing another method in ```Computer```, and want to call the ```pairWithOtherComputer()``` method, you could use ```this``` as the parameter. That call might look something like ```this.pairWithOtherComputer(this)```. You’re using the current object to call the method and are passing that object as that method’s parameter.

```java
public void pairWithOtherComputer(Computer other){
    // Code for method that uses the parameter other
}

public void setUpConnection(){
    // We use "this" to call the method and also pass "this" to the method so it can be used in that method
    this.pairWithOtherComputer(this);
}
```

**Person.java**
```java
public class Person{
    public int age;
    public int wisdom;
    public int fitness;

    public Person(int inputAge){
        this.age = inputAge;
        this.wisdom = inputAge * 5;
        this.fitness = 100 - inputAge;
    }

    public void setAge(int newAge){
        this.age = newAge;
    }

    public void setWisdom(int newWisdom){
        this.wisdom = newWisdom;
    }

    public void setFitness(int newFitness){
        this.fitness = newFitness;
    }

    public void hasBirthday(){
        //Complete this method
        
    }
}
```

**Main.java**
```java
public class Main{
    public static void main(String[] args){
        Person emily = new Person(20);
        emily.hasBirthday();
        System.out.println("New age is: " + emily.age);
        System.out.println("New wisdom is: " + emily.wisdom);
        System.out.println("New fitness is: " + emily.fitness);
    }
}
```

EXERCISE:
1. Look at the ```Person``` class. It has three instance fields ```age```, ```wisdom```, and ```fitness```. Each instance field has its mutator method declared.

    For now, run the code.

    **SOLUTION**

    ```git
    Error: Main method not found in class Person, please define the main method as:
    public static void main(String[] args)
    or a JavaFX application class must extend javafx.application.Application
    ```

2. Notice that we’ve provided an empty ```hasBirthday()``` method.

    Inside the ```hasBirthday()``` method, use the mutator method to increase the ```age``` by ```1```, increase ```wisdom``` by ```5```, and decrease ```fitness``` by ```3```.

    **SOLUTION:**

    **Person.java**
    ```java
    public class Person{
        public int age;
        public int wisdom;
        public int fitness;

        public Person(int inputAge){
            this.age = inputAge;
            this.wisdom = inputAge * 5;
            this.fitness = 100 - inputAge;
        }

        public void setAge(int newAge){
            this.age = newAge;
        }

        public void setWisdom(int newWisdom){
            this.wisdom = newWisdom;
        }

        public void setFitness(int newFitness){
            this.fitness = newFitness;
        }

        public void hasBirthday(){
            //Complete this method
            this.setAge(this.age + 1);
            this.setWisdom(this.wisdom + 5);
            this.setFitness(this.fitness - 3);
        }
    }
    ```

3. Switch over to **Main.java**. You will notice that we created an instance of ```Person``` named ```emily```! Run the code to see the output.

    **SOLUTION:**

    **Main.java**
    ```java
    public class Main{
        public static void main(String[] args){
            Person emily = new Person(20);
            emily.hasBirthday();
            System.out.println("New age is: " + emily.age);
            System.out.println("New wisdom is: " + emily.wisdom);
            System.out.println("New fitness is: " + emily.fitness);
        }
    }
    ```

    OUTPUT:
    ```git
    New age is: 21
    New wisdom is: 105
    New fitness is: 77
    ```

