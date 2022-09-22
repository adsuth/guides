# Java 9 - Interfaces

**Interfaces** play into **Polymorphism**, another one of the **FOUR PILLARS OF OBJECT ORIENTED PROGRAMMING** (that never gets old). It's definitely weirdest name of the four, but if you know a bit of Greek you can kinda guess what it means. 

  *Poly* meaning many

  *Morphism* meaning shapes or forms

**Polymorphism** is the concept of have **objects be recognised as different types depending on the situation**. More on that in it's own part, now what is an interface?

An **interface** is a collection of "promised methods" that any class implementing it will have.

For example, if I had a collection of `SmartDevice` classes, each of them would expect `turnOff()` and `turnOn()` methods.

We could then have an **interface** that ensures each device has **some kind of implementation of those two methods**.

##### Anatomy

```java
public interface Turnable()
{
  public void turnOn();
  public void turnOff();
}
```

That's all there is to it. Just a collection of **method signatures** without the bodies. A class would **implement** an interface like so,

```java
public class Light implements Turnable
{
  private boolean isOn;

  public Light() {}

  @Override
  public void turnOn()
  {
    isOn = true;
  }
  @Override
  public void turnOff()
  {
    isOn = false;
  }

}
```

Note the `implements` keyword. That means

Netbeans will warn you of any unimplemented methods with the lightbulb icon with a red exclamation point. Click it and select `implement all abstract methods`.

`@Override` just indicates that the method is being overridden from the interface. You can ignore it.

##### Okay, but why?

Great question. Imagine you have a bunch of classes that you *know* you can turn off, but you can't have every class the same array as they are different types.

Well, if each of the **implement the `Turnable` interface**, you can use **Polymorphism** to have all of these different classes be read as the same.

*for the below example, `TV` and `Radio` are nearly identical to `Light`*

```java
TV    tv    = new TV();
Radio radio = new Radio();
Light light = new Light();

Turnable[] turnables = { tv, radio, light };

for ( int i = 0; i < turnables.length; i++ )
{
  turnables[i].turnOff();
}
```

Boom. We have successfully turned off all of our devices. This is a *really* basic example, but I hope you can see the value of this.

Important note: **objects of the `Turnable` type will only have access to the methods defined in the `Turnable` interface**. You won't be able to use, for example, the `TV` class's `changeChannel()` method, or `Light` class's `changeColor()` method.
