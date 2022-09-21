# JS 1 - Introduction

Javascript was originally designed for browsers, but thanks to Node, it can be used for practically anything. Its an incredibly versatile language, being used from front end to back end. It's my personal favourite language, and is a great gateway to learn programming concepts.

Javascript and Python are similar in that they are both weakly typed languages. that basically means that data types don't matter all that much - especially not as much as they would in other languages like C or Java.

This page will get you started with JS, learning how to do the most basic operations.

*Important Note: Getting user input is quite convoluted in Node.js. Repl.it will allow you to use browser methods to achieve things like printing and getting input with `alert()` and `prompt()` respectively.*

## Printing

```javascript
// Printing to console
console.log( "Hello World!" )

// Printing in browser (as a popup)
alert( "Hello World!" )
```

#### String Concatenation

String concatenation is a fancy way of saying "adding strings together". 

```javascript
console.log( "Hello " + "World!" )
```

#### String Interpolation

String Interpolation is a (slightly) more advanced way to format strings. It allows you to add non-string data types seamlessly, without a melange of pluses.

In python:

```python
print( f"This is the number {10}!" ) # >> This is the number 10!

print( "This is the number %d", 10 ) # >> This is the number 10!
# Uses Format Specifiers
# %d is an int, %s is a string, etc. ( look up for more info )
```

In Javascript:

```javascript
console.log( `This is the number ${10}!` ) // >> This is the number 10!
// Note: the ${} syntax requires back ticks (``) instead of quotes ("")
```

# Variables

Variables are essentially named bits of data - a common analogy being that they are like boxes that you can store data in.

In python:

```python
myVariable = "Hello World!"
print( myVariable ) # >> Hello World!
```

In Javascript:

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

For example, this can be defined to avoid the use of "magic numbers"

```javascript
const NUMBERS_OF_LETTERS_IN_ALPHABET = 26
```

# Arrays and Lists

Arrays are a data structure that allow you to store an ordered list of values. In python these are (perhaps more intuitively) known as lists.

In both languages

In python:

```python
myArray = [ 1, 2, 3 ]
```

In Javascript:

```javascript
let myArray = [ 1, 2, 3 ]
```

### Accessing Specific Position

Both languages use the same syntax to access a specific position (**index**).

Remember that **arrays start at index 0**

```javascript
let myArray = [ 1, 2, 3 ]
console.log( myArray[ 1 ] ) // >> 2
```
