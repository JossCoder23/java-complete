## The public Keyword
After running the code in the last exercise, you should be developing an intuition on what the ```public``` and ```private``` keywords are doing. These keywords are defining what parts of your code have access to other parts of your code.

We can define the access of many different parts of our code including instance ```variables```, ```methods```, ```constructors```, and even a class itself. If we choose to declare these as ```public``` this means that any part of our code can interact with them - even if that code is in a different class!

The way we declare something to be ```public``` is to use the ```public``` keyword in the declaration statement. In the code block below, we have a public class, constructor, instance variables, and method. Notice the five different uses of ```public```.

```java
public class Dog{
    public String name;
    public int age;

    public Dog(String input_name, int input_age){
        name = input_name;
        age = input_age;
    }
        
    public void speak() {
        System.out.println("Arf Arf! My name is " + name + " and I am a good dog!");
    }
}
```

Since everything about a ```Dog``` is public, any other class can access anything about a ```Dog```. For example, let’s say there was a ```DogSchool``` class. Any method of the ```DogSchool``` class could make a new Dog using the ```public Dog``` constructor, directly access that ```Dog```’s instance variables, and directly use that ```Dog```’s methods:

```java
public class DogSchool{
    public void makeADog(){
        Dog cujo = new Dog("Cujo", 7);
        System.out.println(cujo.age);
        cujo.speak();
    }
}
```

Notice that the ```DogSchool``` class and the ```makeADog()``` method are also public. This means that if some other class created a ```DogSchool```, they would have access to these methods as well! We have public methods calling public methods!

One final thing to note is that for the purposes of this lesson, we’ll almost always make our ```classes``` and constructors ```public```. While you can set them to ```private```, it’s fairly uncommon to do so. Instead, we’ll focus on why you might make your instance variables and methods ```private```. We’ll start looking into the ```private``` keyword in the next exercise.

**CheckingAccount.java**
```java
public class CheckingAccount{
    private String name;
    private int balance;
    private String id;
    
    public CheckingAccount(String inputName, int inputBalance, String inputId){
        name = inputName;
        balance = inputBalance;
        id = inputId;
    }
    
    public void addFunds(int fundsToAdd){
        balance += fundsToAdd;
    }
    
    public void getInfo(){
        System.out.println("This checking account belongs to " + name +". It has " + balance + " dollars in it.");
    }
}
```

**Bank.java**
```java
public class Bank{
    public static void main(String[] args){
        CheckingAccount accountOne = new CheckingAccount("Zeus", 100, "1");
        CheckingAccount accountTwo = new CheckingAccount("Hades", 200, "2");
        System.out.println(accountOne.name);
        accountOne.addFunds(5);
        accountOne.getInfo();
    }
}
```

EXERCISE:
1. Inside the **CheckingAccount.java** file, observe the declared methods and variables.

    Open the Bank.java file and click “Run” and take note of the errors that appear.

    *Note: Make sure you have the Bank.java file open (not CheckingAccount.java file) when you click “Run”.*

    **SOLUTION:**

    ```cmd
    Bank.java:5: error: name has private access in CheckingAccount
        System.out.println(accountOne.name);
                                    ^
    1 error
    ```

2. We are getting errors because inside ```main()``` of **Bank.java**, we are trying to access the ```name``` instance field of ```CheckingAccount``` which is declared as ```private```.

    To fix the problem, change the access modifier of the ```name``` field so that it may be accessed from outside the ```CheckingAccount``` class.

    **SOLUTION:**

    **CheckingAccount.java**
    ```java
    public class CheckingAccount{
        public String name;
        private int balance;
        private String id;
        
        public CheckingAccount(String inputName, int inputBalance, String inputId){
            name = inputName;
            balance = inputBalance;
            id = inputId;
        }
        
        public void addFunds(int fundsToAdd){
            balance += fundsToAdd;
        }
        
        public void getInfo(){
            System.out.println("This checking account belongs to " + name +". It has " + balance + " dollars in it.");
        }
    }
    ```

    OUTPUT:
    ```git
    Zeus
    This checking account belongs to Zeus. It has 105 dollars in it.
    ```