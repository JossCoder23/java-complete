## Static Methods Refresher
In this lesson, we’re going to dive into how to create ```classes``` with your own static ```methods``` and static ```variables```. To begin, let’s take a quick refresher on static methods.

Static methods are methods that belong to an entire class, not a specific object of the class. Static methods are called using the class name and the . operator. We’ve seen a couple of static methods already!

```java
double randomNumber = Math.random();
// Stores a random decimal between 0.0 and 1.0 in randomNumber

double number = Double.valueOf("2.5");
// Transforms the String "2.5" into a double
```

In the first example, ```random()``` is a static method that belongs to the ```Math``` class. We didn’t need to create a ```Math``` object (like ```Math myMathObject = new Math()```) in order to use that method. We could just call it using the class name.

Similarly, ```valueOf()``` is a static method of the ```Double``` class. Given a ```String``` as an input, this method will turn that ```String``` into a ```double```. Again, we don’t need to create a ```Double``` object in order to call this method — we use the class itself to call it.

Finally, notice that our ```main()``` methods have been ```static``` this whole time. When Java runs your program, it calls that the main method of your class — ```YourClassName.main()```.