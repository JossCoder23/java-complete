## Quizz

1. Complete the for-each loop.
    ```java
    for (_______ _______ llamas) {
  
        sayHello(llama);
    
    }
    ```
    * in
    * llama
    * ```:```
    * ```String llama```

2. Rebuild the while loop as a for loop.
    ```java
    int i = 99;

    while (i > 0) {
    
        System.out.println(i + " bottles of soda on the wall.");
        i--;
    
    }

    // Rebuild here:
    for (______ ; ______ ; ______) {
    
        System.out.println(j + " bottles of soda on the wall.");
    
    }
    ```
    * j++
    * ```j--```
    * ```int j = 99```
    * j < 0
    * ```j > 0```

3. Complete the for loop so that it won’t cause an infinite loop.
    ```java
    for (______ ; ______ ; ______) {
    
        System.out.println(i);

    }
    ```
    * i--
    * ```i++```
    * ```i < 5```
    * i < 0
    * i = 0
    * ```int i = 0```
    * int i

4. When would it be helpful to use a ```for``` loop instead of a for-each loop when iterating over an ```ArrayList``` of items?
   
    * When you don’t know how long the ArrayList will be.
    * ```When you aren’t starting from the beginning of the ArrayList.```
    * When each item in the ArrayList has a different value.
    * When you’re worried about causing an infinite loop.

5. How many times will ```"Hello, I.T. Have you tried turning it off and on again?"``` be printed to the console?
    ```java
    int i = 1;

    while (i < 100) {
    
        System.out.println("Hello, I.T. Have you tried turning it off and on again?");
        
        i++;
    
    }
    ```
    * ```99```
    * An unknown number of times.
    * It will continue printing until the program crashes because of an infinite loop.
    * 100

6. How can you modify this code so that it won’t cause an infinite while loop?
    ```java
    int i = 7;

    while (i > 0) {
    
        System.out.println(i);
    
    }
    ```
    * ```Add i-- inside the while loop.```
    * Add i++ inside the while loop.
    * Add i++ after the while loop.
    * Add i-- after the while loop.
