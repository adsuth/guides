# JS 7 - Functions

**Functions** (or methods) are blocks of code that can be called multiple times. They allow you to write cleaner code without repeating yourself.

##### Anatomy

You define a function like so:

```javascript
function myFunction()
{
  // code logic here
}
```

You then call the function like so:

```javascript
myFunction()
```

### Parameters

**Parameters** (or arguments) are values that you can pass in to a function.

```javascript
function addNumbers( a, b )
{
  return a + b
}
```

In the above example, the `addNumbers` function has the parameters `a` and `b`. When we call this method, we need to pass in values to replace `a` and `b`.

Note the `return` statement. This can be used to *return* a value from the function which can then be captured in a variable for example 

```javascript
let result = addNumbers( 10, 20 ) // returns 30
console.log( result ) // 30 
```

### Default Parameters

If you'd like to pass default parameters for your method to allow a user to call the method without passing certain parameters, you can do so like:

```javascript
function myFunction( a = "Default Value" )
{
  console.log( a )
}
```

If the user doesn't provide another value, `"Default Value"` will be used instead. This doesn't have to be a string, it can be anything - a number, boolean, array, object, etc.

### Different Types of Functions

Javascript has **three ways to define methods**. There is the standard one as shown above, but also **arrow functions** and **anonymous functions**.

Why? Well, functions can be stored in variables like any other data type, or passed as parameters to other functions. It's very useful to be able to pass small "anonymous" functions without having to declare them in an entire namespace.

**I'd recommend sticking to the above method of function declaration, unless you're using them as callback functions**

##### Anonymous Function

They work the same way as regular functions, but [**be aware of function hoisting**](https://www.tutorialspoint.com/function-hoisting-in-javascript#:~:text=Hoisting%20is%20a%20JavaScript%20technique,the%20top%20of%20their%20scope.).

The TL;DR is that, anonymous functions **will only be read as they appear sequentially in the script**, so you can't use them before they are declared.

**Regular functions** on the other hand can be used **before they're declared**.

```javascript
let myFunction = function() {
  // logic here
}

// calling
myFunction()
```

Anywhere you can store data, you can store an anonymous function.

```javascript
let object = {
  method: function() {
    // logic
  }
}

// calling
object.method()
```

##### Arrow Function

Arrow Functions are **anonymous functions with a shorter syntax**. They are similar to lambda functions in Java and Python. You'll see them a lot, specifically as callbacks for methods like `forEach` and `reduce`

```javascript
let myFunction = () => {}

// if you only have one parameter
let greet = name => {
  let output = "Hello ", name
  console.log( output )
}

// if you only need one line
let addNums = (a, b) => a + b
```

### Recursion

I thought I'd put this here because its a topic that a lot of people overcomplicate for no good reason. Recursion is the act of a function **calling itself**. Thats it. There's not much else to it. You'll learn later on that recursion is actually really bad for space complexity and that there's really no good reason to do it.

The easiest example is the Fibonacci sequence

```javascript
const ANCHOR_VALUE = 10000 // the "upper limit" of the function
function fibonacci( current, previous )
{
  if ( current > ANCHOR_VALUE ) return
  console.log( current )

  return fibonacci( current + previous, current )
}
```

A recursive function calls itself. In order to prevent infinite loops, you'll need an **anchor**. This can be anything, but most commonly, it reacts to the state of the function. For example, here, if the `current` value goes to high, it'll stop.
