# JS 8 - Arrays

Arrays (or lists) are a **data structure** that can store multiple values. Unlike more strict languages like Java, Arrays:

- Can have values of varying types

- Are dynamically sized

Arrays are **mutable**.

##### Anatomy

```javascript
let array = [1, false, "a"]
```

### Common Methods and Properties

*For the below examples, `let arr = [1, 2, 3]`*

| Name        | Example            | Result      | What it Does                                            |
| ----------- | ------------------ | ----------- | ------------------------------------------------------- |
| `length`    | `arr.length`       | `3`         | Property stores the size of the array.<br/>Not a method |
| `shift()`   | `arr.shift()`      | `[2, 3]`    | Removes and returns **first** value of array            |
| `pop()`     | `arr.pop()`        | `[1, 2]`    | Removes and returns **last** value of array             |
| `unshift()` | `arr.unshift( 0 )` | `[0,1,2,3]` | Adds given value to the start of the array              |
| `push()`    | `arr.push( 4 )`    | `[1,2,3,4]` | Adds given value to the ned of the array                |
| `indexOf()` | `arr.indexOf( 2 )` | `1`         | Returns index of **first occurence** of given value     |

### Mutability

Arrays are mutable. That means **their values will change when acted upon by processes**

For example:

```javascript
let array = [ 1, 2, 3 ]
array.pop()
console.log( array ) // [1, 2]
```

Unlike strings **you do not need to capture the output of these kinds of operations.**
