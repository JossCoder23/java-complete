## Reassigning Instance Fields
Earlier, we thought about a Savings Account as a type of object we could represent in Java.

Two of the ```methods``` we need are depositing and withdrawing:
```java
public class SavingsAccount{

    double balance;

    public SavingsAccount(double startingBalance){
        balance = startingBalance;
    }

    public void deposit(double amountToDeposit){
        //Add amountToDeposit to the balance
    }

    public void withdraw(double amountToWithdraw){
        //Subtract amountToWithdraw from the balance
    }

    public static void main(String[] args){

    }

}
```

These methods would change the value of the variable ```balance```. We can reassign balance to be a new value by using our assignment operator, ```=```, again.
```java
public void deposit(double amountToDeposit){
    double updatedBalance = balance + amountToDeposit;
    balance = updatedBalance;
}
```

Now, when we call ```deposit()```, it should change the value of the instance field ```balance```:
```java
public static void main(String[] args){
    SavingsAccount myAccount = new SavingsAccount(2000);
    System.out.println(myAccount.balance);
    myAccount.deposit(100);
    System.out.println(myAccount.balance);
}
```

This code first prints ```2000```, the initial value of ```myAccount.balance```, and then prints ```2100```, which is the value of ```myAccount.balance``` after the ```deposit()``` method has run.

Changing instance fields is how we change the state of an object and make our objects more flexible and realistic.

**Store.java**
```java
public class Store {

    // instance fields
    String productType;
    public double price;
        
    // constructor method
    public Store(String product, double initialPrice) {
        productType = product;
        price = initialPrice;
    }
        
    // increase price method
    public void increasePrice(){
        
    }
    
}
```

**Main.java**
```java
public class Main {
  public static void main(String[] args) {
    Store lemonadeStand = new Store("Lemonade", 3.75);
  }
}
```

EXERCISE:
1. We have added a new instance field to our ```Store``` class called ```price``` and an empty ```increasePrice()``` method.

    Add a parameter ```double priceToAdd``` to the ```increasePrice()``` method.    
    
    *Note: it is okay to get an error regarding a missing main() method. The main() method is defined in Main.java.*

    SOLUTION:
    
    **Store.java**
    ```java
    public class Store {

        // instance fields
        String productType;
        public double price;
            
        // constructor method
        public Store(String product, double initialPrice) {
            productType = product;
            price = initialPrice;
        }
            
        // increase price method
        public void increasePrice(double priceToAdd){
            
        }
            
    }
    ```

2. We need to create a variable to store the increased price of our product.

    Inside ```increasePrice()```, create a new variable called ```double newPrice``` and set it equal to the addition of ```price``` and ```priceToAdd```.

    *new Price = price + priceToAdd*

    SOLUTION:
    
    **Store.java**
    ```java
    public class Store {

        // instance fields
        String productType;
        public double price;
            
        // constructor method
        public Store(String product, double initialPrice) {
            productType = product;
            price = initialPrice;
        }
            
        // increase price method
        public void increasePrice(double priceToAdd){
            double newPrice = price + priceToAdd;
        }
            
    }
    ```

3. Inside the ```increasePrice()``` method, assign the ```newPrice``` to the instance field ```price```.

    SOLUTION:
    
    **Store.java**
    ```java
    public class Store {

        // instance fields
        String productType;
        public double price;
            
        // constructor method
        public Store(String product, double initialPrice) {
            productType = product;
            price = initialPrice;
        }
            
        // increase price method
        public void increasePrice(double priceToAdd){
            double newPrice = price + priceToAdd;
            price = newPrice;
        }
            
    }
    ```

4. Let’s use our ```increasePrice()``` method inside ```main()``` in Main.java.

    Increase the price of ```lemonadeStand``` by 1.50 using ```increasePrice()``` method.

    Print the instance field ```price``` to see the updated price of ```lemonadeStand```.

    SOLUTION:
    
    **Main.java**
    ```java
    public class Main {
        public static void main(String[] args) {
            Store lemonadeStand = new Store("Lemonade", 3.75);
            lemonadeStand.increasePrice(1.50);
            System.out.println(lemonadeStand.price);
        }
    }
    ```

    OUTPUT:
    ```git
    5.25
    ```