## Review
Conditional operators work on boolean values to simplify our code. They’re often combined with conditional statements to consolidate the branching logic.

Conditional-AND, ```&&```, evaluates to ```true``` if the booleans on both sides are ```true```.
```java
if (true && false) {
    System.out.println("You won't see me print!");
} else if (true && true) {
    System.out.println("You will see me print!");
}
```

Conditional-OR, ```||```, evaluates to ```true``` if one or both of the booleans on either side is ```true```.
```java
if (false || false) {
    System.out.println("You won't see me print!");
} else if (false || true) {
    System.out.println("You will see me print!");
}
```

Logical-NOT, ```!```, evaluates to the opposite boolean value to which it is applied.
```java
if (!false) {
    System.out.println("You will see me print!");
}
```