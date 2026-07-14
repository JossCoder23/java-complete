## Method Overriding
One common use of polymorphism with Java ```classes``` is something we mentioned earlier — overriding parent class ```methods``` in a child class. Like the + operator, we can give a single method slightly different meanings for different classes. This is useful when we want our child class method to have the same name as a parent class method but behave a bit differently in some way.

Let’s say we have a ```BankAccount``` class that allows us to print the current balance. We want to build a ```CheckingAccount``` class that inherits the functionality of a ```BankAccount``` but with a modified ```printBalance()``` method. We can do the following:

```java
class BankAccount {
    protected double balance;

    public BankAccount(double balanceIn){
        balance = balanceIn;
    }

    public void printBalance() {
        System.out.println("Your account balance is $" + balance);
    }
    }

    class CheckingAccount extends BankAccount {
    
    public CheckingAccount(double balance) {
        super(balance);
    }

    @Override
    public void printBalance() {
        System.out.println("Your checking account balance is $" + balance);
    }
}
```

Notice that in order to properly override ```printBalance()```, in ```CheckingAccount``` the method has the following in common with the corresponding method in ```BankAccount```:

* Method name
* Return type
* Number and type of parameters

You may have also noticed the @Override keyword above printBalance() in CheckingAccount. This annotation informs the compiler that we want to override a method in the parent class. If the method doesn’t exist in the parent class, we’ll get a helpful error when we compile the program.

### Keep Reading: AP Computer Science A Students
In a previous exercise, we learned that the super keyword can be used to call the constructor of a superclass. That’s not the only use of super; we can also use this keyword to call the methods of a parent class. While we now have the ability to override methods from a superclass, we may find ourselves in a unique situation where we want to use the superclass method instead of the subclass’ overridden method.

If that’s the case, we can call the parent class method by prepending super followed by the dot operator (.) to the method call. Note that this only works if we pass in the proper method parameters. Let’s see this in action by adding a checkBalances() method to CheckingAccount that calls both versions of printBalance():

```java
class CheckingAccount extends BankAccount {
    public CheckingAccount(double balance) {
        super(balance);
    }

    @Override
    public void printBalance() {
        System.out.println("Your checking account balance is $" + balance);
    }

    public void checkBalances() {
        // calls method from CheckingAccount
        printBalance();
        // calls method from BankAccount
        super.printBalance();
    }

    public static void main(String[] args) {
        CheckingAccount myCheckings = new CheckingAccount(5000);
        myCheckings.checkBalances();
    }
}
```

This program will output:
```git
Your checking account balance is $5000
Your account balance is $5000
```

**EXERCISE:**
1. Inside the ```Noodle``` class, we have a ```cook()``` method that prints “Boiling.” and changes the ```texture``` to “cooked”.

    The ```Noodle``` class has a child class called spätzle which is a German noodle that follows a different cooking procedure than the normal noodle: grinding or scraping the dough into the pot of boiling water. 

    Override the inherited ```cook()``` method so we can use it to cook the spätzle too.

    In the ```cook()``` method print the following string “Grinding or scraping the dough into the pot of boiling water.” and set the ```texture``` to “cooked”.

    Remember to add ```@Override``` above the method.

    **SOLUTION:**

    **Spaetzle.java**
    ```java
    class Spaetzle extends Noodle {
        
        Spaetzle() {
            super(3.0, 1.5, "irregular", "eggs, flour, salt");
            this.texture = "lumpy and liquid";     
        }

        // Add the new cook() method below:  
        @Override
        public void cook() {
            System.out.println("Grinding or scraping the dough into the pot of boiling water.");
            this.texture = "cooked";
        }

    }
    ```

2. Inside the overridden method ```cook()``` of ```Spaetzle``` class, include a line that prints out the string “Boiling”.

    *Note: Switch over to Main.java when running your code to see the final results.*

    **Spaetzle.java**
    ```java
    class Spaetzle extends Noodle {
        
        Spaetzle() {
            super(3.0, 1.5, "irregular", "eggs, flour, salt");
            this.texture = "lumpy and liquid";     
        }

        // Add the new cook() method below:  
        @Override
        public void cook() {
            System.out.println("Grinding or scraping the dough into the pot of boiling water.");
            System.out.println("Boiling");
            this.texture = "cooked";
        }

    }
    ```

    **Main.java**
    ```java
    public class Main{
        public static void main(String[] args) {
            Spaetzle kaesespaetzle = new Spaetzle();
            kaesespaetzle.cook();
        }
    }
    ```

    OUTPUT:
    ```git
    Grinding or scraping the dough into the pot of boiling water.
    Boiling
    ```