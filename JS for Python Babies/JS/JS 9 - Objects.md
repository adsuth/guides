# JS 9 - Objects

**Objects** are another data structure in Javascript. Unlike arrays which are ordered lists, objects are unordered lists of key/value pairs.

They are similar to dictionaries in Python and structs in C.

You can also use classes in JS to create objects, but this "struct-like" syntax is a lot more common and simple.

##### Anatomy

```javascript
let object = {
  key: "value",
  num: 1,
  bool: true,
  obj: {
    key: "This is an inner object"
  },
  arr: [1, 2, 3],
  func: () => {
    // logic here
  }
}
```

### Accessing Values

You can access the values at specific keys by either using **dot notation** or in a similar way to how you would access values in an array, **square bracket notation**.

Both are useful for different reasons, **square bracket notation** is useful if you don't know the property you want to access before runtime.

```javascript
let object = {
  number: 1997
}

// dot notation
object.number // 1997

// square bracket notation
object["number"] // 1997
```

### Access All Keys and Values

You may want to iterate over all the keys or values in an object.

Take this object,

```javascript
let object = {
  a: 1,
  b: 2,
  c: 3
}
```

You can iterate over the values in an object by using a **for in** loop (see loops).

```javascript
for ( let value in object )
{
  console.log( value )
}
```

To list all *keys* in a string format however, you'll need to do something a bit more elaborate

```javascript
for ( let key of Object.keys( object ) )
{
  console.log( key )
} 
```

# 
