# Java 1 - Data Types and Variables

## Data Types

A **Data Type** defines what values an item can and cannot take - you've seen these before in Python. Strings, Integers, Floats... While in Python, you seldom had to care about them owing to its **weakly typed** nature, Java is a lot more strict.

There are **primitive** and **non-primitive**.

**Primitive** data types are data types **without and methods or properties**. They are used to construct non-primitive data-types. Examples include Integers, Characters and Booleans.

**Non-primitive** data types are the opposite. They have methods and properties. These are mostly the data types **you create yourself** through making your own classes, but there is one very common exception: Strings.

### List of Common Data Types

| Type      | Example                | Use-case                                    | Notes                     |
| --------- | ---------------------- | ------------------------------------------- | ------------------------- |
| Integer   | `int number = 0;`      | Standard for whole numbers, -ve and +ve     |                           |
| Character | `char letter = 'a';`   | For single characters, can convert to ASCII | Must be defined with `''` |
| Float     | `float number = 0.0;`  | For decimals                                | Least precision           |
| Double    | `double number = 0.0;` | For decimals                                | Medium precision          |
| Boolean   | `boolean cond = true;` | `true` or `false` values                    |                           |
| String    | `String str = "Hi!";`  | A list of characters                        | Capital 'S' required      |

These aren't *all* of them, but they are the one's you most likely be using.

## Variables

Variables are containers for values. Unlike in Python, you must **explicitly state the data type the variable contains** on initialisation. Below are a few examples:

```java
int age = 18;
String name = "Ben";
boolean isCool = true;
```

You can then re-set these values like so

```java
age = age + 10;
name = "Wlison";
isCool = false;
```

Note that variables of **any data-type** can have their value set to `null`, meaning empty.
