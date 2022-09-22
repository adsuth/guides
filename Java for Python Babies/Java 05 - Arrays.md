# Java 5 - Arrays

Arrays are a data structure that store an ordered list of values. They are known as lists in Python, but that isn't the only difference.

- Arrays in Java **can only store items of the same data-type**

- Arrays in Java have a **fixed size**

##### Anatomy

```java
int[] numbers = {1, 2, 3}; // defining with values (size will be 3)
int[] myArray = new int[30]; // defining array of size 30 
```

##### Accessing Elements in an Array

An array is an **ordered list of values** and as such, you can access a specific item in an array provided you know its **index**.

We can access values in arrays using the following syntax

```java
numbers[1] // gets index (position) 1 in array, which is 2
```

In the array `numbers`, we have three values, three indices.  As you can see below, each index corresponds to a specific value in the array.

```
numbers[0] >> 1
numbers[1] >> 2
numbers[2] >> 3
```

Remember that **arrays begin at position 0**.

##### Overwriting elements in an array

You can overwrite values in an array by assigning a new value to the specific index like so:

```java
numbers[1] = 5;
// numbers becomes
// { 1, 5, 3 }
```

Emphasis on **overwrite**. You **cannot add or remove values from an array in Java**. In other words, you **cannot change the size of arrays in Java**. You can assign a value in an array to `null` to essentially remove that value, but the position will still be there and the size of the array will not change.

##### Working with Arrays

Arrays don't have any methods, so you'll have to implement your own. We can easily get certain functionality by using `for` loops to iterate over all the values in the array.

*printing all values in the `numbers` array*

```java
for ( int i = 0; i < numbers.length; i++ )
{
  System.out.println( numbers[i] );
}
```

Note the use of `numbers.length`. `length` is a **property** of all arrays. It is an `int` representation of the length or size of the array (how many indices are in the array)

###### Index Of

*Get the index of the first ocurrence of 2 in the `numbers` array*

```java
int index;

for ( int i = 0; i < numbers.length; i++ )
{
  if ( numbers[ i ] == 2 )
  {
    index = i;
  }
}

// index >> 1
```

###### Contains

*See if `numbers` contains 2*

```java
boolean valueFound = false;

for ( int i = 0; i < numbers.length; i++ )
{
  if ( numbers[ i ] == 2 )
  {
    valueFound = true;
  }
}

// valueFound >> true
```

## Array Lists

Slightly more memory-intensive (so slight it doesnt really matter), an `ArrayList` is Java's way to create dynamic lists. You can add and remove elements from an `ArrayList`.

`ArrayList` is **not in Java by default**, you will need to import it. Netbeans will notify you with this ![](C:\Users\Adam\AppData\Roaming\marktext\images\2022-07-30-22-28-43-image.png) icon when you are missing an import. Click the icon, then `Add import for java.util.ArrayList` to automatically import `ArrayList`.

```java
import java.util.ArrayList; // to import just ArrayList
import java.util.*;         // to import everything from java.util
```

##### Anatomy

This is quite an ugly bit of syntax, but this is how you'd define an `ArrayList` of type `int`:

```java
ArrayList<Integer> numbers = new ArrayList<>();
```

- `ArrayList` is a data type.

- `<Integer>` specifies the data-type that is stored in the ArrayList (See [this page](./Java X - Primitive Type Wrappers.md))

- `numbers` is the name of the ArrayList

- `new ArrayList<>()` is instantiating a new object from the class `ArrayList` (more on that in Objects)

Important note: you cannot use the `[]` syntax to get the specific index of an ArrayList. Instead, use the `get()` method. See below for more methods.

##### Common Methods

*For the examples:*

  *We'll call ArrayLists "lists"*

  `ArrayList<Integer> arr = { 1, 2, 3 };`

| Method       | Example             | Result           | What it does                                     |
| ------------ | ------------------- | ---------------- | ------------------------------------------------ |
| `add()`      | `arr.add( 4 )`      | `{ 1, 2, 3, 4 }` | Adds new index to the end of the list            |
| `remove()`   | `arr.remove( 2 )`   | `{ 1, 3 }`       | Removes **first occurence** of given value       |
| `contains()` | `arr.contains( 2 )` | `true`           | returns `true` if list contains given value      |
| `indexOf()`  | `arr.indexOf( 2 )`  | `1`              | returns index of given value                     |
| `size()`     | `arr.size()`        | `3`              | returns the length of the list (how many values) |
| `get()`      | `arr.get( 1 )`      | `2`              | returns the value at given index                 |
| `clear()`    | `arr.clear()`       | `{}`             | removes all values in list                       |
| `toArray()`  | `arr.toArray()`     | `{ 1, 2, 3 }`    | returns an array equivalent of the list          |
