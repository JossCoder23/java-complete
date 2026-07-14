## Quiz

1. Change Dinosaur so that only Dinosaur, its child classes, and the package it is in have access to the weight field.

    ```java
    public class Dinosaur {
  
        __________ double weight;
        
        public double getWeight() {
            return this.weight;
        }
    
    }
    ```
    * final
    * public
    * ```protected```
    * private

2. Imagine you want to build three Java classes in your package — one parent class and two child classes.

    How many files will you need to create?

    * ```Three.```
    * One.
    * Six.
    * Two.

3. Which is NOT a facet of polymorphism in Java?
    * It’s possible to use objects of different classes that share a parent class together in an array or ArrayList.
    * ```A Java class can inherit fields and methods from another class.```
    * You can use a child class object like a member of its parent class.
    * A Java child class can override its parent’s methods.

4. The parent class of Sauropoda requires that you pass a String called size into its constructor.

    Modify the constructor of Sauropoda so that all Sauropoda objects will be instantiated with a size of "large".

    ```java
    Sauropoda() {
        _________  _________  _________  _________;
    }
    ```
    * ```super```
    * ```(```
    * ```"large"```
    * ```)```
    * .
    * parent
    * String

5. Set up the class so that Triceratops inherits from Dinosaur.
    
    ```java
    public class _________ _________ _________ {
        // additional class members go here
    }
    ```
    * inherits
    * ```Triceratops```
    * ```Dinosaur```
    * Mangosaurus
    * ```extends```

6. Instantiate a Stegosaurus object as a Dinosaur.

    ```java
    public static void main(String[] args) {
    
        _________ steggy = new _________;
    
    }
    ```
    * Stegosaurus
    * Dinosaur()
    * ```Dinosaur```
    * ```Stegosaurus()```