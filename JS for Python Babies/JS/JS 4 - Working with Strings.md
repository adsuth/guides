# JS 4 - Working With Strings

Strings are a little more complex than numbers and booleans, so here's a quick little guide to the most common methods or operations you can do with them.

You'll notice strings share a lot in common with arrays, this is because at a lower level **strings are literally just arrays of characters**.

Strings are **immutable**, which means if you perform an operation (for example, using `trim()` to remove excess spaces in the front and back of a string), you will need to "capture" the returned value of that operation. The original string will **not be affected**.

For example

```javascript
let string = "Hello World!    "
string.trim()
console.log( string ) // would return -> "Hello World!    "

// you need to capture it like so:
let string = "Hello World!    "
string = string.trim()
console.log( string ) // would return -> "Hello World!"
```

##### Common String Methods and Properties

*For the below examples, `let str = "Hello World!"`*

| Method       | Example                  | Result          | What it does                                                                                      |
| ------------ | ------------------------ | --------------- | ------------------------------------------------------------------------------------------------- |
| `length`     | `str.length`             | `12`            | Property that contains the length of the string.<br/>Not a method.                                |
| `replace()`  | `str.replace( "l", "" )` | `"Helo World!"` | [1] Replaces **first occurence** of first given value, with second given value                    |
| `includes()` | `str.includes( "l" )`    | `true`          | returns `true` if list contains given value                                                       |
| `indexOf()`  | `str.indexOf( "l" )`     | `2`             | returns index of given value (if you pass a longer string, it will return the **starting index**) |
|              |                          |                 |                                                                                                   |
|              |                          |                 |                                                                                                   |
|              |                          |                 |                                                                                                   |
|              |                          |                 |                                                                                                   |

**[1] - How to Change ALL occurences**

Replacing ALL instances (requires use of [Regular Expressions](https://www.rexegg.com/regex-quickstart.html))

```javascript
let string = "llllllalllllll"
string = string.replace( /l/g, "a" )
console.log( string ) // "aaaaaaaaaaaaaa"
```

You can also have a replacement string that is longer than the target like

```javascript
let string = "HEY EVERY!"
string = string.replace( "!", "ONE" )
console.log( string )
```


