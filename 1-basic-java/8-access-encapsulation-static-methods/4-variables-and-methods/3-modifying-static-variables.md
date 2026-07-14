## Modifying Static Variables
Now that we’ve created a couple of static ```variables```, let’s start to edit them. The good news is that editing static variables is similar to editing any other variable. Whether you’re writing code in a constructor, a non-static method, or a static method, you have access to static variables.

Before we jump into the checkpoints, let’s think about times when you might want to edit static variables. Often times, you’ll see static variables used to keep track of information about all objects of a class. For example, our variable ```numATMs``` is keeping track of the total number of ```ATM```s in the system. Therefore, every time an ```ATM``` is created (using the constructor), we should increase that variable by 1. If we could somehow destroy an ```ATM```, the method that destroys it should decrease ```numATMs``` static variable by ```1```.

Similarly, we have a variable named ```totalMoney```. This variable is keeping track of all money across all ATMs. Whenever we remove money from an ATM using the non-static ```withdrawMoney()``` method, we should modify the ```money``` instance variable for that particular ATM as well as the ```totalMoney``` variable. In doing so, all ATMs will know how much money is in the system.

**ATM.java**
```java
public class ATM{
    // Static variables
    public static int totalMoney = 0;
    public static int numATMs = 0;

    // Instance variables
    public int money;

    public ATM(int inputMoney){
        this.money = inputMoney;

        // Steps 1 and 2: Edit numATMs and total money here
    }

    public void withdrawMoney(int amountToWithdraw){
        if(amountToWithdraw <= this.money){
        this.money -= amountToWithdraw;
        // Step 3: Edit totalMoney here
        }
    }

    public static void main(String[] args){

        System.out.println("Total number of ATMs: " + ATM.numATMs); 
        ATM firstATM = new ATM(1000);
        ATM secondATM = new ATM(500);
        System.out.println("Total number of ATMs: " + ATM.numATMs); 

        System.out.println("Total amount of money in all ATMs: " + ATM.totalMoney);  
        firstATM.withdrawMoney(500);
        secondATM.withdrawMoney(200);
        System.out.println("Total amount of money in all ATMs: " + ATM.totalMoney);    



    }

}
```

EXERCISE:
1. Edit the constructor to increase ```numATMs``` by ```1``` every time an ```ATM``` is created. In the main method, we’re printing out ```numATMs``` before and after creating some ```ATM```s. You should expect to see that number go up as you create ```ATM```s.

    **SOLUTION:**

    **ATM.java**
    ```java
    public class ATM{
        // Static variables
        public static int totalMoney = 0;
        public static int numATMs = 0;

        // Instance variables
        public int money;

        public ATM(int inputMoney){
            this.money = inputMoney;

            // Steps 1 and 2: Edit numATMs and total money here
            numATMs += 1;
        }

        public void withdrawMoney(int amountToWithdraw){
            if(amountToWithdraw <= this.money){
            this.money -= amountToWithdraw;
            // Step 3: Edit totalMoney here
            }
        }

        public static void main(String[] args){

            System.out.println("Total number of ATMs: " + ATM.numATMs); 
            ATM firstATM = new ATM(1000);
            ATM secondATM = new ATM(500);
            System.out.println("Total number of ATMs: " + ATM.numATMs); 

            System.out.println("Total amount of money in all ATMs: " + ATM.totalMoney);  
            firstATM.withdrawMoney(500);
            secondATM.withdrawMoney(200);
            System.out.println("Total amount of money in all ATMs: " + ATM.totalMoney);    



        }

    }
    ```

2. Edit the constructor so when a new ```ATM``` is created, the amount of money that ```ATM``` starts with gets added to the static variable ```totalMoney```.

    **SOLUTION:**

    **ATM.java**
    ```java
    public class ATM{
        // Static variables
        public static int totalMoney = 0;
        public static int numATMs = 0;

        // Instance variables
        public int money;

        public ATM(int inputMoney){
            this.money = inputMoney;

            // Steps 1 and 2: Edit numATMs and total money here
            numATMs += 1;
            totalMoney += inputMoney;
        }

        public void withdrawMoney(int amountToWithdraw){
            if(amountToWithdraw <= this.money){
            this.money -= amountToWithdraw;
            // Step 3: Edit totalMoney here
            }
        }

        public static void main(String[] args){

            System.out.println("Total number of ATMs: " + ATM.numATMs); 
            ATM firstATM = new ATM(1000);
            ATM secondATM = new ATM(500);
            System.out.println("Total number of ATMs: " + ATM.numATMs); 

            System.out.println("Total amount of money in all ATMs: " + ATM.totalMoney);  
            firstATM.withdrawMoney(500);
            secondATM.withdrawMoney(200);
            System.out.println("Total amount of money in all ATMs: " + ATM.totalMoney);    



        }

    }
    ```

3. Edit the ```withdrawMoney()``` method so when money is taken out of a specific ```ATM```, the static variable ```totalMoney``` also reflects that change.

    Take a look at the ```main()``` method — we’re printing ```totalMoney``` before and after withdrawing money from a couple of ```ATM```s.

    **SOLUTION:**

    **ATM.java**
    ```java
    public class ATM{
        // Static variables
        public static int totalMoney = 0;
        public static int numATMs = 0;

        // Instance variables
        public int money;

        public ATM(int inputMoney){
            this.money = inputMoney;

            // Steps 1 and 2: Edit numATMs and total money here
            numATMs += 1;
            totalMoney += inputMoney;
        }

        public void withdrawMoney(int amountToWithdraw){
            if(amountToWithdraw <= this.money){
                this.money -= amountToWithdraw;
                // Step 3: Edit totalMoney here
                totalMoney -= amountToWithdraw;
            }
        }

        public static void main(String[] args){

            System.out.println("Total number of ATMs: " + ATM.numATMs); 
            ATM firstATM = new ATM(1000);
            ATM secondATM = new ATM(500);
            System.out.println("Total number of ATMs: " + ATM.numATMs); 

            System.out.println("Total amount of money in all ATMs: " + ATM.totalMoney);  
            firstATM.withdrawMoney(500);
            secondATM.withdrawMoney(200);
            System.out.println("Total amount of money in all ATMs: " + ATM.totalMoney);    



        }

    }
    ```