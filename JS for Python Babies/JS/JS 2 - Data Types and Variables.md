# JS 2 - Data Types and Variables

### Data Types

Javascript, like Python, is dynamically typed. As such, data types aren't *too* important. They still matter mind you. `"1" + 2` will work, but likely won't return what you may expect.

| Type      | Example                 | Notes                                                              |
| --------- | ----------------------- | ------------------------------------------------------------------ |
| Number    | `0`, `0.5`, `-10`       | Integers and Floats                                                |
| String    | `"Hello World!`, `'Hi'` | Also denoted with backticks (`) for **string interpolation**       |
| Boolean   | `true` and `false`      |                                                                    |
| Undefined | `undefined`             | when a variable **is declared, but has no value assigned to it**   |
| Null      | `null`                  | Similar to undefined, but **you assign it manually to a variable** |

### Variables

Variables are essentially named bits of data - a common analogy being that they are like boxes that you can store data in.

```javascript
let myVariable = "Hello World!"
console.log( myVariable ) // >> Hello World!
```

#### Let, Var and Const

All variables have a **scope** - what can and can't see it. for example, a variable in a function won't be visible to a variable outside of that function and so on.

```javascript
let number = 10 
var number = 10
const NUMBER = 10
```

`let` and `var` are (mostly) identical, but I'd recommend you commit to using one or the other for consistency.

I generally use `let` for local variables, and `var` for my global variables that change like states of true/ false.

`const` on the other hand means **constant** and as it implies, a `const` variable **cannot be changed after it is defined**. These may seem useless, but they are very useful for global declarations of things you know shouldn't change.

For example, this can be defined to avoid the use of [magic numbers](https://en.wikipedia.org/wiki/Magic_number_(programming)#Unnamed_numerical_constants)

```javascript
const NUMBERS_OF_LETTERS_IN_ALPHABET = 26
```
