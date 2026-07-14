## Quiz

1. What does encapsulation mean?
    * The concept that some variables only exist in a certain scope.
    * ```The concept of separating methods and variables into distinct bundles of logic.```
    * The concept of creating different classes to represent objects in the real world.
    * The concept of returning values from your methods.

2. What value will be printed given the following code snippet?
    ```java
    public class Human(){
        public String name;
        
        public Human(String inputName){
            this.name = inputName;
        }
        
        public void sayName(String name){
            System.out.println("My name is " + name);
        }
        
        public static void main(String[] args){
            Human hero = new Human("Clark Kent");
            hero.sayName("Superman");
        }
    }
    ```
    * ```My name is Superman```
    * My name is hero
    * Nothing will be printed since sayName() is a void method.
    * My name is Clark Kent

3. Let’s say you’re writing a method named ```increaseAgeByFive()``` that is trying to increase the instance variable of the ```Dog``` class named ```age``` by ```5```. However, there is also a local variable named ```age```. How would you increase only the instance variable by ```5```.
    * age += 5;
    * ```this.age += 5;```
    * Dog.age += 5;
    * self.age += 5;

4. Explain the body of the methodOne() method in simple terms.
    ```java
    class myDemoClass(){
  
        int demoInstanceVariable;
        
        public void methodOne(){
            this.methodTwo(this);
        }
        
        public void methodTwo(myDemoClass a){
            System.out.println(a.demoInstanceVariable);
        }
        
    }
    ```
    * ```Whatever object (this) that called methodOne() proceeds to call methodTwo(). methodTwo() takes a myDemoClass object as a parameter, so in addition to calling the method, this passes itself as a parameter to methodTwo().```
    * Whatever object (this) that called methodOne() proceeds to call methodTwo(). methodTwo() has a default parameter of this which will automatically be whatever object called methodOne.
    * The method will print the instance variable demoInstanceVariable of whatever myDemoClass object that it gets as a parameter.
    * Look, Codecademy, we’re using that weird this keyword twice, and that’s really confusing. I can’t explain what that’s doing.

5. Fill in the code so the ```String``` instance variable named ```name``` is accessible from other classes, but the ```int``` variable named ```age``` isn’t.
    ```java
    public class Student{
        __________ String __________;
        __________ int __________;
    }
    ```
    * 20
    * int
    * ```age```
    * ```public```
    * ```private```
    * String
    * ```name```
    * "Winston"

6. Given the following instance variables for a ```Dog``` class, which of the following methods is an accessor method for the ```age``` variable?
    ```java
    public class Dog{
        private String name;
        private int age;
    
    }
    ```

    * ```java
        private String getAge(){
            return this.age;
        }
      ```

    * ```java
        private int getAge(){
            return this.age;
        }
      ```

    * ```cmd
        public int getAge(){
            return this.age;
        }
      ``` 

    * ```java
        public String getAge(){
            return this.age;
        }
      ```

7. Which of the following is NOT true about mutator methods.
    * Mutator methods are often void methods.
    * Mutator methods should be marked as public.
    * Mutator methods often have one parameter of the same type as the instance variable they’re interacting with.
    * ```Mutator methods return the value of an instance variable.```

