## Scope: The this Keyword
Often times when creating ```classes```, programmers will create local ```variables``` with the same name as instance variables. For example, consider the code block below:

```java
public class Dog{

    public String name;

    public Dog(String inputName){
        name = inputName;
    }

    public void speakNewName(String name){
        System.out.println("Hello, my new name is" + name);
    }

    public static void main(String[] args){
        Dog myDog = new Dog("Winston");
        myDog.speakNewName("Darla"); // Prints "Darla" - "Winston" ignored
    }

}
```

We have an instance variable named ```name```, but the method ```speakNewName``` has a parameter named ```name```. So when the method tries to print ```name```, which variable will be printed? By default, Java refers to the local variable name. So in this case, the value passed to the parameter will be printed and not the instance variable.

If we wanted to access the instance variable and not the local variable, we could use the ```this``` keyword.

```java
public class Dog{

    public String name;

    public Dog(String inputName){
        name = inputName;
    }

    public void speakNewName(String name){
        System.out.println("Hello, my new name is" + this.name);
    }
        
    public static void main(String[] args){
        Dog a = new Dog("Fido");
        Dog b = new Dog("Odie");

        a.speakNewName("Winston");
        // "Fido", the instance variable of Dog a is printed. "Winston" is ignored

        b.speakNewName("Darla");
        // "Odie", the instance variable of Dog b is printed. "Darla" is ignored.
    }

}
```

The ```this``` keyword is a reference to the current object. We used ```this.name``` in our ```speakNewName()``` method. This caused the method to print out the value stored in the instance variable ```name``` of whatever ```Dog``` Object called ```speakNewName()```. (Note that in this somewhat contrived example, the local variable ```name``` used as a parameter gets completely ignored).

Oftentimes, you’ll see ```constructors``` have parameters with the same name as the instance variable. For example, you might see something like:

```java
public Dog(String name){
    this.name = name;
}
```

You can read this as “set ```this Dog```‘s instance variable ```name``` equal to the variable passed into the constructor”. While this naming is a common convention, it can also be confusing. There’s nothing wrong with naming your parameters something else to be more clear. Sometimes you will see something like:

```java
public Dog(String inputName){
    this.name = inputName;
}
```

This is now a little clearer — we’re setting the ```Dog```‘s instance variable name equal to the ```name``` we give the constructor.

Finally, mutator ```nethods``` also usually follow this pattern:

```java
public void setName(String name){
    this.name = name;
}
```

We reset the instance variable to the value passed into the parameter.

Throughout the rest of this lesson, we’ll use ```this.``` when referring to an instance variable. This isn’t always explicitly necessary — if there’s no local variable with the same name, Java will know to use the instance variable with that name. That being said, it is a good habit to use ```this.``` when working with your instance variables to avoid potential confusion.

**SavingsAccount.java**
```java
public class SavingsAccount{

    public String owner;
    public double balanceDollar;
    public double balanceEuro;

    public SavingsAccount(String owner, double balanceDollar){
        // Complete the constructor
    }

    public void addMoney(int balanceDollar){
        // Complete this method
    }

}
```

**Main.java**
```java
public class Main{
    public static void main(String[] args){
        SavingsAccount zeusSavingsAccount = new SavingsAccount("Zeus", 1000);

        // Make a call to addMoney() to test your method
        
    }
}
```

EXERCISE:
1. We have an empty constructor for the ```SavingsAccount``` class. Inside the ```SavingsAccount``` class, there are three instance fields called ```owner```, ```balanceDollar```, and ```balanceEuro```.

    Inside the constructor ```SavingsAccount()```, set the instance variables to the local variables.

    For the instance variable ```balanceEuro``` set it equal to the local variable ```balanceDollar``` multiplied by ```0.85```. (Let’s suppose, every dollar is worth ```0.85``` euros.)

    **SOLUTION:**
    
    **SavingsAccount.java**
    ```java
    public class SavingsAccount{

        public String owner;
        public double balanceDollar;
        public double balanceEuro;

        public SavingsAccount(String owner, double balanceDollar){
            // Complete the constructor
            this.owner = owner;
            this.balanceDollar = balanceDollar;
            this.balanceEuro = balanceDollar * 0.85;
        }

        public void addMoney(int balanceDollar){
            // Complete this method
            
        }

    }
    ```

2. Inside ```SavingsAccount```, create a method called ```addMoney()``` that accepts a parameter called ```balanceDollar``` and increases the value of the field ```balanceDollar``` by the local variable of ```balanceDollar```.

    **SOLUTION:**
    
    **SavingsAccount.java**
    ```java
    public class SavingsAccount{

        public String owner;
        public double balanceDollar;
        public double balanceEuro;

        public SavingsAccount(String owner, double balanceDollar){
            // Complete the constructor
            this.owner = owner;
            this.balanceDollar = balanceDollar;
            this.balanceEuro = balanceDollar * 0.85;
        }

        public void addMoney(int balanceDollar){
            // Complete this method
            this.balanceDollar += balanceDollar;
        }

    }
    ```

3. Now add a print statement before adding the money to print this line:
    
    ```git
    "Adding <amountToAdd> dollars to the account." 
    ```

    And this statement should print after adding the money:

    ```git
    "The new balance is <currentBalance> dollars." 
    ```

    The code should print the actual balance in place of ```<currentBalance>```.

    **SOLUTION:**
    
    **SavingsAccount.java**
    ```java
    public class SavingsAccount{

        public String owner;
        public double balanceDollar;
        public double balanceEuro;

        public SavingsAccount(String owner, double balanceDollar){
            // Complete the constructor
            this.owner = owner;
            this.balanceDollar = balanceDollar;
            this.balanceEuro = balanceDollar * 0.85;
        }

        public void addMoney(int balanceDollar){
            // Complete this method
            System.out.println("Adding " + balanceDollar + " dollars to the account.");
            this.balanceDollar += balanceDollar;
            System.out.println("The new balance is " + this.balanceDollar + " dollars.");
        }

    }
    ```


4. Inside ```main()``` of the Main.java file, add ```2000``` dollars to ```zeusSavingsAccount``` by calling the ```addMoney()``` method of the ```zeusSavingsAccount``` instance.*

    **SOLUTION:**
    
    **Main.java**
    ```java
    public class Main{
        public static void main(String[] args){
            SavingsAccount zeusSavingsAccount = new SavingsAccount("Zeus", 1000);

            // Make a call to addMoney() to test your method
            zeusSavingsAccount.addMoney(2000);
        }
    }
    ```