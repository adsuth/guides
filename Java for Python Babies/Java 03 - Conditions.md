# Java 3 - Conditions

Conditions are a fancy way of saying `if` statements. They allow you to direct the flow of your program by choosing what to do in response to the current state.

### Logical Operators

**Logical Operators** are things like and, or, not, greater than, etc. They are particularly useful for performing boolean logic for use in `if` statements. Below is a table of operators, and their Python equivalents

*for the examples:*

  `boolean x = true; boolean y = false;`

  `int a = 5; int b = 10;`

| Python | Java | Example   | Condition                                                                    |
| ------ | ---- | --------- | ---------------------------------------------------------------------------- |
| `and`  | `&&` | `x && x`  | Both must be true                                                            |
| `or`   | `\|  | `         | `x \|                                                                        |
| `not`  | `!`  | `x && !y` | Inverts the value of condition. If y is false, makes it true and vice-versa. |
| `<`    | `<`  | `a < b`   | true if `a` **is less than** `b`                                             |
| `>`    | `>`  | `b > a`   | true if `b` **is greater than** `a`                                          |
| `==`   | `==` | `a == a`  | true if `a` **is equal to** `a`                                              |
| `<=`   | `<=` | `a <= b`  | true if `a` **is greater than or equal to** `b`                              |

You can also chain these together to create a more complex condition:

*if either x or y is true and a is less than b, then do this* 

```java
if ( ( x || y ) && ( a < b ) )
{
  // then do this stuff
}
```

## If, Else If and Else

`if` checks if a condition is met, and if it is, runs its codeblock. 

*If this is true, then do this*

```java
if ( true )
{
  // do this stuff
}
```

`else` is **only executed if the condition is not true**

*If this is true, then do this. Otherwise, do this instead.*

```java
if ( false )
{
  // do this stuff
}
else
{
  // do this instead
}
```

`else if` on the otherhand allows you to **provide additional checks if the initial `if` fails**. You can have as many of these as you want, just remember that **only the first sequential `else if` that is true will fire**.

*If this is true, then do this. If that isn't true, but this is, then do this. Otherwise, do this instead.*

```java
if ( false )
{
  // do this stuff
}
else if ( true )
{
  // do this stuff if the first one failed
}
else
{
  // do this instead
}
```

## Ternary Operator

A bit of an oddball in terms of syntax is the **ternary operator**. It functions as a (very unreadable) way to have an if / else statement on a single line.

```java
boolean x = true;
String result = ( x ) ? "x was true" : "x was false";
```

Just use an if / else - for the sake of my sanity and yours.

## Switch Statement

A `switch` statement takes in a value, and compares it to its set of "cases" to determine what to do next. These are relatively uncommon.

```java
switch ( val ):
  case 0:
    // this will run if val = 0
    break;
  case 1: 
    // this will run if val is 1
    break;
  default:
    // this will run if no other case matches
    break;
```

`break` keyword is required for each `case` as it breaks out of the `switch`, preventing multiple cases from firing.
