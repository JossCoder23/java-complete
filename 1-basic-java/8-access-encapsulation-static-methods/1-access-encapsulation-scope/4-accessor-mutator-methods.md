## Accessor and Mutator Methods
When writing ```classes```, we often make all of our instance variables ```private```. However, we still might want some other classes to have access to them, we just don’t want those classes to know the exact variable name. To give other classes access to a private instance variable, we would write an accessor method (sometimes also known as a “getter” method).

```java
public class Dog{
    private String name;
        
    //Other methods and constructors

    public String getName() {
        return name;
    }
}
```

Even though the instance variable ```name``` is ```private```, other classes could call the ```public``` method ```getName()``` which returns the value of that instance variable. Accessor methods will always be ```public```, and will have a return type that matches the type of the instance variable they’re accessing.

Similarly, ```private``` instance variables often have mutator methods (sometimes known as “setters”). These methods allow other classes to reset the value stored in ```private``` instance variables.

```java
public class Dog{
    private String name;
        
    //Other methods and constructors

    public void setName(String newName) {
        name = newName;
    }

    public static void main(String[] args){
        Dog myDog = new Dog("Cujo");
        myDog.setName("Lassie");
    }
}
```

Mutator methods, or “setters”, often are ```void``` methods — they don’t return anything, they just reset the value of an existing variable. Similarly, they often have one parameter that is the same type as the variable they’re trying to change.

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
}
```

**Bank.java**
```java
public class Bank{
    public static void main(String[] args){
        CheckingAccount accountOne = new CheckingAccount("Zeus", 100, "1");
        CheckingAccount accountTwo = new CheckingAccount("Hades", 200, "2");
    }
}
```

EXERCISE:
1. Inside ```CheckingAccount```, write an accessor method for the ```balance``` instance field called ```getBalance()```. This method should be accessible from other classes.

    Inside ```main()``` of **Bank.java**, use the accessor method ```getBalance()``` to print out the balance of ```accountOne```.

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

        public int getBalance() {
            return balance;
        }

    }
    ```

    **Bank.java**
    ```java
    public class Bank{
        public static void main(String[] args){
            CheckingAccount accountOne = new CheckingAccount("Zeus", 100, "1");
            CheckingAccount accountTwo = new CheckingAccount("Hades", 200, "2");
            System.out.println(accountOne.getBalance());
        }
    }
    ```

2. Let’s create a mutator method too.

    Inside the ```CheckingAccount``` class, write a mutator method called ```setBalance()``` that can be used to change the value of the ```balance``` field.

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

        public int getBalance() {
            return balance;
        }

        public void setBalance(int newBalance) {
            balance = newBalance;
        }

    }
    ```

3. Inside ```main()``` of Bank.java, use the ```setBalance()``` to set ```accountOne```’s ```balance``` to ```5000```.

    **SOLUTION:**

    **Bank.java**
    ```java
    public class Bank{
        public static void main(String[] args){
            CheckingAccount accountOne = new CheckingAccount("Zeus", 100, "1");
            CheckingAccount accountTwo = new CheckingAccount("Hades", 200, "2");
            System.out.println(accountOne.getBalance());
            accountOne.setBalance(5000);
        }
    }
    ```

4. Print the new ```balance``` of ```accountOne``` using ```getBalance()```.

    **SOLUTION:**

    **Bank.java**
    ```java
    public class Bank{
        public static void main(String[] args){
            CheckingAccount accountOne = new CheckingAccount("Zeus", 100, "1");
            CheckingAccount accountTwo = new CheckingAccount("Hades", 200, "2");
            System.out.println(accountOne.getBalance());
            accountOne.setBalance(5000);
            System.out.println(accountOne.getBalance());
        }
    }
    ```

    OUTPUT:
    ```git
    100
    5000
    ```
