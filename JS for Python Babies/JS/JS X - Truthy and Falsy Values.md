# JS X - Truthy and Falsy Values

In Javascript, certain values can be implicitly true or false. This trait is known as truthy or falsy respectively.

Perhaps the most infamous being `""`, an empty string. If you were to run the following code, you'd find `""` is false, while `"hello!"` is true

```javascript
if ( "" )
{
  // this won't run
}
else
{
  // this will
}
```

Below are a list of (most) falsy values

| Value       | Notes |
| ----------- | ----- |
| `0`         |       |
| `"0"`       | [1]   |
| `""`        |       |
| `null`      |       |
| `undefined` |       |

**[1] - Warning for Common Pitfall**

Imagine a hypothetical situation where you are receiving a numeric value from an `<input>` tag by accessing it's `value` property. You want to make sure the user can't break your program by **not submitting a value**. Simple, right? An empty string is a **falsy value**, and so we can do the following:

```javascript
const input_tag = document.getElementById( "inputTagID" )
```

```javascript
if ( input_tag.value )
{
  // do this
}
else
{
  // reject bad input
}
```

The big, invisible issue is **what if a user enters the number 0?** This will be treated like a bad input, and rejected. To remedy this, make sure you are more specific with your conditions.

```javascript
if ( input_tag.value.length > 0 )
{
  // do this
}
else
{
  // reject bad input
}
```
