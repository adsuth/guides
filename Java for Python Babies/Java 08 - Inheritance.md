# Java 8 - Inheritance

Inheritance is perhaps the most intuitive title of the **FOUR PILLARS OF OBJECT ORIENTED PROGRAMMING** (oooh fancy name!). It refers to a class **inheriting** properties and methods from a "parent" or "super" class.

First, there are a couple of ideas you should be aware of: **abstract classes** and **concrete classes**.

A good way of picturing the difference is with our `Dog` example from [Java 7](./Java 7 - Classes and Objects.md). Imagine we hade the abstract class `Animal`.

A `Dog` is an animal, as is a `Cat`. They are tangible, concrete things. They share properties, and could inherit from the same parent class, `Animal`.

But you can't have an `Animal` without it being something like a `Cat` or `Dog`. It's too vague, too abstract.

### Abstract Class

An abstract class **cannot be initialised**.

```java
public abstract class Animal {
  protected String name;

  public Animal( String name )
  {
    this.name = name;
  }
}
```

All animals have a `name`, so anything that inherits from `Animal` will also have a name.

Note that children of `Animal` will **not be able to see any `private` variables** . Instead, use the `protected` access modifier.

A `protected` variable makes it so **only the class itself and any children can read its content**.

### Concrete Class

A concrete class **can be initialised**.

```java
public class Dog extends Animal {

  public Dog( String name )
  {
    super( name );
  }

  public String getName()
  {
    return this.name;
  }
}
```

Note the `extends` keyword. That means that the **class is inheriting from `Animal`**

the `super` keyword **calls the constructor of the inherited class**. It's redundant if you aren't passing any parameters to the parent's constructor.

Instantiating the `Dog` class will give you access to the `public` or `protected` properties of the inherited class in the new `Dog` object.
