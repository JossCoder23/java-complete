## Static Variables
We’ll begin writing our own static ```method``` soon, but before we do, let’s take a look at static ```variables```. Much like static methods, you can think of static variables as belonging to the class itself instead of belonging to a particular object of the class.

Just like with static methods, we can access static variables by using the name of the class and the ```.``` operator. Finally, we declare static variables by using the ```static``` keyword during declaration. This keyword usually comes after the variable’s access modifier (```public``` or ```private```).

When we put this all together, we might end up with a class that looks something like this:

```java
public class Dog{
    // Static variables
    public static String genus = "Canis";

    //Instance variables
    public int age;
    public String name;

    public Dog(int inputAge, String inputName){
        this.age = inputAge;
        this.name = inputName;
    }
}
```

Since all dogs share the same genus, we could use a static variable to store that information for the entire class. However, we want each dog to have its own unique ```name``` and ```age```, so those aren’t ```static```. We could now access this static variable in a ```main()``` function like so:

```java
public class Dog{
    //Variables, constructors and methods defined here

    public static void main(String[] args){
        System.out.println(Dog.genus); // Prints Canis
    }
}
```

Unlike static methods, you can still access static variables from a specific object of the class. However, no matter what object you use to access the variable, the value will always be the same. You can think of it as all objects of the class sharing the same variable

```java
public static void main(String[] args){
    Dog snoopy = new Dog(3, "Snoopy");
    Dog ringo = new Dog(5, "Ringo");

    System.out.println(Dog.genus); // Prints Canis
    System.out.println(snoopy.genus); // Prints Canis
    System.out.println(ringo.genus); // Prints Canis
}
```

Finally, you might have seen a few static variables before. If you want easy access to the largest possible integer, you can get it by using ```Integer.MAX_VALUE```. If you look at the ```official documentation``` you’ll see that this variable is ```public```, ```static```, and ```final```. (```final``` means that you can’t change the variable’s value after creating it.) We’re starting to know a lot of Java keywords!

**ATM.java**
```java
public class ATM{

    // Step 2: Create your static variables here

    // Instance variables
    public int money;

    public ATM(int inputMoney){
        this.money = inputMoney;
    }

    public void withdrawMoney(int amountToWithdraw){
        if(amountToWithdraw <= this.money){
        this.money -= amountToWithdraw;
        }
    }

    public static void main(String[] args){
        // Step 1: Create your two ATMs here

        // Step 3: Print your static variable in three different ways here
    }

}
```

EXERCISE:
1. We’re going to be building out an ATM class that has both static and non-static variables. We’ve started by giving you an ATM class with non-static variables, a constructor, and some methods. In the ```main()``` method, use the constructor to create two ```ATM```s named ```firstATM``` and ```secondATM```. Use the constructor so the first ```ATM``` has ```1000``` dollars in it and the second has ```500```.

    If you’d like, you could print out each ```ATM```‘s ```money``` variable to confirm you created them successfully.

    **SOLUTION:**

    **ATM.java**
    ```java
    public class ATM{

        // Step 2: Create your static variables here

        // Instance variables
        public int money;

        public ATM(int inputMoney){
            this.money = inputMoney;
        }

        public void withdrawMoney(int amountToWithdraw){
            if(amountToWithdraw <= this.money){
            this.money -= amountToWithdraw;
            }
        }

        public static void main(String[] args){
            // Step 1: Create your two ATMs here
            ATM firstATM = new ATM(1000);
            ATM secondATM = new ATM(500);
            // Step 3: Print your static variable in three different ways here
        }

    }
    ```

2. Let’s create two static variables.

    First, we want to create a variable to keep track of how much money is in the system across all ATMs. This should be a ```public static int``` variable and should be named ```totalMoney```. This variable should begin with a value of 0.

    Second, we want to know how many ```ATM```s there are in the system. Again, this should be a ```public static int``` variable that has an initial value of ```0```. Name this variable ```numATMs```.

    **SOLUTION:**

    **ATM.java**
    ```java
    public class ATM{

        // Step 2: Create your static variables here
        public static int totalMoney = 0;
        public static int numATMs = 0;

        // Instance variables
        public int money;

        public ATM(int inputMoney){
            this.money = inputMoney;
        }

        public void withdrawMoney(int amountToWithdraw){
            if(amountToWithdraw <= this.money){
            this.money -= amountToWithdraw;
            }
        }

        public static void main(String[] args){
            // Step 1: Create your two ATMs here
            ATM firstATM = new ATM(1000);
            ATM secondATM = new ATM(500);
            // Step 3: Print your static variable in three different ways here
        }

    }
    ```

3. Let’s take a look at the first of these static variables. In the ```main()``` method, print your ```totalMoney``` variable three different times. The first time, you should use ```ATM.totalMoney```, the second time you should use ```firstATM.totalMoney```, and the third time you should use ```secondATM.totalMoney```. Do you expect these print statements to be the same or different?

    Right now the value stored in ```totalMoney``` doesn’t actually represent the total amount of money stored in all ATMs. In the next exercise, we’ll look into how to change the value of static variables.

    **SOLUTION:**

    **ATM.java**
    ```java
    public class ATM{

        // Step 2: Create your static variables here
        public static int totalMoney = 0;
        public static int numATMs = 0;

        // Instance variables
        public int money;

        public ATM(int inputMoney){
            this.money = inputMoney;
        }

        public void withdrawMoney(int amountToWithdraw){
            if(amountToWithdraw <= this.money){
            this.money -= amountToWithdraw;
            }
        }

        public static void main(String[] args){
            // Step 1: Create your two ATMs here
            ATM firstATM = new ATM(1000);
            ATM secondATM = new ATM(500);
            // Step 3: Print your static variable in three different ways here
            System.out.println(ATM.totalMoney);
            System.out.println(firstATM.totalMoney);
            System.out.println(secondATM.totalMoney);
        }

    }
    ```