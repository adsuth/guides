# Java 6 - Methods

**Methods** (or functions) are blocks of code that you can alias and run anywhere.

### In the Main Class

```java
public class Main {

  public static void main( String[] args )
  {
    // calling a functions
    myFunction();
  }

  public static void myFunction()
  {
    // logic for the function here
  }

}
```

Notice that the function is defined **outside the `main` method, but within the `Main` class**

##### Anatomy

```java
public static void myFunction()
{
  // logic for function
}
```

- The first line is known as the **method signature**.

- `public` is an access modifier ( see more about that here [Access Modifiers](./Java X - Access Modifiers.md) )

- `static` means the method can be called **without instantiating the class** (more on what that means later)

- `void` is the return type. This can be any type, primitive or non-primitive. `void` means **nothing is returned**

- `myFunction` is the name of the function. Obviously, can be anything you like.

##### Parameters

Parameters are values you can pass into a function. This is best shown with an example

*First, define the function like always*

```java
public void greet( String firstname, String lastname )
{
  System.out.println( "Hello, " + firstname + " " + lastname );
}
```

The above method has two parameters, `firstname` and `lastname`. We have to explicitly declare their type in the **method signature**.

When we call this method, we can provide the values of these parameters to be used when running the code

```java
greet( "Ben", "Benderson" );
// > Hello, Ben Benderson
```

##### Returning

Methods can **return** values when called. This, again, is exemplified with an demonstration.

*Observe the following method*

```java
public int findSum( int a, int b )
{
  return a + b;
}
```

*When we call this method, it returns the value of `a + b`*

```java
int sum = findSum( 3, 7 );
// sum >> 10
```
