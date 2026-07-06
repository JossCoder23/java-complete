## Combining Conditional Operators
We have the ability to expand our boolean expressions by using multiple conditional operators in a single expression.

For example:
```java
boolean foo = true && !(false || !true)
```

How does an expression like this get evaluated by the compiler? The order of evaluation when it comes to conditional operators is as follows:

1. Conditions placed in parentheses - ```()```
2. NOT - ```!```
3. AND - ```&&```
4. OR - ```||```
Using this information, let’s dissect the expression above to find the value of ```foo```:
```java
true && !(false || !true)
```

First, we’ll evaluate (```false || !true```) because it is enclosed within parentheses. Following the order of evaluation, we will evaluate ```!true```, which equals ```false```:
```java
true && !(false || false)
```

Then, we’ll evaluate ```(false || false)``` which equals ```false```. Now our expression looks like this:
```java
true && !false
```

Next, we’ll evaluate ```!false``` because it uses the NOT operator. This expression equals ```true``` making our expression the following:
```java
true && true
```

```true && true``` evaluates to ```true```; therefore, the value of ```foo``` is ```true```.