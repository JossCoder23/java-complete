## Quiz

1. What is the difference between declaring static variables and instance variables?
    * When declaring static variables, you use the this keyword along with the variable type.
    * ```When declaring static variables, you use the static keyword. For instance variables, you use the this keyword, or no keyword.```
    * When declaring static variables, you use no keywords, but when declaring instance variables you use the this keyword
    * When declaring static variables, you use keywords like private or public to make the variable static.

2. Given the code block, which line(s) of code will successfully print the value 5.
    ```java
    public class ATM{

        public static int totalMoney = 0;
        
        public ATM(){
            totalMoney += 5;
        }
        
        public static void main(String[] args){

            System.out.println(ATM.totalMoney); //Line 1
            
            ATM myATM = new ATM();
            System.out.println(ATM.totalMoney); //Line 2
            System.out.println(myATM.totalMoney); //Line 3
            
            ATM mySecondATM = new ATM();
            System.out.println(ATM.totalMoney); //Line 4
            System.out.println(myATM.totalMoney); //Line 5 
        }
    
    }
    ```
    * Line 2
    * Lines 1, 2, and 3
    * Lines 2, 3, 4, and 5
    * ```Lines 2 and 3```

3. What is the mistake in the code block?
    ```java
    public class ATM{

        public static int totalMoney = 0;
        
        public int money;
        
        public ATM(int money){
            this.money = money;
        }
        
        public static int getMoney(){
            return this.money;
        }
        
        public int getTotalMoney(){
            return totalMoney;
        }
    
    }
    ```
    * The non-static method getTotalMoney() is trying to access the static variable totalMoney.
    * ```The static method getMoney() is trying to access the non-static variable money.```
    * The variable totalMoney can’t be given the value of 0 when it is declared.
    * The constructor is incorrectly setting the value of an instance variable due to incorrectly using a local variable.

4. Fill in the code so the value 5 will be printed.
    ```java
    public class MyDemoClass{
  
        public static int variableA = 4;
        public int variableB;
        
        public MyDemoClass(){
            variableA += 1;
            this.variableB = 4;
        }
        
        public static void main(String[] args){
            
            MyDemoClass myObject = new _________;
            System.out.println(_________ . _________);
        }
    
    }
    ```
    * ```MyDemoClass```
    * ```MyDemoClass()```
    * ```variableA```
    * this
    * variableB

5. Why are static methods unable to interact with instance variables and non-static methods?
    * Static methods are associated with an object, not the class itself. As a result, static methods have no this reference.
    * Static methods can interact with non-static variables and methods. However, non-static methods can’t interact with static variables.
    * ```Static methods are associated with a class, not an object of the class. As a result, static methods have no this reference.```
