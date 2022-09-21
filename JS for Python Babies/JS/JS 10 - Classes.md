# JS 10 - Classes

Classes aren't too relevant in Javascript. However, it's better to know the syntax if they ever do come up. I know personally, learning how classes worked made everything else click.

For example, **arrays are a type of object** that are derived from the Array class. As such, every array has the same stuff. `length` is just a property of every array, the `forEach()` function is just a class method of the Array class and so on.

Classes form the basis of Object Oriented Programming, but they can prove useful for other paradigms too.

##### Anatomy

```javascript
class ClassName {
  constructor( name )
  {
    this.name = name
  }
  
  classMethod() 
  {
    return "This is basically just a function"
  }
}
```

- `ClassName` can be whatever you want; recommended you use `PascalCase` as opposed to `camelCase` for the name

- `constructor()` is a method called on object instantiation (in Python, its `__init__()`). It essentially sets up the object.

- `this` refers to the object itself. So `this.name` will refer to the `name` variable of that specific object as opposed to any other.

Of couse, constructors and class methods can also take parameters.

### Instantiating an object with a class

```javascript
let object = new ClassName("Ben")
```

Accessing Properties and Methods

```javascript
object.name           // "Ben"
object.classMethod()  // "This is basically just a function"
```


