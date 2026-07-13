## What are Access and Scope?
As our Java programs begin to get bigger and we begin to have multiple Objects and Classes that interact with each other, the concepts of access and scope come into play. To oversimplify things, the concepts of access and scope both center around what parts of your programs can interact with specific variables or methods from other parts of your program. Let’s take a brief look at some of the concepts we’ll cover:

### Access 
* The ```public``` and ```private``` keywords and how they relate to Classes, variables, ```constructors```, and methods
* The concept of encapsulation
* Accessor methods, sometimes known as “getters”
* Mutator methods, sometimes known as “setters”

### Scope
* Local variables vs. instance variables
* The ```this``` keyword

**CheckingAccount.java**
```java
public class CheckingAccount{
    private String name;
    private int balance;
    
    public CheckingAccount(String inputName, int inputBalance){
        name = inputName;
        balance = inputBalance;
    }
}
```

**Bank.java**
```java
public class Bank{
    private CheckingAccount accountOne;
    private CheckingAccount accountTwo;

    public Bank(){
        accountOne = new CheckingAccount("Zeus", 100);
        accountTwo = new CheckingAccount("Hades", 200);
    }

    public static void main(String[] args){
        Bank bank = new Bank();

        System.out.println(bank.accountOne.name);
        System.out.println(bank.accountOne.balance);
    }
}
```

