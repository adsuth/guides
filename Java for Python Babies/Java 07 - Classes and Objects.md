# Java 7 - Classes and Objects

This is where things deviate from what you may know from functional programming languages like JavaScript or Python - though these concepts certainly exist in those languages, you can get by without them. The same is not true in Java.

A `class` is like a mould, from which `objects` can be **instantiated** created.

Making a class is equivalent to making your own, non-primitive data type. As such, you can use them in `ArrayLists` and so on.

##### Example of a Class

```java
class Dog {
  // [1]    
  private String name;  
  public int animalNumber = 10;

  // [2]
  public Dog( String name )
  {
    this.name = name;
  }

  // [3]
  public void greet()
  {
    System.out.println( this.name + " says hello!" );
  }

  public int void getAnimalNumber()
  {
    return this.animalNumber;
  }

}
```

There's quite a bit to unpack here, but it's just a lot. None of it is difficult.

###### [1] Instance variables

```java
private String name;
public int animalNumber = 10;
```

Instance variables are variables tied to **each instance (or object) of the class**. They are independent from any other instance. For example, if I had two `Dog` objects, each would have a `name` property, but each would be independent from one another.

You should give each instance variable an [Access Modifier](./Java X - Access Modifiers.md). `private` will mean **only methods within the class will be able to read its value**.

Lastly, unless you want the value of your instance variable to be the same in every class, you shouldn't give it a value here. That's what the **constructor** is for. The `animalNumber` property is an example of a set instance variable that will be the same in all new instances.

###### [2] Constructor

Important to note: The constructor **must share the name of the class**.

```java
public Dog( String name )
{
  this.name = name;
}
```

The constructor is **the method that is called when instantiating an object**. It *constructs* the object from the class "blueprint".

The `this` keyword is a way of indicating that you are referring to **the object's property of that name**. in the case of,

```java
this.name = name;
```

We are saying *set the name property of this object to the name I passed in*.

###### [3] Class methods

Class methods are like regular methods, but they can only be used **in relation to an instance**, provided they are not static (more on that below). Like with instance variables, if they are `private`, they will not be accessible outside of the class.

The `getAnimalNumber()` method is `static`, and as such can be accessed **without an instance** like so,

```java
Dog.getAnimalNumber() // >> 10
```

Note that you **cannot use any instance variables set by the constructor** in these methods as there isn't an instance.

## Initialising a Class

A running theme in this guide is that showing is the best way to explain things, and this is no exception.

```java
Dog myDog      = new Dog( "Sif" );       // creates a new Dog with name "Sif"
Dog myOtherDog = new Dog( "Amaterasu" ); // creates a new Dog with name "Amaterasu" 
```

Above, we **instantiated** two **objects**, `myDog` and `myOtherDog`. The class `Dog` has a method, `greet()` and as such, both objects have a `greet()` method which we can access with **dot notation**.

```java
     myDog.greet() // >> Sif says hello!
myOtherDog.greet() // >> Amaterasu says hello!
```

Properties can also be accessed, provided **they are not private**. You can do so in pretty much the same way,

```java
myDog.animalNumber // >> 10
```

## Getters and Setters

**Getters** and **Setters** are methods that get and set data from an object respectively.

  Getters allow access to `private` variables that would otherwise be inaccessible.

  Setters allow you to set a property to a new value.

*In the below example, the methods are within the `Dog` class*

```java
public String getName()
{
  return this.name;
}
public void setName( String newName )
{
  this.name = newName;
}
```

## Extra Reading

- [Access Modifiers](./Java X - Access Modifiers.md)

- [Inheritance](./Java 8 - Inheritance.md)

- [Interfaces](./Java 9 - Interfaces.md)

- Object Oriented Programming
