## Classes: Review
Object-oriented programming revolves around classes and objects. The ```class``` is a fundamental concept of OOP and programs in Java are built with multiple classes and their objects.

Let’s review what we’ve learned throughout this lesson:
* A class is a blueprint to create instances. It defines the state and behavior of these instances.
* Every class has a special method called constructor which is invoked when a new object is created. Constructors initialize the state of newly created instances.
* Instance fields define the characteristics of an object. We can declare them within a class but outside of any method or constructor.
* We use the dot operator (.) to access the instance fields.
* A program can have multiple classes, instances, and instance fields as per our program’s requirements.

Later, we will explore how a program can be made from multiple classes. For now, our programs have a single class.

```java
public class Dog { 
 // instance field 
 public String breed; 

 // constructor method 
 public Dog(String dogBreed) { 

   // value of parameter dogBreed assigned to instance field breed 
   breed = dogBreed; 
 }
} 
```

```java
public static void main(String[] args) { 
    // create instance: use 'new' operator and invoke constructor 
    Dog fido = new Dog("poodle"); 

    // fields are accessed using: the instance name, `.` operator, and the field name. 
    System.out.println(fido.breed);  // Prints "poodle" 
} 
```

Dog.java
```java
public class Dog {
    String breed;
    boolean hasOwner;
    int age;
    
    public Dog(String dogBreed, boolean dogOwned, int dogYears) {
        System.out.println("Constructor invoked!");
        breed = dogBreed;
        hasOwner = dogOwned;
        age = dogYears;
    }
    
    public static void main(String[] args) {
        System.out.println("Main method started");
        Dog fido = new Dog("poodle", false, 4);
        Dog nunzio = new Dog("shiba inu", true, 12);
        boolean isFidoOlder = fido.age > nunzio.age;
        int totalDogYears = nunzio.age + fido.age;
        System.out.println("Two dogs created: a " + fido.breed + " and a " + nunzio.breed);
        System.out.println("The statement that fido is an older dog is: " + isFidoOlder);
        System.out.println("The total age of the dogs is: " + totalDogYears);
        System.out.println("Main method finished");
    }
}
```