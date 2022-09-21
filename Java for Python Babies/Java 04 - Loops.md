# Java 4 - Loops

Loops allow you to run the same code multiple times, albeit with a different value each time.

There are two main types: `for` and `while`.

### For Loop

The safer of the two, `for` loops have a lot more structure - making infinite loops a lot less likely.

##### Anatomy

*Run this code 10 times*

```java
for ( int i = 0; i < 10; i++ )
{
  // do this 
}
```

A `for` loop consists of 3 major aspects:

| Part         | What its doing                                                                 |
| ------------ | ------------------------------------------------------------------------------ |
| `int i = 0;` | initialising our **sentinel**.                                                 |
| `i < 10;`    | the condition for the loop to keep going. *If `i` is less than 10, keep going* |
| `i++`        | the **increment**. How much does `i` change by. `i++` just means `i = i + 1`   |

You can change the name of the **sentinel** from `i` to anything you want.

You can have `i` start at value you'd like as well

the **increment** can also **decrement** or **decrease** the value of `i` if you'd like.

### For Of Loop

**If index does not matter**, you can opt to use the cleaner and more concise **for of** loop when dealing with arrays.

```javascript
char[] arr = { 'a', 'b', 'c' };

for ( char letter : arr )
{
  System.out.println( letter ); // 'a' then 'b' then 'c'
}
```

### While Loops

A lot less structured, `while` loops will keep going **until their condition is met**.

##### Anatomy

*While counter is less than 10, keep running this*

```java
while ( counter < 10 )
{
  // do this
  counter++;
}
```

In the above example, we created our own **sentinel**, named `counter`. You could, however, have the condition be something a bit more advanced.

##### Do While

A very uncommon bit of syntax, the `do while` loop **guarantees the while loop is run at least once**. In essence, it ignores the condition the first time, and begins checking it after that.

```java
do {
  // this code
  counter++;
}
while ( counter < 10 )
```
