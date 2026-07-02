## Compound Assignment Operators
Sometimes, we need to adjust the value of a variable.

Imagine we’re working at a bake sale and want to keep track of how many cupcakes we have by creating a variable called ```numCupcakes```:
```java
int numCupcakes = 12;
```

If we baked ```8``` more cupcakes, we know that we could update our variable using the ```+``` operator:
```java
numCupcakes = numCupcakes + 8; // Value is now 20
```

While this method works just fine, we had to write our variable ```numCupcakes``` twice. We can shorten this syntax by using a *compound assignment operator*.

Compound assignment operators perform an arithmetic operation on a variable and then reassigns its value. Using the ```+=``` compound assignment operator, we can rewrite our previous code like so:
```java
numCupcakes += 8; // Value is now 20
```

Now we only need to reference ```numCupcakes``` once.

We can use compound assignment operators for all of the arithmetic operators we’ve covered:
* Addition (```+=```)
* Subtraction (```-=```)
* Multiplication (```*=```)
* Division (```/=```)
* Modulo (```%=```)

EXERCISE:
1. You are also in charge of keeping track of how many cookies there are at the bake sale. This value is represented by the variable ```numCookies```.

    A customer comes and buys ```3``` cookies. Use the appropriate compound assignment operator to reflect this change.
2. Another customer buys half of the remaining cookies.

    Use the appropriate compound assignment operator to reflect this change.

    **BakeSale.java**
    ```java
    public class BakeSale {
        public static void main(String[] args) {   
            int numCookies = 17;

            // Add your code above
            System.out.println(numCookies);
        }
    }
    ```

SOLUTION - ONE:
```java
public class BakeSale {
	public static void main(String[] args) {   
		int numCookies = 17;
        numCookies -= 3;

        // Add your code above
        System.out.println(numCookies);
	}
}
```

OUTPUT:
```git
14
```

SOLUTION - TWO:
```java
public class BakeSale {
	public static void main(String[] args) {   
		int numCookies = 17;
        numCookies -= 3;

        // Add your code above
        System.out.println(numCookies);
        numCookies /= 2;
	}
}
```