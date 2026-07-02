## Order of Operations
If we were to place multiple operators in a single expression, what operation would the compiler evaluate first?
```java
int num = 12 / (10 - 4) + 4 * 2;
```

The order of operations dictates the order in which an expression (like the preceding one) is evaluated.

The order is as follows:
1. Parentheses
2. Exponents
3. Modulo/Multiplication/Division
4. Addition/Subtraction

Each numbered item in the list represents a level of precedence, where the levels are executed in ascending order. Operators that share the same precedence are evaluated from left to right within the expression.

With this new information in mind, let’s dissect the expression from before so that we can find the value of ```num```:
```java
12 / (10 - 4) + 4 * 2
```

```10 - 4``` would be evaluated first because it is wrapped in parentheses, and parentheses take first precedence. This value would become ```6```, making our expression look like this:
```java
12 / 6 + 4 * 2 
```

Next, our expression now contains division, addition, and multiplication. Multiplication and division take precedence over addition, so we will execute these first, moving left to right. ```12 / 6``` will be evaluated, yielding ```2```. Our expression now looks like this:
```java
2 + 4 * 2
```

Next, we calculate the multiplication, ```4 * 2```, which is ```8```. The expression now looks like this:
```java
2 + 8
```

```2 + 8``` is ```10```. This means that the value of num is ```10```.