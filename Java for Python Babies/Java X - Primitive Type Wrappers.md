# Java ? - Primitive Type Wrappers

**Wrappers** are object equivalents to primitive data-types. Basically, they are a way to make things like `int`, `char`, etc. objects for use with certain generic classes.

Below are some of the most common types:

| Primitive Type | Generic Wrapper |
| -------------- | --------------- |
| `int`          | `Integer`       |
| `char`         | `Character`     |
| `float`        | `Float`         |

## Example of Usage

`ArrayList` is the most common place wrappers, but any **generic class** will use them.

```java
ArrayList<Integer>   numbers   = ArrayList<>();
ArrayList<Character> letters   = ArrayList<>();
ArrayList<Float>     decimals  = ArrayList<>();  
```
