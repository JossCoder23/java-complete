## Introducing Inheritance
When you hear the word “inheritance,” code may not be the first thing that springs to mind; you’re probably more likely to think of inheriting genetic traits, like eye color from your mother or a smile from your grandfather. But ```inheritance``` is also an important feature of object-oriented programming in Java.

Suppose we are building a ```Shape``` class in Java. We might give it some points in 2D, a method for calculating the area, and another method for displaying the shape. But what happens if we want a class for a triangle that has some triangle-specific methods? Do we need to redefine all of the same ```methods``` that we created for ```Shape```?

No! (Phew.) Lucky for us, a Java class can also inherit traits from another class. Because a ```Triangle``` is a ```Shape```, we can define ```Triangle``` so that it inherits fields and methods directly from ```Shape```. A reference of type ```Shape``` can refer to an object of ```Shape``` or an object of ```Triangle```. The object-oriented principle of inheritance saves us the headache of redefining the same class members all over again.

Our ```Triangle``` class will inherit all the traits of ```Shape```, but ```Triangle``` can also contain its own unique methods and ```variables```. For example, we could have an instance variable called ```hypotenuse``` and a method called ```findHypotenuse()``` that can only be accessed by ```Triangle``` class references. Objects of ```Triangle``` can call any method contained in ```Triangle``` or ```Shape```. This gives us a bunch of possibilities!

There are several terms you’ll encounter frequently:

* *Parent class, superclass, and base class* refer to the class that another class inherits from (like ```Shape```).
* *Child class, subclass, and derived class* refer to a class that inherits from another class (like ```Triangle```).

<img src="introduction.png" width="500">